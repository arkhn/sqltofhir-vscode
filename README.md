# dbtonfhir-vscode

VSCode snippet package for writing sql queries with dbtonfhir(r) 

## dbtonfhir-vscode

Provides snippets for easily writing the FHIR sql queries with dbtonfhir(r)

Each snipet corresponds to a general-purpose FHIR datatype or to a dbtonfhir function.


## How to install

To use the extension, you shall copy it in your `Users/{username}/.vscode/extensions/`, and reload VSCode.

## How to use 

In a sql file, every dbtonfhir command starts with the prefix `fhir`

`fhirbuildobject` to create: `json_build_object()`

`fhirbuildarray` to create: `json_build_array()`

`fhirselect` to create: 
```
SELECT
    
AS fhir
FROM 
```

`fhir{datatype}` to create a datatype. For exemple, with `fhiridentifier`:
```
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
