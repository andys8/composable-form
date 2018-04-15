  * [Login](Login.elm) shows a simple login form with 3 fields.
  * [Signup](Signup.elm) showcases a select field, a _meta_ field and external form errors.
  * [ReusingValues](ReusingValues.elm) shows how field values are decoupled from any form, and how they can be reused with a single source of truth. It also showcases an optional field.
  * [Composability](Composability) shows three different approaches to form composition:
    * [Simple](Composability/Simple.elm) uses `Form.wrapValues`
    * [WithConfiguration](Composability/WithConfiguration.elm) uses a function that configures the composable form
    * [WithExtensibleRecords](Composability/WithExtensibleRecords.elm) uses extensible records