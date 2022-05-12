# dbtonfhir-vscode

This is the README for your extension "dbtonfhir-vscode". After writing up a brief description, we recommend including the following sections.

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

`fhiridentifier` to create:
```
'identifier',
json_build_array(
    json_build_object(
        'use', '',
        'type', json_build_object(
            'text', ,
            'coding',
            json_build_array(
                json_build_object(
                    'system', ,
                    'version', ,
                    'code', ,
                    'display', ,
                    'userSelected', 
                )
            ),
        ),
        'system', ,
        'value', ,
        'period', json_build_object(
            'start', ,
            'end', 
        ),
        assigner, ,
    ),
),
```
