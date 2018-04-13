# elm-wip-form

A WIP form API for Elm.

This package aims to streamline form handling in Elm.


## Demo/Examples

Try out the [live demo](https://hecrj.github.io/elm-wip-form) and/or
[check out the examples](examples).


## Introduction

The basic idea of this package is to treat forms as composable pipelines of data. The input being
the current untrusted values of the fields, and the output being validated values that we can trust.
Therefore, this package defines a `Form values output` type.

These pipelines of data are composed of fields. Each field describes how to access data from `values`
(`values -> Value a`), validate it (`value -> Result String b`), and how to update it
(`Value a -> values -> values`), alongside other field attributes.

Finally, a `Form values output` can be rendered as `Html output`. The `Form` API allows the renderer
to access each field individually with its value and update strategy. The `Form` API also allows
the renderer to access the resulting output of the `Form`, so the renderer can set an
`onSubmit` event with the produced `output` when validation succeeds, or show the form errors when
validation fails.


## Extensibility

The main `Form` module is basically built on top of the `Form.Base` module. `Form.Base` exposes a
slightly different form type: `Form values output field`. It should be possible to build your own form API
on top of `Form.Base` with your own custom field type (examples pending, see [Form](src/Form.elm) and
[Form.View](src/Form/View.elm) for now).
