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
SizedBox (height)

```json
	"SizedBoxHeight": {
		"prefix": "sizedboxh",
		"body": [
			"const SizedBox(height: $1),",
		]
	},
```

SizedBox (width)

```json
	"SizedBoxHeight": {
		"prefix": "sizedboxh",
		"body": [
			"const SizedBox(height: $1),",
		]
	},
```



## Bloc

Bloc

```json
	"Bloc": {
		"prefix": "bloc",
		"body": [
			"import 'package:flutter_bloc/flutter_bloc.dart';",
			"import 'package:equatable/equatable.dart';",
			"part '${TM_FILENAME/bloc/event/}';",
			"part '${TM_FILENAME/bloc/state/}';",
			"",
			"class ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/g} extends Bloc<$1,$2>{",
			"\t${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/g}() : super($3);",
			"",
			"}",
		]
	},
```

Event

```json
	"Event": {
		"prefix": "event",
		"body": [
			"part of '${TM_FILENAME/event/bloc/}';",
			"",
			"abstract class ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/g} extends Equatable{",
			"\tconst ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/g}();",
			"",
			"\t@override",
			"\tList<Object?> get props => [];",
			"}",
		]
	},
```

State

```json
	"State": {
		"prefix": "state",
		"body": [
			"part of '${TM_FILENAME/state/bloc/}';",
			"",
			"class ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/g} extends Equatable{",
			"\tconst ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/g}();",
			"",
			"\t@override",
			"\tList<Object?> get props => [];",
			"}",
		]
	},
```

## Data

Data class JsonSerializable(createToJson: false)

```json
	"dataClassFrom": {
		"prefix": "dataClassFrom",
		"body": [
			"import 'package:json_annotation/json_annotation.dart';",
			"",
			"part '$TM_FILENAME_BASE.g.dart';",
			"",
			"@JsonSerializable(createToJson: false)",
			"class ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/g}{",
			"\tconst ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/g}();",
			"",
			"\tfactory ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/g}.fromJson(Map<String, dynamic> json) => _$${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/g}FromJson(json);",
			"",
			"\t$1",
			"}",
		]
	},
```

Data class JsonSerializable(createToJson: false)

```json
	"dataClassFrom": {
		"prefix": "dataClassFrom",
		"body": [
			"import 'package:json_annotation/json_annotation.dart';",
			"",
			"part '$TM_FILENAME_BASE.g.dart';",
			"",
			"@JsonSerializable(createToJson: false)",
			"class ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/g}{",
			"\tconst ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/g}();",
			"",
			"\tfactory ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/g}.fromJson(Map<String, dynamic> json) => _$${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/g}FromJson(json);",
			"",
			"\t$1",
			"}",
		]
	},
```

Data class

```json
	"dataClass": {
		"prefix": "dataClass",
		"body": [
			"class ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/g}{",
			"\tconst ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/g}();",
			"",
			"\t$1",
			"}",
		]
	},
```



