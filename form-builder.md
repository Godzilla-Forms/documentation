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

To access the build you can go to [https://godzilla-forms.io/](https://godzilla-forms.io)

## Create a new account

If you would like to create a new account, you can do so by clicking on the `Sign Up` button on the top right corner of
the page. this is only *required* if you want to save your forms to the cloud and access them later to modify or so.

## Create a new form

To create a new form, you can click on the `Builder` button on the top right corner of the page. This will navigate you
to the wizard page.
You will find two options there, `Start from scratch` and `Import a form`.

### Start from scratch

From the left side of the page, you can drag and drop the elements to the canvas. You will find two sections,
the `Form Elements` and `Ready Froms`.
The `Form Elements` section contains all the elements that you can add to the form. The `Ready Forms` section contains
some pre-made forms that you can use as a starting point.
To configure any elements, you can click on the element and the configuration will be displayed on the right side of the
page.

### Import from JSON

If you have a form that you have created before, you can import it by clicking on the `Import a form` button on the
builder page.

## Edit a form

There's two ways to edit a form, you can either [import](#import-from-json) it from the builder page if you already have
the json or if it's
saved on your account you can go to the `My Forms` page and click on the `Edit` button.

## Export a form

If you are done with your form, you can export it by clicking on the `Genrate` button on the top of the
page. This will open a modal with the json of the form. you need to copy the json and save it on your client side to use
it later with [Godzilla Parser](parser-quickstart.md).


