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

```typescript
type ProjectDoc = {
	created_at: bigint;
	data: ProjectDocData;
	key: string;
	owner: string;
	updated_at: bigint;
};
```

### project doc `.data` object

```typescript
type ProjectDocData = {
	// main
	name: string;
	slug: string;
	description: string;
	// categories is an array of strings: project may be in more than one category
	categories: string[];

	// main links
	logo: string;
	website: string;
	canister: string;

	// social links
	twitter: string;
	discord: string;
	telegram: string;
	github: string;
	medium: string;

	// social ic links
	dscvr: string;
	distrikt: string;
	openchat: string;
	taggr: string;
	seers: string;
	nuance: string;
	catalyze: string;
	funded: string;

	// additional
	app: string;
	docs: string;
	faq: string;
	whitepaper: string;
	grantee: null | boolean;

	// nft main
	nft_sale_date: string;
	nft_units: string;
	nft_unit_price: string;
	nft_sale_url: string;

	// nft markets
	nft_market: string;
	// 🔗 entrepot.app
	nft_market_entrepot: string;
	// 🔗 skeh5-daaaa-aaaai-aar4q-cai.raw.ic0.app
	nft_market_ccc: string;
	// 🔗 tppkg-ziaaa-aaaal-qatrq-cai.raw.ic0.app
	nft_market_yumi: string;

	// nft rarity checkers
	nft_rarity: string;
	// 🔗 dgdg.app
	nft_rarity_dgdg: string;

	// nft stats
	nft_stats: string;
	nft_stats_nftgeek: string;

	// nft image examples
	nft_img_1: string;
	nft_img_2: string;
	nft_img_3: string;
	nft_img_4: string;

	// metadata
	added: null | boolean;
	updated: null | number;
	archived: null | number;
};
```

### list of project categories

· · ·

If you have any questions, please reach out on [Twitter](https://twitter.com/cyqlio) or [Telegram](https://t.me/tomkoom)
