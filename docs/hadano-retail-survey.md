# Hadano retail survey

Tracked by issue #4. Remote survey date: 2026-10-02.

## Result

The remote pass verified the main Hadano-area retail targets, but **did not verify a current shelf price for red pickled ginger at any Hadano store**.

This is an important result rather than a missing-data failure: chain product pages, flyers, and store pages do not establish a store's ordinary shelf price unless they explicitly identify the Hadano store and SKU.

Accordingly:

- no historical or chain-wide price is copied into the Hadano shelf-price field;
- chain-standard prices are stored separately as reference prices;
- local availability remains `unknown` until a store-specific source or direct observation exists.

Canonical files:

- `data/hadano-stores.csv`
- `data/hadano-retail-observations.csv`

## Highest-priority targets

### 1. 業務スーパー秦野店

The store is officially verified at 秦野市今泉台3-18-16.

The official site currently exposes **at least two distinct 1 kg SKUs with the same product name**:

1. **P002 / JAN 4942355166528 / page 3695**
   - China origin
   - solid amount 1 kg
   - salt equivalent 2.4 g/100 g
   - ingredient list explicitly includes acidulant, amino-acid seasoning, stevia, potassium sorbate and Red 102
2. **P008 / JAN 4942355166511 / page 4464**
   - China origin
   - solid amount 1 kg
   - salt equivalent 2.4 g/100 g
   - accessible official page does not populate the ingredient field
   - official online page currently reports out of stock

These are not treated as interchangeable. In particular, additive evidence from JAN 6528 must not be copied to JAN 6511.

Therefore the Hadano field check must record the **JAN on the actual package** in addition to price and availability.

Current state:

- local SKU/JAN: unknown
- local availability: unknown
- Hadano shelf price: unknown
- field priority: **highest**

Store:
https://www.gyomusuper.jp/shop/detail.php?sh_id=588

Candidate products:
- https://www.gyomusuper.jp/onlineshop/products/detail/3695
- https://www.gyomusuper.jp/onlineshop/products/detail/4464

### 2. イオン秦野店

The store is officially verified at 秦野市入船町12-1.

Topvalu Best Price currently sells a 60 g red pickled ginger SKU:

- JAN 4901810486755
- Thai ginger
- red-radish color
- 60 g
- standard AEON-group price: ¥116.64 tax included
- salt equivalent: 4.7 g per 60 g = approximately 7.83 g/100 g
- shelf life: 120 days

The Topvalu page explicitly states that the shown price is the **AEON-group standard retail price** and actual price varies by store.

Therefore ¥116.64 is a chain benchmark, **not an observed Hadano price**.

Store:
https://www.aeon.com/store/list/%E7%B7%8F%E5%90%88%E3%82%B9%E3%83%BC%E3%83%91%E3%83%BC/%E3%82%A4%E3%82%AA%E3%83%B3%E3%83%BB%E3%82%A4%E3%82%AA%E3%83%B3%E3%82%B9%E3%82%BF%E3%82%A4%E3%83%AB/%E9%96%A2%E6%9D%B1%E5%9C%B0%E6%96%B9/%E7%A5%9E%E5%A5%88%E5%B7%9D%E7%9C%8C/%E3%82%A4%E3%82%AA%E3%83%B3%E7%A7%A6%E9%87%8E%E5%BA%97/

Product:
https://www.topvalu.net/items/detail/4901810486755/

### 3. ロピア秦野店 / ロピア渋沢店

Both stores are present in the official Lopia store directory.

No current red-pickled-ginger SKU or shelf price was found in accessible current web material.

Field observation is required.

### 4. ヨークフーズ秦野緑町店 / 西大竹店

Both stores are present in the current York store directory.

Current flyer material for 秦野緑町店 was checked; red pickled ginger was not among the published sale items. This **does not mean the store lacks it**—ordinary shelf products are not exhaustively listed in flyers.

Field observation is required.

### 5. ベルク フォルテ秦野店

The official store page and current flyer are available. Current published flyer items were checked and no red-pickled-ginger SKU was found.

Again, absence from the flyer is not evidence of absence from the shelf.

### 6. マックスバリュ秦野東田原店 / 秦野渋沢店

Both current stores are verified by MaxValu Tokai.

The Topvalu 60 g item is a plausible chain candidate but local availability and shelf price remain unverified.

## Why the field survey matters

At approximately 300 g/month, a trip made only to save tens of yen on a small pack can erase the food-cost advantage. The valuable targets are therefore:

1. large packs near the normal shopping route;
2. products with unusually low sodium;
3. products with a solid-weight price far below mail-order alternatives;
4. products whose label resolves additive concentration or ingredient uncertainty.

## Minimal in-store capture protocol

For each red-pickled-ginger SKU, capture:

1. shelf label with tax-included price
2. package front
3. ingredient label
4. nutrition label
5. net / solid weight
6. country of origin
7. JAN code
8. store + date

If photography is inconvenient, record at minimum:

`store | date | product | JAN | tax-included price | net g | solid g | salt g/100g | colorant | preservative | sweetener | origin`

## Priority route

For information gain per stop:

1. 業務スーパー秦野店 — establishes the local price of the current low-sodium 1 kg baseline.
2. イオン秦野店 — checks whether the Topvalu 60 g benchmark is actually stocked and at what local price.
3. ロピア秦野店 — high probability of a competing value-oriented SKU but currently no web-verifiable product data.
4. ベルク フォルテ秦野店 / ヨークフーズ — useful conventional-supermarket comparators.
5. Other Hadano supermarkets if the first four do not produce a strong natural-color / low-sodium option.

## Completion criterion for issue #4

Do not close #4 until at least:

- the 業務スーパー秦野店 1 kg SKU has a dated local price/availability observation, and
- at least two competing Hadano stores have dated shelf observations.

Remote work alone cannot honestly satisfy that criterion with the currently public data.
