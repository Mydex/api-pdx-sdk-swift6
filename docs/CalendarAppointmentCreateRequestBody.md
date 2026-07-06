# CalendarAppointmentCreateRequestBody

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **String** | Title of the event | 
**description** | **String** | Detailed description of the event | [optional] 
**startTimestamp** | **Int64** | Start date and time as Unix timestamp | 
**endTimestamp** | **Int64** | End date and time as Unix timestamp | 
**status** | **String** | Status of the event | [default to .tentative]
**organiser** | **String** | Creator of the event | [optional] 
**attendee** | **String** | Person attending the event | [optional] 
**location** | **String** | Event location | [optional] 
**context** | **String** | The context the appointment belongs to e.g. a referral | 
**contextId** | **Int** | The id of the specific context record that this appointment relates to e.g. the referral id | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


