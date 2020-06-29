---
title: 'Dart: Handling HTTP Connections'
date: 2020-04-07 11:59:06
lang: en
direction: ltr
tags:
	- dart
	- dartlang
	- http
	- status
	- connection
	- handling
	
---






```dart
Future<Tuple2<ErrorResponse, T>> fetchItem<T>(String url, Map<String, String> headers, Function jsonConverter,
    {String jsonModelKey, HttpMethod httpMethod = HttpMethod.get, Map body}) async {
  try {
    final Response response =
        httpMethod == HttpMethod.get ? await getRequest(url, headers) : await postRequest(url, headers, body);

    if (response.statusCode == 200) {
      final jsonModel = jsonModelKey == null ? json.decode(response.body) : json.decode(response.body)[jsonModelKey];

      final T model = jsonConverter(jsonModel) as T;

      return Tuple2(null, model);
    } else {
      return Tuple2(ErrorResponse(message: response.body.toString(), statusCode: response.statusCode), null);
    }
  } catch (e) {
    return Tuple2(ErrorResponse(message: e.toString(), statusCode: networkError), null);
  }
}
```

{% gist dae10c703fc760bd6d65c5ba86e937df  %}


