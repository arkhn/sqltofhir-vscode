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

For any data type, make sure you write `fhir` in the prefix.
