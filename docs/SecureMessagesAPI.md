# SecureMessagesAPI

All URIs are relative to *https://api.mydex.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getSecureMessageConversation**](SecureMessagesAPI.md#getsecuremessageconversation) | **GET** /secure-messages/conversation | Retrieve all secure messages for a given conversation.
[**postSecureMessageReceive**](SecureMessagesAPI.md#postsecuremessagereceive) | **POST** /secure-messages/receive | Supports sending a message to the member&#39;s PDS.
[**postSecureMessageSend**](SecureMessagesAPI.md#postsecuremessagesend) | **POST** /secure-messages/send | Supports sending a message from the member&#39;s PDS.


# **getSecureMessageConversation**
```swift
    open class func getSecureMessageConversation(connectionToken: String, uid: String, conId: String, conversationId: String, completion: @escaping (_ data: SecureMessageConversationResponse?, _ error: Error?) -> Void)
```

Retrieve all secure messages for a given conversation.

Returns a list of secure messages that form part of a conversation.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let connectionToken = "connectionToken_example" // String | Member's Connection Key
let uid = "uid_example" // String | The unique ID of a mydex member
let conId = "conId_example" // String | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
let conversationId = "conversationId_example" // String | The specific ID of the conversation that groups messages together

// Retrieve all secure messages for a given conversation.
SecureMessagesAPI.getSecureMessageConversation(connectionToken: connectionToken, uid: uid, conId: conId, conversationId: conversationId) { (response, error) in
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
 **conversationId** | **String** | The specific ID of the conversation that groups messages together | 

### Return type

[**SecureMessageConversationResponse**](SecureMessageConversationResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **postSecureMessageReceive**
```swift
    open class func postSecureMessageReceive(connectionToken: String, uid: String, conId: String, secureMessageReceiveRequest: SecureMessageReceiveRequest? = nil, completion: @escaping (_ data: CreateResponse?, _ error: Error?) -> Void)
```

Supports sending a message to the member's PDS.

Creates a new received message in the member's PDS.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let connectionToken = "connectionToken_example" // String | Member's Connection Key
let uid = "uid_example" // String | The unique ID of a mydex member
let conId = "conId_example" // String | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
let secureMessageReceiveRequest = SecureMessageReceiveRequest(messageContent: "messageContent_example", conversationId: "conversationId_example", messageFrom: "messageFrom_example") // SecureMessageReceiveRequest |  (optional)

// Supports sending a message to the member's PDS.
SecureMessagesAPI.postSecureMessageReceive(connectionToken: connectionToken, uid: uid, conId: conId, secureMessageReceiveRequest: secureMessageReceiveRequest) { (response, error) in
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
 **secureMessageReceiveRequest** | [**SecureMessageReceiveRequest**](SecureMessageReceiveRequest.md) |  | [optional] 

### Return type

[**CreateResponse**](CreateResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **postSecureMessageSend**
```swift
    open class func postSecureMessageSend(connectionToken: String, uid: String, conId: String, secureMessageSendRequest: SecureMessageSendRequest? = nil, completion: @escaping (_ data: CreateResponse?, _ error: Error?) -> Void)
```

Supports sending a message from the member's PDS.

Creates a new sent message in the member's PDS.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let connectionToken = "connectionToken_example" // String | Member's Connection Key
let uid = "uid_example" // String | The unique ID of a mydex member
let conId = "conId_example" // String | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
let secureMessageSendRequest = SecureMessageSendRequest(messageContent: "messageContent_example", conversationId: "conversationId_example", messageTo: "messageTo_example") // SecureMessageSendRequest |  (optional)

// Supports sending a message from the member's PDS.
SecureMessagesAPI.postSecureMessageSend(connectionToken: connectionToken, uid: uid, conId: conId, secureMessageSendRequest: secureMessageSendRequest) { (response, error) in
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
 **secureMessageSendRequest** | [**SecureMessageSendRequest**](SecureMessageSendRequest.md) |  | [optional] 

### Return type

[**CreateResponse**](CreateResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

