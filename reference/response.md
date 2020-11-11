---
description: Represents JSON payload returned by NCALayer
---

# Response

| Return Type | Description | Description |
| :--- | :--- | :--- |
| **getResult** | `string` | Result field returned by NCALayer |
| **getResultObject** | `any` | Result field returned by NCALayer without concrete type |
| **getSecondResult** | `string` | Second result field returned by NCALayer |
| **getErrorCode** | `string` | Error code field returned by NCALayer |
| **isOk** | `boolean` | True of error code is equal to `NONE` |
| **isPasswordAttemptsError** | `boolean` | True of error code is equal to `WRONG_PASSWORD` and result contains attempts |
| **isPasswordError** | `boolean` | True of error code is equal to `WRONG_PASSWORD` |
| **isKeyTypeError** | `boolean` | True of error code is equal to `EMPTY_KEY_LIST` |
| **isRdnNotFoundError** | `boolean` | True of error code is equal to `RDN_NOT_FOUND` |
| **isXmlParseError** | `boolean` | True of error code is equal to `XML_PARSE_EXCEPTION` |
| **isSignatureValidationError** | `boolean` | True of error code is equal to `SIGNATURE_VALIDATION_ERROR` |
| **isCommonError** | `boolean` | True of error code is equal to `COMMON` |
| **isKeyStoreError** | `boolean` | True of error code is equal to `LOAD_KEYSTORE_ERROR` |
| **isUnknownStorageError** | `boolean` | True of error code is equal to `UNKNOWN_STORAGE` |
| **isFileReadError** | `boolean` | True of error code is equal to `FILE_READ_ERROR` |



