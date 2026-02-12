# # BroadbandOrderDetails

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**username** | **string** | Name of the user |
**password** | **string** | Password of the user |
**cli** | **string** | Calling line identity | [optional]
**simultaneous_provide** | **bool** | Simultaneous provide |
**sim_code** | **string** | SIM/LORN Code | [optional]
**address_reference** | **string** | The address reference (NAD key). Required for SIM Provide orders | [optional]
**product_id** | **int** | ID of the product |
**activation_date** | **\DateTime** | Activation date |
**fast_track** | **bool** | Fast track order | [optional]
**care_level** | **string** | Care level&lt;p&gt;Possible values:&lt;/p&gt;  &lt;ul&gt;  &lt;li&gt;&lt;b&gt;1&lt;/b&gt; - Standard.&lt;/li&gt;  &lt;li&gt;&lt;b&gt;2&lt;/b&gt; - Enhanced.&lt;/li&gt;  &lt;/ul&gt; |
**send_completion_email** | **bool** | Send completion email |
**ip** | [**\OpenAPI\Client\Model\BroadbandOrderIp**](BroadbandOrderIp.md) |  | [optional]
**ripe** | [**\OpenAPI\Client\Model\BroadbandOrderRIPE**](BroadbandOrderRIPE.md) |  | [optional]
**installation_options** | [**\OpenAPI\Client\Model\BroadbandOrderInstallationOptions**](BroadbandOrderInstallationOptions.md) |  | [optional]
**friendly_name** | **string** | A friendly name for the connection | [optional]
**customer_id** | **int** | ID of the customer associated to the broadband user | [optional]
**tariff_id** | **int** | ID of the broadband tariff associated to the broadband user | [optional]
**number_transfer** | **string** | Number transfer/port option&lt;p&gt;Possible values:&lt;/p&gt;  &lt;ul&gt;  &lt;li&gt;&lt;b&gt;0&lt;/b&gt; - None.&lt;/li&gt;  &lt;li&gt;&lt;b&gt;1&lt;/b&gt; - Morning.&lt;/li&gt;  &lt;li&gt;&lt;b&gt;2&lt;/b&gt; - Afternoon.&lt;/li&gt;  &lt;li&gt;&lt;b&gt;3&lt;/b&gt; - Afternoon.&lt;/li&gt;  &lt;/ul&gt; | [optional]
**cupid** | **int** | CUPID for 3rd party number transfers | [optional]
**ecc** | **int** | Engineering Charge Code. Set to -1 for Not Applicable. | [optional]
**trc** | **int** | Time Related Costs. Set to 0 for up to 1-hour and no charge. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
