## Changes

### 0.8.37

- Fix loading error on 'yaml' document
- Fix parameter renderer failed on int/number without 'format'
- Windows Support

### 0.8.33

- Support customized headers when making requests

### 0.8.17

- (not support anymore) implicit dereferencing, which is conflict with 'relative file reference'
  ```json
  "definitions":{
    "User":{
    },
    "AuthorizedUser":{
      "$ref": "User"   --> deferenced to "#/definitions/User"
    }
  }
  ```
- __NEW__ relative file reference
  ```
  "definitions":{
    "User": {
      "$ref": "other_folder/User.json"
    }
  }
  ```
- __NEW__ the root object of external documents can be any object (need to be an Swagger/PathItem object before this version)
- fix issue: use 'netloc' only when no host provided.
