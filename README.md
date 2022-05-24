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
| fhiridentifier      | [identifier](https://www.hl7.org/fhir/datatypes.html#Identifier)           |
| fhircoding          | [coding](https://www.hl7.org/fhir/datatypes.html#Coding)                   |
| fhirratio           | [ratio](https://www.hl7.org/fhir/datatypes.html#Ratio)                     |
| fhirperiod          | [period](https://www.hl7.org/fhir/datatypes.html#Period)                   |
| fhirrange           | [range](https://www.hl7.org/fhir/datatypes.html#Range)                     |
| fhirratioRange      | [ratioRange](https://www.hl7.org/fhir/datatypes.html#RatioRange)           |
| fhirattachement     | [attachement](https://www.hl7.org/fhir/datatypes.html#Attachement)         |
| fhirannotation      | [annotation](https://www.hl7.org/fhir/datatypes.html#Annotation)           |
| fhirhumanName       | [humanName](https://www.hl7.org/fhir/datatypes.html#HumanName)             |
| fhircodeableConcept | [codeableConcept](https://www.hl7.org/fhir/datatypes.html#CodeableConcept) |
| fhirtiming          | [timing](https://www.hl7.org/fhir/datatypes.html#Timing)                   |
| fhirmoney           | [money](https://www.hl7.org/fhir/datatypes.html#Money)                     |
| fhiraddress         | [address](https://www.hl7.org/fhir/datatypes.html#Address)                 |
| fhirquantity        | [quantity](https://www.hl7.org/fhir/datatypes.html#Quantity)               |
| fhirsimpleQuantity  | [simpleQuantity](https://www.hl7.org/fhir/datatypes.html#SimpleQuantity)\* |
| fhirmoneyQuantity   | [moneyQuantity](https://www.hl7.org/fhir/datatypes.html#MoneyQuantity)\*   |
| fhircount           | [count](https://www.hl7.org/fhir/datatypes.html#Count)\*                   |
| fhirduration        | [duration](https://www.hl7.org/fhir/datatypes.html#Duration)\*             |
| fhirdistance        | [distance](https://www.hl7.org/fhir/datatypes.html#Distance)\*             |
| fhirage             | [age](https://www.hl7.org/fhir/datatypes.html#Age)\*                       |
| fhirsampledData     | [sampledData](https://www.hl7.org/fhir/datatypes.html#SampledData)         |
| fhirsignature       | [signature](https://www.hl7.org/fhir/datatypes.html#Signature)             |
| fhircontactPoint    | [contactPoint](https://www.hl7.org/fhir/datatypes.html#ContactPoint)       |

##### \* Defined Variations on Quantity
