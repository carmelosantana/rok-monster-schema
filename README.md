# RoK Schema

🌽 This repository will attempt the following;

- Provide up-to-date interface coordinates for Rise of Kingdoms UI elements.
- Unify OCR processes in the RoK data capture community.

---

📢 **Important:** All coordinates currently reference a UI of `1920 x 1080`.

---

📌 Areas that need improvement and could use help from the community;

- Native tools to help build action, ocr, and input templates.
- Determine how best to handle other resolutions when using coordinate arguments.

## Definitions

|Schema|Purpose|
|-|-|
|[Action](#action)|Grouping of inputs to perform an action.|
|[Input](#input)|Allowed inputs as defined by [adb](https://developer.android.com/studio/command-line/adb).|
|[OCR](#ocr)|Instructions for optical character recognition.|

### Actions

Lists several inputs to perform a particular action. Actions should be limited to a *single task*.

#### Definition

|Key|Type|Description|
|-|-|-|
|name|`string`|Unique identifier|
|description|`string`|Describe action|
|input|`array`|Ordered list of [inputs](#input) to perform|

- Keyed by unique `(string)` ID
- 1 action per file

#### Example

```json
{
    "gather-resource-cropland": {
        "name": "Gather corn",
        "description": "Collect resources from Cropland.",
        "input": [
            "map-castle",
            "search-build",
            "search-food",
            "search-food-plus",
            "search-food-search",
            "resource-gather",
            "new-troops",
            "search-march"
        ]
    }
}
```

## Tools

Utilities to help explore the schema and build valid action and input mappings.

- [json-schema-visual-editor](https://hellosean1025.github.io/json-schema-visual-editor/)

## Community

Have a question, idea, or need help getting started? Checkout our [Discord](https://discord.gg/drhxwVQ)!

## Funding

If you find **rok-monster-schema** useful you can help fund future development by making a contribution to one of our funding sources below.

- [PayPal](https://www.paypal.com/donate?hosted_button_id=EKK8CQTPJG7WL)
- Bitcoin `bc1qx7v5vvxwnhpl3dssggy0hytcx2rpq5dkkfwyy4`
- Ethereum `0xA8Ebb6e5EC503E90551dD1bdE2d00B6C126eD5C5`
- Tron `TPnGEfkUZ2py6CFkh8wgqqYehJ29EbMWVw`

## License

The code is licensed [MIT](https://opensource.org/licenses/MIT) and the documentation is licensed [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).
