# # BroadbandAvailability

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Name of the product. | [optional]
**range_bottom** | **float** | Bottom of the speed range of the product. | [optional]
**range_top** | **float** | Top of the speed range of the product. | [optional]
**likely_down_speed** | **float** | Likely down speed of the product. | [optional]
**likely_up_speed** | **float** | Likely up speed of the product. | [optional]
**availability** | **bool** | Availability of the product. |
**availability_date** | **\DateTime** | Availability date. | [optional]
**speed_range** | **string** | Downstream range (Mbps). | [optional]
**speed_range_up** | **string** | Upstream range (Mbps) - Available for AnnexM, FTTC and G.Fast. | [optional]
**provider** | **string** | Provider.&lt;p&gt;Possible values:&lt;/p&gt;  &lt;ul&gt;  &lt;li&gt;&lt;b&gt;1&lt;/b&gt; - WBC 21CN.&lt;/li&gt;  &lt;li&gt;&lt;b&gt;3&lt;/b&gt; - WBC 20CN.&lt;/li&gt;  &lt;li&gt;&lt;b&gt;4&lt;/b&gt; - Cable &amp; Wireless.&lt;/li&gt;  &lt;li&gt;&lt;b&gt;5&lt;/b&gt; - TalkTalk&lt;/li&gt;  &lt;li&gt;&lt;b&gt;7&lt;/b&gt; - TalkTalk&lt;/li&gt;  &lt;li&gt;&lt;b&gt;8&lt;/b&gt; - Vodafone&lt;/li&gt;  &lt;/ul&gt; |
**technology** | **string** | Technology. | [optional]
**limited_capacity** | **bool** | Whether there is a limited capacity at the exchange. |
**availability_flag** | **string** | Detailed product availability&lt;p&gt;Possible values:&lt;/p&gt;  &lt;ul&gt;  &lt;li&gt;&lt;b&gt;0&lt;/b&gt; - Unknown&lt;/li&gt;  &lt;li&gt;&lt;b&gt;1&lt;/b&gt; - Available&lt;/li&gt;  &lt;li&gt;&lt;b&gt;2&lt;/b&gt; - Not available&lt;/li&gt;  &lt;li&gt;&lt;b&gt;3&lt;/b&gt; - Planned&lt;/li&gt;  &lt;li&gt;&lt;b&gt;4&lt;/b&gt; - Potentially available&lt;/li&gt;  &lt;li&gt;&lt;b&gt;5&lt;/b&gt; - Limited Capacity&lt;/li&gt;  &lt;li&gt;&lt;b&gt;6&lt;/b&gt; - Prohibited&lt;/li&gt;  &lt;/ul&gt; | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
