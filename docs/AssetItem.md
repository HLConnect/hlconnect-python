# AssetItem

Digital asset with complete metadata. Represents a digital product available for purchase, including sheet music, recordings, and other media.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**asset_id** | **int** | Unique identifier for the asset. This is Hal Leonard&#39;s internal identifier for the digital product. | [optional] 
**format_short_name** | **str** | Short name of the asset format (e.g., PVG for Piano/Vocal/Guitar, SSA for Soprano/Soprano/Alto). | [optional] 
**format** | **str** | Full name of the asset format (e.g., Piano/Vocal/Guitar, Soprano/Soprano/Alto). | [optional] 
**page_count** | **int** | The number of pages in the sheet music or document. | [optional] 
**title** | **str** | Title of the asset (song or composition name). | [optional] 
**description** | **str** | Detailed description of the asset, including background information, arrangement details, and other relevant content. | [optional] 
**song_number** | **int** | Hal Leonard&#39;s internal song identifier. This is a unique number assigned to each musical composition. | [optional] 
**public_domain** | **bool** | Indicates whether the song represented by this asset exists in the public domain. | [optional] 
**external_ref** | **str** | Identifier of the company providing the asset. This field identifies the external source or provider of the asset. | [optional] 
**external_ref_id** | **int** | Numeric identifier of the company providing the asset. | [optional] 
**voicing** | **str** | Voicing configuration for choral format assets (e.g., SATB for Soprano/Alto/Tenor/Bass, SSA for Soprano/Soprano/Alto). | [optional] 
**performance_time** | **int** | Performance duration of the asset in seconds. | [optional] 
**difficulty_level_low** | **float** | Lower bound of difficulty level on a scale (typically 1-5 or 1-10). | [optional] 
**difficulty_level_high** | **float** | Upper bound of difficulty level on a scale (typically 1-5 or 1-10). | [optional] 
**min_qty** | **int** | Minimum allowed purchase quantity, typically enforced on choral format assets to ensure complete sets are purchased. | [optional] 
**tempo** | **int** | Tempo of the musical piece in beats per minute (BPM). | [optional] 
**world** | **bool** | Indicates if the asset can be sold in all countries (true) or has geographic restrictions (false). | [optional] 
**retail_price** | **float** | Hal Leonard&#39;s suggested retail price for the asset in the vendor&#39;s currency. | [optional] 
**smd_id** | **str** | SMD (Sheet Music Direct) identifier for the asset. | [optional] 
**asset_type** | **str** | Type classification of the asset (e.g., FOLIO for folio editions, CHMBK for chord books, PCK for packs). | [optional] 
**explicit** | **bool** | Indicator that denotes whether an asset contains graphic material such as profanity in lyrics. | [optional] 
**partable** | **bool** | Indicator that denotes whether an ensemble&#39;s parts may be sold individually. | [optional] 
**countries** | **List[str]** | List of ISO 3166-1 alpha-2 country codes where the asset is available for sale. | [optional] 
**instruments** | [**List[InstrumentItem]**](InstrumentItem.md) | List of instruments associated with the asset. | [optional] 
**categories** | **List[str]** | List of categories that classify the asset (e.g., Pop, Rock, Jazz). | [optional] 
**images** | [**List[ImageItem]**](ImageItem.md) | List of images associated with the asset (cover art, sample pages, etc.). | [optional] 
**contributors** | [**List[ContributorItem]**](ContributorItem.md) | List of contributors (composers, arrangers, editors, etc.) associated with the asset. | [optional] 
**keywords** | **List[str]** | List of keywords associated with the asset for search and discovery. | [optional] 
**related_goods** | [**List[RelatedGoodItem]**](RelatedGoodItem.md) | List of related goods (physical products, digital bundles, etc.) associated with the asset. | [optional] 
**renderings** | [**List[RenderingItem]**](RenderingItem.md) | List of available renderings (formats) for the asset (e.g., PDF, Scorch, MusicXML). | [optional] 
**series** | **List[str]** | List of series that the asset belongs to (e.g., Best Sellers, Top Hits collections). | [optional] 
**skills** | **List[str]** | List of skill levels or educational classifications associated with the asset. | [optional] 
**usergens** | [**List[UsergenItem]**](UsergenItem.md) | List of user-generated content or customization options associated with the asset. | [optional] 
**prices** | [**List[PriceItem]**](PriceItem.md) | List of pricing options for the asset in different currencies or for different customer segments. | [optional] 
**packages** | [**List[PackageItem]**](PackageItem.md) | List of package deals or bundles that include this asset. | [optional] 

## Example

```python
from hlconnect_client.models.asset_item import AssetItem

# TODO update the JSON string below
json = "{}"
# create an instance of AssetItem from a JSON string
asset_item_instance = AssetItem.from_json(json)
# print the JSON string representation of the object
print(AssetItem.to_json())

# convert the object into a dict
asset_item_dict = asset_item_instance.to_dict()
# create an instance of AssetItem from a dict
asset_item_from_dict = AssetItem.from_dict(asset_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


