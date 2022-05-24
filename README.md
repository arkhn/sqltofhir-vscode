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

| Command name        | Data-type                                                                  |
| ------------------- | -------------------------------------------------------------------------- |
| fhiridentifier      | [Identifier](https://www.hl7.org/fhir/datatypes.html#Identifier)           |
| fhircoding          | [Coding](https://www.hl7.org/fhir/datatypes.html#Coding)                   |
| fhirratio           | [Ratio](https://www.hl7.org/fhir/datatypes.html#Ratio)                     |
| fhirperiod          | [Period](https://www.hl7.org/fhir/datatypes.html#Period)                   |
| fhirrange           | [Range](https://www.hl7.org/fhir/datatypes.html#Range)                     |
| fhirratioRange      | [RatioRange](https://www.hl7.org/fhir/datatypes.html#RatioRange)           |
| fhirattachement     | [Attachement](https://www.hl7.org/fhir/datatypes.html#Attachement)         |
| fhirannotation      | [Annotation](https://www.hl7.org/fhir/datatypes.html#Annotation)           |
| fhirhumanName       | [HumanName](https://www.hl7.org/fhir/datatypes.html#HumanName)             |
| fhircodeableConcept | [CodeableConcept](https://www.hl7.org/fhir/datatypes.html#CodeableConcept) |
| fhirtiming          | [Timing](https://www.hl7.org/fhir/datatypes.html#Timing)                   |
| fhirmoney           | [Money](https://www.hl7.org/fhir/datatypes.html#Money)                     |
| fhiraddress         | [Address](https://www.hl7.org/fhir/datatypes.html#Address)                 |
| fhirquantity        | [Quantity](https://www.hl7.org/fhir/datatypes.html#Quantity)               |
| fhirsimpleQuantity  | [SimpleQuantity](https://www.hl7.org/fhir/datatypes.html#SimpleQuantity)\* |
| fhirmoneyQuantity   | [MoneyQuantity](https://www.hl7.org/fhir/datatypes.html#MoneyQuantity)\*   |
| fhircount           | [Count](https://www.hl7.org/fhir/datatypes.html#Count)\*                   |
| fhirduration        | [Duration](https://www.hl7.org/fhir/datatypes.html#Duration)\*             |
| fhirdistance        | [Distance](https://www.hl7.org/fhir/datatypes.html#Distance)\*             |
| fhirage             | [Age](https://www.hl7.org/fhir/datatypes.html#Age)\*                       |
| fhirsampledData     | [SampledData](https://www.hl7.org/fhir/datatypes.html#SampledData)         |
| fhirsignature       | [Signature](https://www.hl7.org/fhir/datatypes.html#Signature)             |
| fhircontactPoint    | [ContactPoint](https://www.hl7.org/fhir/datatypes.html#ContactPoint)       |

##### \* Defined Variations on Quantity

## Special Purposed Data-Types

| Command name  | Data-type                                                          |
| ------------- | ------------------------------------------------------------------ |
| fhirExtension | [Extension](https://www.hl7.org/fhir/extensibility.html#Extension) |
| fhirMeta      | [Meta](https://www.hl7.org/fhir/resource.html#Meta)                |

## DBT On Fhir References

| Command name   | Data-type |
| -------------- | --------- |
| fhirRefsubject | Subject   |
