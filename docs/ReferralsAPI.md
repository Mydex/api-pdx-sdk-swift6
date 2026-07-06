# ReferralsAPI

All URIs are relative to *https://api.mydex.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getAllReferrals**](ReferralsAPI.md#getallreferrals) | **GET** /referrals/read-all | Retrieve rall referrals for a given member.
[**getSingleReferral**](ReferralsAPI.md#getsinglereferral) | **GET** /referrals/read-single | Retrieve a single referral by id for a given member.
[**postSelfReferral**](ReferralsAPI.md#postselfreferral) | **POST** /referrals/self-refer | Supports self-referral.
[**updateReferralStatus**](ReferralsAPI.md#updatereferralstatus) | **PUT** /referrals/update-status | Supports updating the status of a referral.


# **getAllReferrals**
```swift
    open class func getAllReferrals(connectionToken: String, uid: String, conId: String, completion: @escaping (_ data: ReferralListResponse?, _ error: Error?) -> Void)
```

Retrieve rall referrals for a given member.

Returns a list of referrals.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let connectionToken = "connectionToken_example" // String | Member's Connection Key
let uid = "uid_example" // String | The unique ID of a mydex member
let conId = "conId_example" // String | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.

// Retrieve rall referrals for a given member.
ReferralsAPI.getAllReferrals(connectionToken: connectionToken, uid: uid, conId: conId) { (response, error) in
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

[**ReferralListResponse**](ReferralListResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getSingleReferral**
```swift
    open class func getSingleReferral(connectionToken: String, uid: String, conId: String, id: String, completion: @escaping (_ data: ReferralSingleResponse?, _ error: Error?) -> Void)
```

Retrieve a single referral by id for a given member.

Returns the requested referral.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let connectionToken = "connectionToken_example" // String | Member's Connection Key
let uid = "uid_example" // String | The unique ID of a mydex member
let conId = "conId_example" // String | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
let id = "id_example" // String | The record id requested.

// Retrieve a single referral by id for a given member.
ReferralsAPI.getSingleReferral(connectionToken: connectionToken, uid: uid, conId: conId, id: id) { (response, error) in
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
 **id** | **String** | The record id requested. | 

### Return type

[**ReferralSingleResponse**](ReferralSingleResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **postSelfReferral**
```swift
    open class func postSelfReferral(connectionToken: String, uid: String, conId: String, selfReferralRequestBody: SelfReferralRequestBody? = nil, completion: @escaping (_ data: CreateResponse?, _ error: Error?) -> Void)
```

Supports self-referral.

Creates a new referral of type 'Self Referred' in the member's PDS.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let connectionToken = "connectionToken_example" // String | Member's Connection Key
let uid = "uid_example" // String | The unique ID of a mydex member
let conId = "conId_example" // String | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
let selfReferralRequestBody = SelfReferralRequestBody(serviceId: 123, referreeBackground: "referreeBackground_example", referreeRequirements: "referreeRequirements_example", referreeAvailability: ReferralCommonRequestBodyFields_referree_availability(AM: ["AM_example"], PM: ["PM_example"]), referrerName: "referrerName_example", serviceName: "serviceName_example", serviceDescription: "serviceDescription_example", serviceUrl: "serviceUrl_example", serviceEmail: "serviceEmail_example", contactNumber: "contactNumber_example", memo: "memo_example", startTime: 123) // SelfReferralRequestBody |  (optional)

// Supports self-referral.
ReferralsAPI.postSelfReferral(connectionToken: connectionToken, uid: uid, conId: conId, selfReferralRequestBody: selfReferralRequestBody) { (response, error) in
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
 **selfReferralRequestBody** | [**SelfReferralRequestBody**](SelfReferralRequestBody.md) |  | [optional] 

### Return type

[**CreateResponse**](CreateResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateReferralStatus**
```swift
    open class func updateReferralStatus(connectionToken: String, uid: String, conId: String, referralStatusUpdateRequestBody: ReferralStatusUpdateRequestBody? = nil, completion: @escaping (_ data: UpdateResponse?, _ error: Error?) -> Void)
```

Supports updating the status of a referral.

Updates the status of a member's referral specified by id. For example, having been referred to a service, the status is set by default to 'Referred' and this route enables it to be updated to 'Accepted' or 'Rejected'

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let connectionToken = "connectionToken_example" // String | Member's Connection Key
let uid = "uid_example" // String | The unique ID of a mydex member
let conId = "conId_example" // String | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
let referralStatusUpdateRequestBody = ReferralStatusUpdateRequestBody(id: 123, status: "status_example") // ReferralStatusUpdateRequestBody |  (optional)

// Supports updating the status of a referral.
ReferralsAPI.updateReferralStatus(connectionToken: connectionToken, uid: uid, conId: conId, referralStatusUpdateRequestBody: referralStatusUpdateRequestBody) { (response, error) in
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
 **referralStatusUpdateRequestBody** | [**ReferralStatusUpdateRequestBody**](ReferralStatusUpdateRequestBody.md) |  | [optional] 

### Return type

[**UpdateResponse**](UpdateResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

