# generic_json_annotation

 Annotations that extend `json_annotation`. Used for `Generator` `generic_json_serializable`.

## Usage

```dart
import 'package:json_annotation/json_annotation.dart';
import 'package:generic_json_annotation/generic_json_annotation.dart';

@JsonSerializable()
class ApiResult<T> {
  @JsonKey(name: 'success')
  final bool success;
  @JsonKey(name: 'error')
  final String error;
  @GenericKey(name: 'data')
  final T data;

  ApiResult(this.success, this.error, this.data);
}
```