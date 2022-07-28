# Nexgen CalcEngine Documentation Contents

- [Overview](#Overview)
- [Benefit Requirements Document](#Benefit-Requirements-Document)
    - [Global and Client Merging Flow](#Global-and-Client-Merging-Flow)
    - [BRD Settings](#BRD-Settings)
        - [API DataSource Mappings](#API-DataSource-Mappings)
            - [Massaging to xDS Format](#Massaging-to-xDS-Format)
            - [API DataSource CalcEngine Tables](#API-DataSource-CalcEngine-Tables)

- [Command Processing](#Command-Processing)

# Overview

[TBD]

# Benefit Requirements Document

In the Nexgen framework, the _Benefit Requirements Document CalcEngines_ (BRD) control almost all 'settings/rules' that will control the site experience for each client.  There is a concept of a 'global' BRD that generates settings for all clients, then each client has its own client BRD that merges with, and overrides when necessary, the global settings.

## Global and Client Merging Flow

[TBD]

## BRD Settings

[TBD]

### API DataSource Mappings

Almost all of the data the represents a logged in user is managed and provided by 'Nexgen APIs'.  These API endpoints are documented inside CalcEngines with the BRD being the primary source, however, API endpoints can be specified in other CalcEngines during 'command processing' (See the [Command Processing](#Command-Processing) for more information).  The APIs are called upon login and can also be called later on in the lifecycle to update, refresh, or query data.

#### Massaging to xDS Format

When the API is a _GET_ method, the json data returned from the API is massaged back into xml known as 'xDS format' to ensure that all the framework code from the _BTR Evolution_ and _RBLe_ frameworks continued to work.  The xDS format is represented by Xml structure that has a `Profile` element containing demographic (or non-repeating) data and a `HistoryData` element containing `HistoryItem` elements that represent repeating/transactional data.

**Sample API json response**

```json
{
    "response": {
        "person": {
            "ssn": "911390205",
            "name": {
                "nameLast": "Doe",
                "nameFirst": "John"
            },
            "communication": {
                "addresses": [
                    {
                        "addressType": "HOME",
                        "address1": "123 Normal Way",
                        "city": "New York",
                        "postalCode": "12121",
                        "state": "NY"
                    },
                    {
                        "addressType": "MAILING",
                        "address1": "999 Conduent Towers",
                        "city": "Manhattan",
                        "postalCode": "34343",
                        "state": "NY"
                    }
                ],
            }
        }
    },
    "status": {
        "code": "0",
        "message": "SUCCESS"
    }
}
```

**Resulting xDS Format**

```xml
<xDataDef>
    <Profile>
        <ssn>911390205</ssn>
        <nameFirst>John</nameFirst>
        <nameLast>Doe</nameLast>
    </Profile>
    <HistoryData>
        <HistoryItem hisType="addresses" hisIndex="HOME">
            <index>HOME</index>
            <address1>123 Normal Way</address1>
            <city>New York</city>
            <state>NY</state>
            <postalCode>12121</postalCode>
        </HistoryItem>
        <HistoryItem hisType="addresses" hisIndex="MAILING">
            <index>MAILING</index>
            <address1>999 Conduent Towers</address1>
            <city>Manhattan</city>
            <state>NY</state>
            <postalCode>34343</postalCode>
        </HistoryItem>
    </HistoryData>
</xDataDef>
```

#### API DataSource CalcEngine Tables

There are two tables that describe the mapping rules when converting Nexgen API responses into BTR xDS Format: `apiDataSource` and `apiDataSourceMapping`.  `apiDataSource` is the 'parent' table of `apiDataSourceMapping`.  That is, endpoints can exist in `apiDataSource` without any mappings, however `apiDataSourceMapping` rows are *always* associated with an existing `apiDataSource` row.  `apiDataSourceMapping` rows are primarily used to describe how to map to historical/transactional data.

##### apiDataSource Layout

Column | Description
---|---
id | The name of the API which is then referenced in the `apiDataSourceMapping` table, `requires` column, and in [Command Processing](#Command-Processing).  The name should start with a lower case domain prefix (i.e. `hw`, `db`, `com`) which generally matches with the controller name in the API.
endpoint | The endpoint url (excluding the site url).
runAtLogin | A value indicating whether or not the API should be ran at login (as a _GET_ method).  _Blank_ or `1` will run it, returning `0` indicates that the API should **not** be run.
eligibility | Upon login, if an API should only be ran based on data that is returned from other API(s), an _XPath Expression_ can be provided to run against xDS Data (i.e. `xDataDef/HistoryData/HistoryItem[@hisType='dbCalculationID' and @hisIndex='ACCRUED']`).  If the expression returns a node, then the API can be ran, otherwise it'll be skipped.
requires | When `eligiblity` is specified, a comma delimmited list of ids are required to indicate the APIs that contain the required data to use during the `eligibility` expression evaluation.
mergeMode | Control how historical/transaction data is merged into the current xDS data model.  The default is `Replace` which will _delete all existing history rows_ before adding rows from API results.  Using `Merge` will leave existing history, and _only delete history rows with matching index values_ before adding the rows from API results.

##### apiDataSourceMappings Layout

Column | Description
---|---
dataSource | The `id` of the `apiDataSource` used to relate mappings to an endpoint.
apiTable | The name of the table (array of objects) returned in json responses.
xdsTable | Optional.  If provided, specifies the name of the table name that should be used in xDS profile.  If not provided, `apiTable` is the name that is used.
indexField | Specifies how to generate the unique index for each history row.

# Command Processing

[TBD]