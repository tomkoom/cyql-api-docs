# cyql api `beta`

Query the data from [cyql.io](https://n7ib3-4qaaa-aaaai-qagnq-cai.raw.ic0.app/) – curated Internet Computer projects registry.

> If you use cyql data please reference cyql.io in your app.

## api canister

- canister id: htxcx-3iaaa-aaaal-acd2q-cai
- candid interface: [a4gq6-oaaaa-aaaab-qaa4q-cai.raw.ic0.app/?id=htxcx-3iaaa-aaaal-acd2q-cai](https://a4gq6-oaaaa-aaaab-qaa4q-cai.raw.ic0.app/?id=htxcx-3iaaa-aaaal-acd2q-cai)
- idl files: ...

## query the data

To query the projects from database you need to access the [cyql api canister](https://a4gq6-oaaaa-aaaab-qaa4q-cai.raw.ic0.app/?id=htxcx-3iaaa-aaaal-acd2q-cai) and call one of the methods below, depending on whether you want to get all the projects or one specific project.

### query single documet

#### `get_doc(text, text)`

Method accepts two arguments of type `text`:

1. collection name: `"cyql-projects"`
2. document key: e.g. `"QX8lS9ogfjBJ"`

### query all documets

#### `list_docs(text)`

Method accepts one argument of type `text`:

1. collection name: `"cyql-projects"`

## examples

### query on the frontend

- example: ...

### query from the canister

- example: ...

## data models

### `get_doc` query result

```js
{
    created_at: 0n, // bigint
    data: { ... },  // object (see project doc data notation below)
    key: "",        // string (document key)
    owner: "",      // string (principal id of the owner)
    updated_at: 0n, // bigint
}
```

### project doc `.data` object

```js
{
    // MAIN
    name: "",
    slug: "",
    description: "",
    categories: [], // project may be in more than one category

    // MAIN LINKS
    logo: "",
    website: "",
    canister: "",

    // SOCIAL LINKS
    twitter: "",
    discord: "",
    telegram: "",
    github: "",
    medium: "",

    // SOCIAL IC LINKS
    dscvr: "",
    distrikt: "",
    openchat: "",
    taggr: "",
    seers: "",
    nuance: "",
    catalyze: "",
    funded: "",

    // ADDITIONAL
    app: "",
    docs: "",
    faq: "",
    whitepaper: "",
    grantee: null, // null or boolean

    // NFT MAIN
    nft_sale_date: "",
    nft_units: "",
    nft_unit_price: "",
    nft_sale_url: "",

    // NFT MARKETS
    nft_market_entrepot: "", // entrepot.app
    nft_market_ccc: "",      // skeh5-daaaa-aaaai-aar4q-cai.raw.ic0.app
    nft_market_yumi: "";     // tppkg-ziaaa-aaaal-qatrq-cai.raw.ic0.app

    // NFT RARITY CHECKERS
    nft_rarity_dgdg: "",     // dgdg.app

    // NFT STATS
    nft_stats: "",
    nft_stats_nftgeek: "",

    // NFT IMAGE EXAMPLES
    nft_img_1: "",
    nft_img_2: "",
    nft_img_3: "",
    nft_img_4: "",

    // METADATA
    added: null,    // null or number
    updated: null,  // null or number
    archived: null, // null or boolean
}
```

### list of project categories

· · ·

If you have any questions, please reach out on [Twitter](https://twitter.com/cyqlio) or [Telegram](https://t.me/tomkoom)
