# openapi_generator_sample

- openapi-generator-cli を使用してAPI提議書からコードを生成した場合、どのようなコードが生成されるか見る
- dart版 と dart-dio版の2種類があるため、それぞれを別のブランチに分けた

## feature/dart (dart版)
- 以下のコマンドを実行し、生成したコードを追加
```
docker run --rm -v "${PWD}:/local" openapitools/openapi-generator-cli generate \
    -i https://raw.githubusercontent.com/openapitools/openapi-generator/master/modules/openapi-generator/src/test/resources/3_0/petstore.yaml \
    -g dart \
    -o /local/out
```

- ref
  - https://github.com/OpenAPITools/openapi-generator/blob/master/docs/generators/dart.md

## feature/dart-dio (dart-dio版)
- 以下のコマンドを実行し、生成したコードを追加
```
docker run --rm -v "${PWD}:/local" openapitools/openapi-generator-cli generate \
    -i https://raw.githubusercontent.com/openapitools/openapi-generator/master/modules/openapi-generator/src/test/resources/3_0/petstore.yaml \
    -g dart-dio \
    -o /local/out
```

- ref
  - https://github.com/OpenAPITools/openapi-generator/blob/master/docs/generators/dart-dio.md