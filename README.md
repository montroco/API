# API
Montro Public Facing API

## Feed

| FIELD | Type | example | Description |
|:----- |------|---------|-------------|
| sku | string | 13388 | Stock Keeping Unit identifier, used to understand the listings is the same on consecutive re-imports |
| brand | string | Rolex | Brand of the watch, please use original full names if possible: `A. Lange & Söhne`, not `A.Lange & Sohne`; `Rolex`, not `ROLEX`. We correct brand naming on our end. |
| model | string | GMT-Master II | Model line name |
| reference | string | 126710BLNR-0002 | Reference of the model in question, please target to use full reference with variant; hence, for Rolex watches — `126710BLNR-0002` instead of `126710` |
| variant | string | 0002 | Variant of the model in question; For Rolex watches most of the times consists of four digits (matching URL scheme used on their online resources) |
| title | string | GMT-Master II "Batman" | Title of the listing, please refrain from using noisy title specifying extra information such as `full-set`, `2021`, `NEW`. We have explicit fields for this data. We might hide your title if it doesn't follow our community guidelines |
| description | string | | Please use this field to mainly communicate something interesting about the listing, refrain from using unnecessary caps-lock and specifying irrelevant information. We might hide your description if it doesn't follow our community guidelines |
| link | string | [0] | Canonical link to the listing page |
| image_links | string | [1] | Listing's images present on your platform  (todo(ilya): specify image dimensions and quality requirements)|
| availability | boolean | true | Wheather listing is available for purchase |
| price | string | 12000 EUR | Canonical price of the listing with currency according to ISO(todo(ilya):), validated by regexp (todo(ilya)) |
| vat | double | 01 | Value Added Tax if applicable |
| condition | enum[unworn, excellent, very good, good, fair] | good | Condition of the listings, please reference to our legend |
| brand-warranty | boolean | false | Whether the listing has a brand issued warranty |
| brand-warranty-till | DDMMYYYY | 08042025 | Brand warranty expiration date if present |
| brand-only-original-parts | boolean | true | Whether listings contains only the brand original parts |
| year | YYYY | Year the watch in questions was produced |
| serviced | boolean | true | Whether the listing in question was serviced |
| brand-serviced | boolean | true | Whether it was serviced by the brand in question or AD |
| service-date | DDMMYYYY | 08042020 | Date or service |
| service-papers| boolean | true | Where service papers are present |
| water-resistance | boolean | true | Whether the watch is still considered to be water resistant |
| original-box | boolean | true | If original box of the watch is present | 
| original-papers | boolean | true | If the listing has original papers or not| 
| original-receipt | boolean | true | If original receipt is present |
| extract-from-archieves | boolean | true | Weather extract from the archieves is present | 
| merchant-warranty-months | number | 36 | Merchant's warranty duration, expressed in months |
| shipping | string | Within 24h by by DHL | Shipping information |
| delivery-time | sting | Usually within 4-5 working days | Key information about delivery |

[0] https://langedykvintagewatches.com/product/rolex-oyster-perpetual-datejust-blue-16233-1989-full-set-2/
[1] https://langedykvintagewatches.com/wp-content/uploads/2021/09/3D071CEC-B0A3-4E5C-ABEF-FB4C54603425_1_105_c.jpeg,https://langedykvintagewatches.com/wp-content/uploads/2021/09/64E997D0-C08B-4BCC-B317-BC9AC6261BD1_1_105_c.jpeg,https://langedykvintagewatches.com/wp-content/uploads/2021/09/46D07F2E-2BC1-4474-9B59-026B8F9140D6_1_105_c.jpeg,https://langedykvintagewatches.com/wp-content/uploads/2021/09/CEFD2C2E-4849-4F88-9271-8054BEE7D927_1_105_c.jpeg,https://langedykvintagewatches.com/wp-content/uploads/2021/09/874B7247-E81A-4E2B-A067-29ED9ACEB67B_1_105_c.jpeg,https://langedykvintagewatches.com/wp-content/uploads/2021/09/8EFB230D-5A19-495C-A3CD-C61D6AB5CC52_1_105_c.jpeg,https://langedykvintagewatches.com/wp-content/uploads/2021/09/B2D6DBF9-1C8F-4457-89E7-E23E10083689_1_105_c.jpeg,https://langedykvintagewatches.com/wp-content/uploads/2021/09/5DAC3E3B-809B-46AB-AB46-AF1A0ACACCA0_1_105_c.jpeg,https://langedykvintagewatches.com/wp-content/uploads/2021/09/F913607A-5F3F-4811-8C23-FC87C84E7B5F_1_105_c.jpeg
