# cyql api (beta)

Query projects data from [cyql.io](https://n7ib3-4qaaa-aaaai-qagnq-cai.raw.ic0.app/#/) – [Internet Computer](https://internetcomputer.org/) curated projects registry.

## cyql api canister

- cyql api canister id: htxcx-3iaaa-aaaal-acd2q-cai
- candid interface: https://a4gq6-oaaaa-aaaab-qaa4q-cai.raw.ic0.app/?id=htxcx-3iaaa-aaaal-acd2q-cai
- idl files: ...

## query data

To query the projects from database you need to access the [cyql api canister](https://a4gq6-oaaaa-aaaab-qaa4q-cai.raw.ic0.app/?id=htxcx-3iaaa-aaaal-acd2q-cai) and call one of the methods below, depending on whether you want to get all the projects or one specific project.

### query single documet `get_doc(text, text)`

Method accepts two arguments of type `text`:

1. collection name: "cyql-projects"
2. document key: e.g. "QX8lS9ogfjBJ"

### query all documets `list_docs(text)`

Method accepts one argument of type `text`:

1. collection name: "cyql-projects"

## examples

### query on the frontend

- example: ...

### query from the canister

- example: ...

## data models

### project doc

### project doc data

### list of project categories

· · ·

If you have any questions, please reach out on [Twitter](https://twitter.com/cyqlio) or [Telegram](https://t.me/tomkoom)
