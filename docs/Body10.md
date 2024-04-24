
# Body10

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** | Name of task |  [optional]
**duration** | **Integer** | Duration of task in milliseconds [1 minute &#x3D; 60000 ms] |  [optional]
**taskTypeId** | **String** | Id for type of task e.g Call / Email / Meeting etc. |  [optional]
**date** | [**OffsetDateTime**] | Task date/time |  [optional]
**notes** | **String** | Notes added to a task |  [optional]
**done** | **Boolean** | Task marked as done |  [optional]
**assignToId** | **String** | To assign a task to a user you can use either the account email or ID. |  [optional]
**contactsIds** | **List&lt;Integer&gt;** | Contact ids for contacts linked to this task |  [optional]
**dealsIds** | **List&lt;String&gt;** | Deal ids for deals a task is linked to |  [optional]
**companiesIds** | **List&lt;String&gt;** | Companies ids for companies a task is linked to |  [optional]



