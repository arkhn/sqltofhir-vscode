# dbtonfhir-vscode

## How to install

To use the extension, you shall copy it in your `Users/{username}/.vscode/extensions/`, and reload VSCode.

## How to use

In a sql file, every dbtonfhir command starts with the prefix `fhir`.

`fhirbuildobject`:

```sql
json_build_object()
```

`fhirbuildarray`:

```sql
json_build_array()
```

`fhirselect`:

```sql
SELECT

AS fhir
FROM
```

`fhir{datatype}` to create a datatype. For exemple, with `fhiridentifier`:

```sql
'identifier',
json_build_array(
    json_build_object(
        'use', ,
        'type', json_build_object(
            'text', ,
            'coding',
            json_build_array(
                json_build_object(
                    'system', ,
                    'version', ,
                    'code', ,
                    'display', ,
                    'userSelected', ,
                )
            ),
        ),
        'system', ,
        'value', ,
        'period', json_build_object(
            'start', ,
            'end',
        ),
        'assigner', ,
    ),
),
```

`fhirRef{reference}` to create a reference. For exemple, with `fhirRefsubject`:

```sql
'subject',
json_build_object(
    ,
    ,
     :: TEXT
)
```

## General commands

| Command name    | Utility                         |
| --------------- | ------------------------------- |
| fhirselect      | creates a sql SELECT request    |
| fhirbuildobject | creates a `fhir_build_object()` |
| fhirbuildarray  | creates a `fhir_build_array()`  |

## General-purpose data-types

| Command name        | Utility         |
| ------------------- | --------------- |
| fhiridentifier      | identifier      |
| fhircoding          | coding          |
| fhirratio           | ratio           |
| fhirperiod          | period          |
| fhirrange           | range           |
| fhirratioRange      | ratioRange      |
| fhirattachement     | attachement     |
| fhirannotation      | annotation      |
| fhirhumanName       | humanName       |
| fhircodeableConcept | codeableConcept |
| fhirtiming          | timing          |
| fhirmoney           | money           |
| fhiraddress         | address         |
| fhirquantity        | quantity        |
| fhirsimpleQuantity  | simpleQuantity  |
| fhirmoneyQuantity   | moneyQuantity   |
| fhircount           | count           |
| fhirduration        | duration        |
| fhirdistance        | distance        |
| fhirage             | age             |
| fhirsampledData     | sampledData     |
| fhirsignature       | signature       |
| fhircontactPoint    | contactPoint    |
