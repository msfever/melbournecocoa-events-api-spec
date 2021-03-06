# Melbourne CocoaHeads Events API Spec

## Swagger 2.0

This spec is written using the [Swagger/OpenAPI 2.0 spec][5]. 

## Online Documentation

Documentation is available at http://docs.melbournecocoaheads.apiary.io

## Pawprints

Open this spec with paw [https://paw.pt/cfikVJT4][4]

## Tests

You can test the production api against the swagger.yml file using the [dredd][2] tool. Dredd is setup as a dependency in the `package.json`. A compatible node version is specified for [nvm][3] in the `.nvmrc` file.

```zsh
$ nvm use
# Found '/.../events-api-spec/.nvmrc' with version <v6.10>
# Now using node v6.10.1 (npm v3.10.10)

$ npm i

$ npm run test

# pass: GET /api/events duration: 2061ms
# complete: 1 passing, 0 failing, 0 errors, 0 skipped, 1 total
# complete: Tests took 2065ms
```

## Swift Code Generation

This project relies on [swagger-codegen][1] which can be installed with homebrew on macOS to generate a swift3 api client.

```
swagger-codegen generate -i swagger.yaml -l swift3 -o ApiClient
```


[1]: https://github.com/swagger-api/swagger-codegen
[2]: https://dredd.readthedocs.io
[3]: https://github.com/creationix/nvm
[4]: https://paw.pt/cfikVJT4
[5]: https://github.com/OAI/OpenAPI-Specification/blob/master/versions/2.0.md