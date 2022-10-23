# Form Builder

The form builder is a web application that allows you to create dynamic forms and export them as json.

So far the builder supports the following elements:

* Short Text
* Long Text
* Number
* Date **(WIP)**
* Time **(WIP)**
* Drop Down
* Radio Group
* Checkbox
* File
* Heading
* Tel
* Email
* Password
* URL
* Color picker

Each element has its own configuration that can be customized. For example, the default short text element has the
following
configuration:

```json
  {
  "id": "nSICoo8",
  "label": "Short Text",
  "placeholder": "Type here",
  "type": "text",
  "value": {
    "defaultValue": ""
  },
  "errors": {},
  "validators": {
    "required": true
  },
  "options": {},
  "style": {
    "col": 12
  }
}

```

The `id` is a unique identifier for each element, the `value` is the default value for the element and so on.
Each setting will be explained in the [Configurations](builder-configurations.md) section.
