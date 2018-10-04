# Frontend challenge

### Objective

Create an arbitrary multilevel object/JSON tree-like viewer/editor, all in one, something like the below mockups demonstrates:

![Mockup](/mockup.png?raw=true "Mockup")

### Technology

Use the latest stable release of Angular (6.1.7 at the time of writing) and the latest stable release of TypeScript (3.0.1 at the time of writing). Other than that the challenge does not allow any extra libraries/frameworks to be used.

### Inputs

There are two inputs:

1. The source object (see `source-object-example.json`): is mandatory, and can host the following types of fields:

- `string`
- `number`
- `boolean`
- `object`
- `array`

2. A schema object (see `schema-object-example.json`): is optional, and defines the following properties of a field (excluding the `object` type field):

- `readonly`: determines if the field is readonly (e.g.: `true`)
- `minimalLength`: determines the minimal length of a `string` value (e.g.: `5`)
- `maximalLength`: determines the maximal length of a `string` value (e.g.: `10`)
- `range`: determines the allowed range of a `number` value (e.g.: `{ from: 100, to: 999 }`)
- `values`: determines the allowed values of a `string` or a `number` value (e.g.: `["abc", "def"]` or `[1, 5, 10]`)

Keep in mind that the schema doesn't have to define all the fields. If nothing is specified, the field is nor readonly, nor does it have any value limitations.

### Requirements

- the `string` type field needs to be displayed as a text field
- the `number` type field needs to be displayed as a number field
- the `boolean` type field needs to be displayed as a check box
- the `object` type field needs to be displayed as a nested object
- the `array` type field needs to be displayed as an arbitrary combination of either of the above type fields
- the type of the field is derived from the source and not the schema object
- the readonly fields need to be disabled
- the fields that have value limitations need to be validated upon the click of a button at the end; success as well as validation errors need to be communicated, so we can clearly recognize and repair them
- all the fields (including the `object` type field) need to be removable
- the viewer/editor needs to be expandable/collapsable
- one of the functionalities needs to be thoroughly tested with unit tests
- the application needs to work in the latest Chrome and Internet Explorer 11
- the application needs to implement a consistent UX and design
- the application needs to be responsive down to the iPhone 6/7/8 level/size
- the application styles need to be written with a SCSS preprocessor and need to have some kind of configuration (i.e. variables)
- the application needs to have some kind of a documentation explaining it's workings
- the application needs to be in a new GIT repository within a feature branch (the repository can be hosted on a GIT platform of your choice, although we prefer GitHub)

Keep in mind that not all the requirements must be met for the challenge to be a success, however, unmet requirements will inevitably decrease the overall evaluation.

### Tips

- try to focus on the quality of the solution in terms of modularization, separation of concerns, code reuse, generics, encapsulation, etc.
- try to leverage as much of Angulars and TypeScripts features as possible


### Questions?

If you have any questions, don't hesitate to ask ;)

We think it's a challenging yet fun task, so good luck! :)
