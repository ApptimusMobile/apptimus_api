#  Simple API integrated application with api_apptimus

  ```dart
  import 'package:api_apptimus/api_apptimus.dart';

  ApiBaseRequsets apiBaseRequsets = ApiBaseRequsets();
  Future<ApiResult<List<YourModel>>> function(
      ) async {
    try {
      var response = await apiBaseRequsets
          .get('your/api');
      return ApiResult.success(response);
    } catch (e) {
      return ApiResult.failure(NetworkExceptions.getDioException(e));
    }
  }
  ```