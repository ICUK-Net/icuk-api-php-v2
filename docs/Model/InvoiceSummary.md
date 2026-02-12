# # InvoiceSummary

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**invoice_id** | **int** | Result ID | [optional]
**create_date** | **\DateTime** | Create Date | [optional]
**due_date** | **\DateTime** | Due Date | [optional]
**paid_status** | **string** | Paid Status&lt;p&gt;Possible values:&lt;/p&gt;  &lt;ul&gt;  &lt;li&gt;&lt;b&gt;0&lt;/b&gt; - Unpaid&lt;/li&gt;  &lt;li&gt;&lt;b&gt;1&lt;/b&gt; - Paid&lt;/li&gt;  &lt;li&gt;&lt;b&gt;2&lt;/b&gt; - Overdue&lt;/li&gt;  &lt;li&gt;&lt;b&gt;4&lt;/b&gt; - Processing&lt;/li&gt;  &lt;li&gt;&lt;b&gt;5&lt;/b&gt; - Cancelled&lt;/li&gt;  &lt;li&gt;&lt;b&gt;-1&lt;/b&gt; - Unknown&lt;/li&gt;  &lt;/ul&gt; | [optional]
**payment_method** | **string** | Payment Method&lt;p&gt;Possible values:&lt;/p&gt;  &lt;ul&gt;  &lt;li&gt;&lt;b&gt;0&lt;/b&gt; - Not Paid&lt;/li&gt;  &lt;li&gt;&lt;b&gt;1&lt;/b&gt; - Cheque&lt;/li&gt;  &lt;li&gt;&lt;b&gt;2&lt;/b&gt; - BACS&lt;/li&gt;  &lt;li&gt;&lt;b&gt;3&lt;/b&gt; - Credit Card&lt;/li&gt;  &lt;li&gt;&lt;b&gt;5&lt;/b&gt; - Other&lt;/li&gt;  &lt;li&gt;&lt;b&gt;6&lt;/b&gt; - Direct Debit&lt;/li&gt;  &lt;li&gt;&lt;b&gt;7&lt;/b&gt; - Credit Card Amex&lt;/li&gt;  &lt;/ul&gt; | [optional]
**description** | **string** | Description | [optional]
**invoice_item_list** | [**\OpenAPI\Client\Model\InvoiceItem[]**](InvoiceItem.md) | Invoice Items | [optional]
**invoice_sub_total** | **float** | Sub Total | [optional]
**invoice_vat** | **float** | VAT Total | [optional]
**invoice_total** | **float** | Total | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
