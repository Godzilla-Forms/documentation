# Configurations

**WIP**

All the form elements are shared the same configuration structure, but some of them are optional and some of them are
not, we will explain each element configuration in the [following sections](form-elements.md).
But first, let's take a look at the configuration structure and what we have in Godzilla.

## General

This is the root of the configuration, it contains the following elements:

| Key         | Type   | Required | Default Value         | Note                                                                                                                                                     |
|-------------|--------|----------|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| id          | string | yes      |                       | ID of the filed, can be any string                                                                                                                       |
| label       | string | no       | " "                   |                                                                                                                                                          |
| placeholder | string | no       | " "                   |                                                                                                                                                          |
| subheader   | string | no       | " "                   |                                                                                                                                                          |
| type        | string | yes      | based on form element | can be any of `text`, `password`, `email`, `url`, `tel`, `number`, `color`, `checkbox`, `radio`, `search`, `dropdown`, `textarea`, `heading` or `upload` |
| value       | json   | yes      | {}                    | See [Value Configuration](#value-configuration)                                                                                                          |
| errors      | json   | yes      | {}                    | See [Errors Configuration](#errors-configuration)                                                                                                        |
| validators  | json   | yes      | {}                    | See [Validators Configuration](#validators-configuration)                                                                                                |
| file        | json   | yes      | {}                    | See [File Configuration](#file-configuration)                                                                                                            |
| options     | json   | yes      | {}                    | See [Options Configuration](#options-configuration)                                                                                                      |
| style       | json   | yes      | {}                    | See [Style Configuration](#style-configuration)                                                                                                          |
| flow        | json   | yes      | {}                    | See [Flow Configuration](#flow-configuration)                                                                                                            |

## Value

This will be used to set the default value for the element with some exceptions for some elements that have more than
one value like dropdown and radio group; `valueOptions`, `serviceName` and `valueSource` are used to set the default
values for that's elements. more details about these options will be explained in
the [Options Configuration](#options-configuration) section.

| Key          | Type                         | Required | Default Value | Note                         |
|--------------|------------------------------|----------|---------------|------------------------------|
| defaultValue | string or boolean            | yes      | " "           |                              |
| valueOptions | GodzillaFormCombinedValues[] | no       | null          |                              |
| serviceName  | string                       | no       | null          |                              |
| valueSource  | string                       | no       | "static"      | can be `static` or `service` |

## Validators

This will be used to set the validation rules for the element, the validation rules are:

| Key          | Type    | Required | Default Value | Note                                                  |
|--------------|---------|----------|---------------|-------------------------------------------------------|
| pattern      | string  | no       |               | regex pattern to be validated on the value            |
| required     | boolean | no       |               |                                                       |
| min          | number  | no       |               |                                                       |
| max          | number  | no       |               |                                                       |
| minLength    | number  | no       |               |                                                       |
| maxLength    | number  | no       |               |                                                       |
| maxSize      | number  | no       |               | Only used for file input, more details [File Input]() |
| allowedTypes | number  | no       |               | Only used for file input, more details [File Input]() |

## Errors

This will be used to show the errors messages for the element if there's any errors are enabled by the validator, the
key is the error type and the value is the error message, can be left empty to use the default error message.
for example:

```json
{
  "errors": {
    "required": "This field is required",
    "minLength": "The minimum length is 5",
    "maxLength": "The maximum length is 10"
  }
}
```

| Key       | Type   | Required | Default Value | 
|-----------|--------|----------|---------------|
| pattern   | string | no       | null          | 
| required  | string | no       | null          |
| min       | string | no       | null          |
| max       | string | no       | null          |
| minLength | string | no       | null          | 
| maxLength | string | no       | null          |
| maxSize   | string | no       | null          | 

## Options

This will be used to set the options for the element, the options are:

```json

```

## Style

**TODO**

## Flow

**TODO**
