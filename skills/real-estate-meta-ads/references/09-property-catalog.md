# 09. Property catalog (Facebook, Instagram, WhatsApp)

Research done on 2026-11-15 in Meta's official documentation. Always separate **confirmed in official docs** from **inference**. Re-check before investing time: Meta changes this often.

## What the property catalog is

- A catalog of type **home listings (`home_listings`)** in Commerce Manager. The type **cannot be changed** after creation. One catalog for all properties.
- Fed by an **XML feed** (root `<listings>`, many `<listing>`), CSV or TSV, **by URL on a schedule** (hourly, daily or weekly). A website plugin that generates the XML works if its format matches the fields below.

## Feed fields

| Required for ads | Useful optional |
|---|---|
| `home_listing_id`, `name`, `availability`, `address` (`addr1`, `city`, `region`, `country`, `postal_code`), `latitude`, `longitude`, `neighborhood`, `price`, `image`, `url` | `description`, `num_beds`, `num_baths`, `year_built`, `property_type` (apartment, condo, house, land, townhouse, other…), `listing_type` (for_sale_by_agent, for_rent_by_agent, new_construction…) |

- `availability`: for_sale, for_rent, sale_pending, recently_sold, off_market, available_soon.
- `price`: amount + 3-letter ISO currency code, e.g. `850000 USD` (or EUR, BRL, GBP…).
- **Field names in English**; the values' text may be in any language.
- **A sold property leaves the feed or changes `availability` the same day** (ads for sold properties burn budget and reputation).
- Instagram image: the `INSTAGRAM_STANDARD_PREFERRED` tag picks the photo used there.

## Facebook and Instagram (confirmed in docs)

- Catalog ads ("ads with product media"): **carousel, collection, single image or video**. Instagram: Feed, Stories and Explore (in Stories, collection/map/catalog video do not show).
- Classic objective: `PRODUCT_CATALOG_SALES`. With Leads/Traffic/Engagement, the **conversion location is Website or App** (the click goes to the property page). There is also a catalog ad with an **instant form**.
- For **qualified leads**, combine: catalog ad → property page with form/WhatsApp, and/or the catalog ad with a form. Measure as in `04-tracking-crm.md`.
- Country availability: the documentation read did not list countries or restrictions for these ads, but also did not state availability for every country. **Test with a paused campaign and a small catalog** before uploading everything.

## Housing category with a catalog

- Meta's general real-estate ads page: "Advertisers must specify `HOUSING` as a `special_ad_category` for ad campaigns that market housing" — **without citing countries**.
- Special category page: outside the US, Canada and Europe the field exists but may be `NONE` (see `07-housing-and-local-rules.md`).
- **Not confirmed:** whether Ads Manager forces/suggests Housing when a home-listings catalog is chosen, and whether automated review pauses a property ad marked `NONE`. **First test to run** (paused campaign). If Meta requires it, declare it and tell the owner: that campaign loses lookalikes, age/gender and neighborhood/postal-code targeting.

## WhatsApp — what works and what does not

**Confirmed in official docs (as read on 2026-11-15)**
- API (Cloud API): catalog and multi-product messages require an **e-commerce catalog** (types "Products" and "Services"). **The home-listings catalog (`home_listings`) is not mentioned anywhere** in the WhatsApp documentation. One catalog per account.
- WhatsApp Business app: product/service catalog **entered by hand**; each item is reviewed.
- ⚠ check: ordering tools were scheduled to leave the app on 2026-11-15 (customers still see the catalog).
- Policy: real estate is **not** among restricted items; land in ecological conservation areas, discrimination in housing listings, and content with no item for sale are prohibited.

**Inference (not tested)**
- The Facebook/Instagram property catalog **probably cannot be connected to WhatsApp**. The route would be a **separate e-commerce catalog** with properties entered as "products" (by hand in the app, or via its own feed). Risk of rejection in review: not ruled out.

**Safer official alternatives**
1. **Click-to-WhatsApp ad** (image, video, carousel) with an automated greeting that can include a "view catalog" button.
2. Catalog ad → property page (feed `url`) → WhatsApp button with a prefilled message naming the property.
3. In the conversation, the agent sends the **property link** (website page) instead of a catalog item.
4. Only invest in an e-commerce catalog on WhatsApp if a test shows a real gain; start with items 1–3.

## Next steps (template)

- [ ] Identify the feed source (website plugin, CRM export) and check that the XML includes the required fields above (especially `latitude`, `longitude`, `neighborhood`, `postal_code` and `price` with the currency code).
- [ ] Create a small `home_listings` catalog and test the feed by URL (with the owner's approval, protocol `08-account-changes.md`).
- [ ] A **paused** catalog campaign to see whether Meta requires Housing.
- [ ] Decide about WhatsApp only after running 1–3.
