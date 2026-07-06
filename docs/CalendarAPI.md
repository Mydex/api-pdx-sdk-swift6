# CalendarAPI

All URIs are relative to *https://api.mydex.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteCalendarEvent**](CalendarAPI.md#deletecalendarevent) | **DELETE** /calendar/delete-event | Supports deleting a calendar-event.
[**getCalendarAppointments**](CalendarAPI.md#getcalendarappointments) | **GET** /calendar/get-appointments | Retrieve appointments for a given context
[**getCalendarEvents**](CalendarAPI.md#getcalendarevents) | **GET** /calendar/get-events | Retrieve calendar events
[**postCalendarAppointment**](CalendarAPI.md#postcalendarappointment) | **POST** /calendar/add-appointment | Supports adding a calendar-appointment.
[**postCalendarEvent**](CalendarAPI.md#postcalendarevent) | **POST** /calendar/add-event | Supports adding a calendar-event.
[**putCalendarEvent**](CalendarAPI.md#putcalendarevent) | **PUT** /calendar/update-event | Supports updating a calendar-event.


# **deleteCalendarEvent**
```swift
    open class func deleteCalendarEvent(connectionToken: String, uid: String, conId: String, calendarEventDeleteRequestBody: CalendarEventDeleteRequestBody? = nil, completion: @escaping (_ data: DeleteResponse?, _ error: Error?) -> Void)
```

Supports deleting a calendar-event.

Deletes an event in the user's calendar.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let connectionToken = "connectionToken_example" // String | Member's Connection Key
let uid = "uid_example" // String | The unique ID of a mydex member
let conId = "conId_example" // String | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
let calendarEventDeleteRequestBody = CalendarEventDeleteRequestBody(id: 123) // CalendarEventDeleteRequestBody |  (optional)

// Supports deleting a calendar-event.
CalendarAPI.deleteCalendarEvent(connectionToken: connectionToken, uid: uid, conId: conId, calendarEventDeleteRequestBody: calendarEventDeleteRequestBody) { (response, error) in
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
 **calendarEventDeleteRequestBody** | [**CalendarEventDeleteRequestBody**](CalendarEventDeleteRequestBody.md) |  | [optional] 

### Return type

[**DeleteResponse**](DeleteResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getCalendarAppointments**
```swift
    open class func getCalendarAppointments(connectionToken: String, uid: String, conId: String, context: String, contextId: Int, completion: @escaping (_ data: GetAppointmentsResponse?, _ error: Error?) -> Void)
```

Retrieve appointments for a given context

Returns a list of appointments filtered by context and context_id.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let connectionToken = "connectionToken_example" // String | Member's Connection Key
let uid = "uid_example" // String | The unique ID of a mydex member
let conId = "conId_example" // String | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
let context = "context_example" // String | The context this belongs to
let contextId = 987 // Int | The specific ID of the context record

// Retrieve appointments for a given context
CalendarAPI.getCalendarAppointments(connectionToken: connectionToken, uid: uid, conId: conId, context: context, contextId: contextId) { (response, error) in
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
 **context** | **String** | The context this belongs to | 
 **contextId** | **Int** | The specific ID of the context record | 

### Return type

[**GetAppointmentsResponse**](GetAppointmentsResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getCalendarEvents**
```swift
    open class func getCalendarEvents(connectionToken: String, uid: String, conId: String, completion: @escaping (_ data: GetEventsResponse?, _ error: Error?) -> Void)
```

Retrieve calendar events

Returns a list of calendar events.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let connectionToken = "connectionToken_example" // String | Member's Connection Key
let uid = "uid_example" // String | The unique ID of a mydex member
let conId = "conId_example" // String | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.

// Retrieve calendar events
CalendarAPI.getCalendarEvents(connectionToken: connectionToken, uid: uid, conId: conId) { (response, error) in
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

[**GetEventsResponse**](GetEventsResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **postCalendarAppointment**
```swift
    open class func postCalendarAppointment(connectionToken: String, uid: String, conId: String, calendarAppointmentCreateRequestBody: CalendarAppointmentCreateRequestBody? = nil, completion: @escaping (_ data: CreateResponse?, _ error: Error?) -> Void)
```

Supports adding a calendar-appointment.

Creates a new appointment in the user's calendar. An appointment must be made within a specified context e.g. a 'Referral'

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let connectionToken = "connectionToken_example" // String | Member's Connection Key
let uid = "uid_example" // String | The unique ID of a mydex member
let conId = "conId_example" // String | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
let calendarAppointmentCreateRequestBody = CalendarAppointmentCreateRequestBody(title: "title_example", description: "description_example", startTimestamp: 123, endTimestamp: 123, status: "status_example", organiser: "organiser_example", attendee: "attendee_example", location: "location_example", context: "context_example", contextId: 123) // CalendarAppointmentCreateRequestBody |  (optional)

// Supports adding a calendar-appointment.
CalendarAPI.postCalendarAppointment(connectionToken: connectionToken, uid: uid, conId: conId, calendarAppointmentCreateRequestBody: calendarAppointmentCreateRequestBody) { (response, error) in
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
 **calendarAppointmentCreateRequestBody** | [**CalendarAppointmentCreateRequestBody**](CalendarAppointmentCreateRequestBody.md) |  | [optional] 

### Return type

[**CreateResponse**](CreateResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **postCalendarEvent**
```swift
    open class func postCalendarEvent(connectionToken: String, uid: String, conId: String, calendarEventCreateRequestBody: CalendarEventCreateRequestBody? = nil, completion: @escaping (_ data: CreateResponse?, _ error: Error?) -> Void)
```

Supports adding a calendar-event.

Creates a new event in the user's calendar.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let connectionToken = "connectionToken_example" // String | Member's Connection Key
let uid = "uid_example" // String | The unique ID of a mydex member
let conId = "conId_example" // String | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
let calendarEventCreateRequestBody = CalendarEventCreateRequestBody(title: "title_example", description: "description_example", startTimestamp: 123, endTimestamp: 123, status: "status_example", organiser: "organiser_example", attendee: "attendee_example", location: "location_example", type: "type_example") // CalendarEventCreateRequestBody |  (optional)

// Supports adding a calendar-event.
CalendarAPI.postCalendarEvent(connectionToken: connectionToken, uid: uid, conId: conId, calendarEventCreateRequestBody: calendarEventCreateRequestBody) { (response, error) in
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
 **calendarEventCreateRequestBody** | [**CalendarEventCreateRequestBody**](CalendarEventCreateRequestBody.md) |  | [optional] 

### Return type

[**CreateResponse**](CreateResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **putCalendarEvent**
```swift
    open class func putCalendarEvent(connectionToken: String, uid: String, conId: String, calendarEventUpdateRequestBody: CalendarEventUpdateRequestBody? = nil, completion: @escaping (_ data: UpdateResponse?, _ error: Error?) -> Void)
```

Supports updating a calendar-event.

Updates an event in the user's calendar. For example, updating the 'status' from 'INVITED' to 'CONFIRMED' when a user accepts the invitation to an appointment.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let connectionToken = "connectionToken_example" // String | Member's Connection Key
let uid = "uid_example" // String | The unique ID of a mydex member
let conId = "conId_example" // String | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
let calendarEventUpdateRequestBody = CalendarEventUpdateRequestBody(title: "title_example", description: "description_example", startTimestamp: 123, endTimestamp: 123, status: "status_example", organiser: "organiser_example", attendee: "attendee_example", location: "location_example", id: 123) // CalendarEventUpdateRequestBody |  (optional)

// Supports updating a calendar-event.
CalendarAPI.putCalendarEvent(connectionToken: connectionToken, uid: uid, conId: conId, calendarEventUpdateRequestBody: calendarEventUpdateRequestBody) { (response, error) in
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
 **calendarEventUpdateRequestBody** | [**CalendarEventUpdateRequestBody**](CalendarEventUpdateRequestBody.md) |  | [optional] 

### Return type

[**UpdateResponse**](UpdateResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

