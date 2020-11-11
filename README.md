---
description: NCALayer JS is a small wrapper around NCALayer web socket API.
---

# 👋 Welcome

## Installation

**Using npm:**

```text
npm install @seithq/ncalayer
```

**Using yarn:**

```text
yarn add @seithq/ncalayer
```

### Usage

```text
import Client from "@seithq/ncalayer"

// Initialize websocket connection with running NCALayer.
let ws = new WebSocket("wss://127.0.0.1:13579/")

// Handle onopen, onerror and onclose events as you want.
ws.onopen = (e) => {
  // your code goes here
}

ws.onerror = (e) => {
  // your code goes here
}

ws.onclose = (e) => {
  // your code goes here
}

// Initialize client to work with API.
const client = new Client(ws)

// Call API method.
client.browseKeyStore("PKCS12", "P12", "", (data) => {
  // on success
  if (data.isOk()) {
    // some action
  }

  // on failure
  console.error(data)
})
```

{% hint style="info" %}
You have to pass `WebSocket` for `Client` constructor without modifying its`onmessage` event listener. Under the hood `Client` instance listen for `onmessage` and performs its internal callback inside it.
{% endhint %}





