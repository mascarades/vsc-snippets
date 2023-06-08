# Dart Snippets

## Widgets

Stateless Widget

```json
    "stateless": {
        "prefix": "stless",
        "body": [
            "import 'package:flutter/material.dart';",
            "",
            "class ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/} extends StatelessWidget {",
            "\tconst ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/}({super.key});",
            "",
            "\t@override",
            "\tWidget build(BuildContext context) {",
            "\t\treturn $1;",
            "\t}",
            "}",
        ]
    },
```

Stateful Widget

```json
    "statefull": {
        "prefix": "stfull",
        "body": [
            "import 'package:flutter/material.dart';",
            "",
            "class ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/} extends StatefulWidget {",
            "\tconst ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/}({super.key});",
            "",
            "\t@override",
            "\tState<${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/}> createState() => _${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/}State();",
            "}",
            "",
            "class _${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/}State extends State<${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/}> {",
            "\t@override",
            "\tWidget build(BuildContext context) {",
            "\t\treturn $2;",
            "\t}",
            "}",
        ]
    },
```

## Bloc

### Bloc with freezed

Freezed state

```json
    "freezedState": {
        "prefix": "freezedState",
        "body": [
            "import 'package:freezed_annotation/freezed_annotation.dart';",
            "",
            "part '$TM_FILENAME_BASE.freezed.dart';",
            "",
            "@freezed",
            "class ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/g} with _$${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/g}{",
            "\tconst factory ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/g}.initial() = $1;",
            "",
            "}",
        ]
    },
```
