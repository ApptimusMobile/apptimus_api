# **ApiBaseRequests**

ApiBaseRequests is a class that provides methods to make HTTP requests to an API.

## Usage

### Importing

First, import the ApiBaseRequests class into your Dart file:


```dart
import 'package:moura_mobile/core/configs/api_config.dart';
```
### Creating an instance

Create an instance of ApiBaseRequests:


```dart
ApiBaseRequests apiBaseRequests = ApiBaseRequests();
```
### Making GET Requests

You can make GET requests using the get method:

```dart
var response = await apiBaseRequests.get('/api/example');
print(response); // Handle the response accordingly
```

### Making POST Requests

You can make POST requests using the post method:

```dart
var response = await apiBaseRequests.post('/api/example', data: {'key': 'value'});
print(response); // Handle the response accordingly
```
### Handling Responses
Responses are returned as dynamic objects. You can handle them according to your API's response structure.


# ****NetworkExceptions**
**
NetworkExceptions is a class that provides methods to handle network exceptions that may occur during API requests.

## Usage

Importing
First, import the NetworkExceptions class into your Dart file:



```dart
import 'package:moura_mobile/core/exceptions/network_exceptions.dart';
```
Handling Dio Exceptions
You can handle Dio exceptions using the getDioException method:

```dart
try {
  // Make API request
} catch (e) {
  var networkException = NetworkExceptions.getDioException(e);
  print(networkException.message); // Handle the exception accordingly
}
```


## Handling Other Exceptions
You can handle other exceptions using the getDefaultException method:

```dart
try {
  // Make API request
} catch (e) {
  var networkException = NetworkExceptions.getDefaultException(e);
  print(networkException.message); // Handle the exception accordingly
}
```
