# Internal linking and measurement

## Linking principles

Link from knowledge pages to:

* related knowledge pages when the reader needs context;
* the relevant MagicWorks service page when the reader has commercial intent;
* contact or work pages when a next action is genuinely appropriate.

Use descriptive anchor text.

## Main site ↔ knowledge subdomain

Treat both as one owned journey for analytics design.

Do **not** add internal UTM parameters to ordinary navigation between the MagicWorks main domain and its knowledge subdomain. Internal UTMs can overwrite acquisition attribution.

Use GA4 domain/subdomain configuration and explicit events instead.

## Suggested events

Consider events such as:

* `knowledge_service_click`
* `knowledge_contact_click`
* `knowledge_resource_download`
* `knowledge_outbound_reference`
* `knowledge_search`

Names should be finalised against the production analytics plan before implementation.
