# TimelineAPI

All URIs are relative to *https://api.mydex.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getTimeline**](TimelineAPI.md#gettimeline) | **GET** /timeline | Retrieve list of timeline items.
[**getTimelineItem**](TimelineAPI.md#gettimelineitem) | **GET** /timeline/single-item | Retrieve a single timeline item.


# **getTimeline**
```swift
    open class func getTimeline(connectionToken: String, uid: String, conId: String, completion: @escaping (_ data: TimelineResponse?, _ error: Error?) -> Void)
```

Retrieve list of timeline items.

Returns a list of timeline items which includes: referrals, calendar events and secure messages.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let connectionToken = "connectionToken_example" // String | Member's Connection Key
let uid = "uid_example" // String | The unique ID of a mydex member
let conId = "conId_example" // String | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.

// Retrieve list of timeline items.
TimelineAPI.getTimeline(connectionToken: connectionToken, uid: uid, conId: conId) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connectionToken** | **String** | Member&#39;s Connection Key | 
 **uid** | **String** | The unique ID of a mydex member | 
 **conId** | **String** | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID. | 

### Return type

[**TimelineResponse**](TimelineResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getTimelineItem**
```swift
    open class func getTimelineItem(connectionToken: String, uid: String, conId: String, featureBlock: FeatureBlock_getTimelineItem, featureBlockId: Int, completion: @escaping (_ data: TimelineSingleItemResponse?, _ error: Error?) -> Void)
```

Retrieve a single timeline item.

Returns a single timeline item based on feature block and feature block id requested e.g. a 'referral' with id 123.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let connectionToken = "connectionToken_example" // String | Member's Connection Key
let uid = "uid_example" // String | The unique ID of a mydex member
let conId = "conId_example" // String | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
let featureBlock = "featureBlock_example" // String | The feature block the teimline item belongs to
let featureBlockId = 987 // Int | The specific ID of the record within the specified feature block e.g. if 'referrals' is the feature block, then this should be a specific referral id

// Retrieve a single timeline item.
TimelineAPI.getTimelineItem(connectionToken: connectionToken, uid: uid, conId: conId, featureBlock: featureBlock, featureBlockId: featureBlockId) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connectionToken** | **String** | Member&#39;s Connection Key | 
 **uid** | **String** | The unique ID of a mydex member | 
 **conId** | **String** | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID. | 
 **featureBlock** | **String** | The feature block the teimline item belongs to | 
 **featureBlockId** | **Int** | The specific ID of the record within the specified feature block e.g. if &#39;referrals&#39; is the feature block, then this should be a specific referral id | 

### Return type

[**TimelineSingleItemResponse**](TimelineSingleItemResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

