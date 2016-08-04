# Order

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**order_id** | **str** | Order ID | [optional] 
**info_email** | **str** | Customer email | [optional] 
**info_first** | **str** | Customer first name | [optional] 
**info_last** | **str** | Customer last name | [optional] 
**phone** | **str** | Customer phone number | [optional] 
**shipset** | **bool** | Customer billing address matches shipping address | [optional] 
**info_adr1** | **str** | Customer billing address line &#39;1&#39; | [optional] 
**info_adr2** | **str** | Customer billing address line &#39;2&#39; | [optional] 
**info_cty** | **str** | Customer billing city | [optional] 
**info_zip** | **str** | Customer billing zip code | [optional] 
**state** | **str** | Customer billing state | [optional] 
**info_sadr1** | **str** | Customer shipping address line &#39;1&#39; | [optional] 
**info_sadr2** | **str** | Customer shipping address line &#39;2&#39; | [optional] 
**info_scty** | **str** | Customer shipping city | [optional] 
**info_szip** | **str** | Customer shipping zip code | [optional] 
**sstate** | **str** | Customer shipping state | [optional] 
**tax_amount** | **float** | Tax amount in hundreds. Must divide by &#39;100&#39; for USD value | [optional] 
**shipping_amount** | **float** | Shipping total in USD | [optional] 
**amount_total** | **float** | Checkout total in USD | [optional] 
**item_i_ds** | **list[str]** | Array of items purchased at checkout | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


