---
description: Used to send API requests to NCALayer
---

# Client

## Fields

| Property | Type | Description |
| :--- | :--- | :--- |
| **method** | \`\`[`Method`](method.md)\`\` | Last method has been called |
| **version** | `string` | Current NCALayer version |

## Methods

Basic API wrappers around NCALayer API

### browseKeyStore

| Argument | Type | Description |
| :--- | :--- | :--- |
| **storageName** | `string` | Storage name. Available values: `PKCS12`, `AKKaztokenStore`, `AKKZIDCardStore`, `AKEToken72KStore`, `AKJaCartaStore` |
| **fileExtension** | `string` | File extension. Usually: `P12` |
| **currentDirectory** | `string` | Directory to browse. By default it's home directory |
| **callback** | [`Callback`](https://github.com/seithq/ncalayerjs#callback) | Callback function to be performed on API response |

### showFileChooser

| Argument | Type | Description |
| :--- | :--- | :--- |
| **fileExtension** | `string` | File extension. Usually: `ALL` |
| **currentDirectory** | `string` | Directory to browse. By default it's home directory |
| **callback** | [`Callback`](https://github.com/seithq/ncalayerjs#callback) | Callback function to be performed on API response |

### getKeys

| Argument | Type | Description |
| :--- | :--- | :--- |
| **storageName** | `string` | Storage name. Available values: `PKCS12`, `AKKaztokenStore`, `AKKZIDCardStore`, `AKEToken72KStore`, `AKJaCartaStore` |
| ~~_storagePath_~~ | `string` | Path to key container. Usually result of [`browseKeyStore`](https://github.com/seithq/ncalayerjs#browsekeystore) |
| password | `string` | Key container password |
| type | `string` | Key type. Available values: `AUTH`, `SIGN`, `ALL` |
| callback | [`Callback`](https://github.com/seithq/ncalayerjs#callback) | Callback function to be performed on API response |

### setLocale

| Argument | Type | Description |
| :--- | :--- | :--- |
| lang | `string` | Language code. Available values: `kk`, `ru`, `en` |
| callback | [`Callback`](https://github.com/seithq/ncalayerjs#callback) | Callback function to be performed on API response |

### getNotBefore

| Argument | Type | Description |
| :--- | :--- | :--- |
| storageName | `string` | Storage name. Available values: `PKCS12`, `AKKaztokenStore`, `AKKZIDCardStore`, `AKEToken72KStore`, `AKJaCartaStore` |
| storagePath | `string` | Path to key container. Usually result of [`browseKeyStore`](https://github.com/seithq/ncalayerjs#browsekeystore) |
| keyAlias | `string` | Key alias extracted from key. See helper [`extractKeyAlias`](https://github.com/seithq/ncalayerjs/blob/master/src/helpers.ts) |
| password | `string` | Key container password |
| callback | [`Callback`](https://github.com/seithq/ncalayerjs#callback) | Callback function to be performed on API response |

### getNotAfter

| Argument | Type | Description |
| :--- | :--- | :--- |
| storageName | `string` | Storage name. Available values: `PKCS12`, `AKKaztokenStore`, `AKKZIDCardStore`, `AKEToken72KStore`, `AKJaCartaStore` |
| storagePath | `string` | Path to key container. Usually result of [`browseKeyStore`](https://github.com/seithq/ncalayerjs#browsekeystore) |
| keyAlias | `string` | Key alias extracted from key. See helper [`extractKeyAlias`](https://github.com/seithq/ncalayerjs/blob/master/src/helpers.ts) |
| password | `string` | Key container password |
| callback | [`Callback`](https://github.com/seithq/ncalayerjs#callback) | Callback function to be performed on API response |

### getSubjectDN

| Argument | Type | Description |
| :--- | :--- | :--- |
| storageName | `string` | Storage name. Available values: `PKCS12`, `AKKaztokenStore`, `AKKZIDCardStore`, `AKEToken72KStore`, `AKJaCartaStore` |
| storagePath | `string` | Path to key container. Usually result of [`browseKeyStore`](https://github.com/seithq/ncalayerjs#browsekeystore) |
| keyAlias | `string` | Key alias extracted from key. See helper [`extractKeyAlias`](https://github.com/seithq/ncalayerjs/blob/master/src/helpers.ts) |
| password | `string` | Key container password |
| callback | [`Callback`](https://github.com/seithq/ncalayerjs#callback) | Callback function to be performed on API response |

### getIssuerDN

| Argument | Type | Description |
| :--- | :--- | :--- |
| storageName | `string` | Storage name. Available values: `PKCS12`, `AKKaztokenStore`, `AKKZIDCardStore`, `AKEToken72KStore`, `AKJaCartaStore` |
| storagePath | `string` | Path to key container. Usually result of [`browseKeyStore`](https://github.com/seithq/ncalayerjs#browsekeystore) |
| keyAlias | `string` | Key alias extracted from key. See helper [`extractKeyAlias`](https://github.com/seithq/ncalayerjs/blob/master/src/helpers.ts) |
| password | `string` | Key container password |
| callback | [`Callback`](https://github.com/seithq/ncalayerjs#callback) | Callback function to be performed on API response |

### getRdnByOid

| Argument | Type | Description |
| :--- | :--- | :--- |
| storageName | `string` | Storage name. Available values: `PKCS12`, `AKKaztokenStore`, `AKKZIDCardStore`, `AKEToken72KStore`, `AKJaCartaStore` |
| storagePath | `string` | Path to key container. Usually result of [`browseKeyStore`](https://github.com/seithq/ncalayerjs#browsekeystore) |
| keyAlias | `string` | Key alias extracted from key. See helper [`extractKeyAlias`](https://github.com/seithq/ncalayerjs/blob/master/src/helpers.ts) |
| password | `string` | Key container password |
| oid | `string` | OID code |
| oidIndex | `number` | OID index. Put `0` |
| callback | [`Callback`](https://github.com/seithq/ncalayerjs#callback) | Callback function to be performed on API response |

### signPlainData

| Argument | Type | Description |
| :--- | :--- | :--- |
| storageName | `string` | Storage name. Available values: `PKCS12`, `AKKaztokenStore`, `AKKZIDCardStore`, `AKEToken72KStore`, `AKJaCartaStore` |
| storagePath | `string` | Path to key container. Usually result of [`browseKeyStore`](https://github.com/seithq/ncalayerjs#browsekeystore) |
| keyAlias | `string` | Key alias extracted from key. See helper [`extractKeyAlias`](https://github.com/seithq/ncalayerjs/blob/master/src/helpers.ts) |
| password | `string` | Key container password |
| toSign | `string` | Plain data to be signed |
| callback | [`Callback`](https://github.com/seithq/ncalayerjs#callback) | Callback function to be performed on API response |

### verifyPlainData

| Argument | Type | Description |
| :--- | :--- | :--- |
| storageName | `string` | Storage name. Available values: `PKCS12`, `AKKaztokenStore`, `AKKZIDCardStore`, `AKEToken72KStore`, `AKJaCartaStore` |
| storagePath | `string` | Path to key container. Usually result of [`browseKeyStore`](https://github.com/seithq/ncalayerjs#browsekeystore) |
| keyAlias | `string` | Key alias extracted from key. See helper [`extractKeyAlias`](https://github.com/seithq/ncalayerjs/blob/master/src/helpers.ts) |
| password | `string` | Key container password |
| toVerify | `string` | Original plain data |
| signature | `string` | Signature to be validated |
| callback | [`Callback`](https://github.com/seithq/ncalayerjs#callback) | Callback function to be performed on API response |

### createCMSSignature

| Argument | Type | Description |
| :--- | :--- | :--- |
| storageName | `string` | Storage name. Available values: `PKCS12`, `AKKaztokenStore`, `AKKZIDCardStore`, `AKEToken72KStore`, `AKJaCartaStore` |
| storagePath | `string` | Path to key container. Usually result of [`browseKeyStore`](https://github.com/seithq/ncalayerjs#browsekeystore) |
| keyAlias | `string` | Key alias extracted from key. See helper [`extractKeyAlias`](https://github.com/seithq/ncalayerjs/blob/master/src/helpers.ts) |
| password | `string` | Key container password |
| toSign | `string` | Plain data to be signed |
| attached | `boolean` | Attach data into signature or not |
| callback | [`Callback`](https://github.com/seithq/ncalayerjs#callback) | Callback function to be performed on API response |

### verifyCMSSignature

| Argument | Type | Description |
| :--- | :--- | :--- |
| toVerify | `string` | Original plain data |
| signature | `string` | Signature to be validated |
| callback | [`Callback`](https://github.com/seithq/ncalayerjs#callback) | Callback function to be performed on API response |

### createCMSSignatureFromFile

| Argument | Type | Description |
| :--- | :--- | :--- |
| storageName | `string` | Storage name. Available values: `PKCS12`, `AKKaztokenStore`, `AKKZIDCardStore`, `AKEToken72KStore`, `AKJaCartaStore` |
| storagePath | `string` | Path to key container. Usually result of [`browseKeyStore`](https://github.com/seithq/ncalayerjs#browsekeystore) |
| keyAlias | `string` | Key alias extracted from key. See helper [`extractKeyAlias`](https://github.com/seithq/ncalayerjs/blob/master/src/helpers.ts) |
| password | `string` | Key container password |
| filePath | `string` | File path of content to be signed |
| attached | `boolean` | Attach data into signature or not |
| callback | [`Callback`](https://github.com/seithq/ncalayerjs#callback) | Callback function to be performed on API response |

### verifyCMSSignatureFromFile

| Argument | Type | Description |
| :--- | :--- | :--- |
| filePath | `string` | Original file content |
| signature | `string` | Signature to be validated |
| callback | [`Callback`](https://github.com/seithq/ncalayerjs#callback) | Callback function to be performed on API response |

### signXml

| Argument | Type | Description |
| :--- | :--- | :--- |
| storageName | `string` | Storage name. Available values: `PKCS12`, `AKKaztokenStore`, `AKKZIDCardStore`, `AKEToken72KStore`, `AKJaCartaStore` |
| storagePath | `string` | Path to key container. Usually result of [`browseKeyStore`](https://github.com/seithq/ncalayerjs#browsekeystore) |
| keyAlias | `string` | Key alias extracted from key. See helper [`extractKeyAlias`](https://github.com/seithq/ncalayerjs/blob/master/src/helpers.ts) |
| password | `string` | Key container password |
| toSign | `string` | Raw xml to be signed |
| callback | [`Callback`](https://github.com/seithq/ncalayerjs#callback) | Callback function to be performed on API response |

### verifyXml

| Argument | Type | Description |
| :--- | :--- | :--- |
| signature | `string` | Raw signed xml to be validated |
| callback | [`Callback`](https://github.com/seithq/ncalayerjs#callback) | Callback function to be performed on API response |

### signXmlByElementId

| Argument | Type | Description |
| :--- | :--- | :--- |
| storageName | `string` | Storage name. Available values: `PKCS12`, `AKKaztokenStore`, `AKKZIDCardStore`, `AKEToken72KStore`, `AKJaCartaStore` |
| storagePath | `string` | Path to key container. Usually result of [`browseKeyStore`](https://github.com/seithq/ncalayerjs#browsekeystore) |
| keyAlias | `string` | Key alias extracted from key. See helper [`extractKeyAlias`](https://github.com/seithq/ncalayerjs/blob/master/src/helpers.ts) |
| password | `string` | Key container password |
| toSign | `string` | Raw xml |
| elementName | `string` | Element name to be signed |
| idAttrName | `string` | Element attribute |
| parentElementName | `string` | Element parent node |
| callback | [`Callback`](https://github.com/seithq/ncalayerjs#callback) | Callback function to be performed on API response |

### verifyXmlByElementId

| Argument | Type | Description |
| :--- | :--- | :--- |
| signature | `string` | Raw signed xml to be validated |
| idAttrName | `string` | Element attribute |
| parentElementName | `string` | Element parent node |
| **callback** | `Callback` | Callback function to be performed on API response |

### getHash

| Argument | Type | Description |
| :--- | :--- | :--- |
| **input** | `string` | Plain data to be hashed |
| **digestAlg** | `string` | Digest algorithm name. Available values: `SHA1`, `SHA256`, `GOST34311` |
| **callback** | \`\`[`Callback`](callback.md)\`\` | Callback function to be performed on API response |

###  

