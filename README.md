[![banner](https://raw.githubusercontent.com/oceanprotocol/art/master/github/repo-banner%402x.png)](https://oceanprotocol.com)

<h1 align="center">fileinfo</h1>

> 🐙 Microservice API endpoint to get metadata for any remote file.
> https://fileinfo.oceanprotocol.com

[![Build Status](https://travis-ci.com/oceanprotocol/fileinfo.svg?branch=main)](https://travis-ci.com/oceanprotocol/fileinfo)
[![Vercel deployment](https://flat.badgen.net/badge/vercel/auto-deployment/21c4dd?icon=now)](https://zeit.co/oceanprotocol/fileinfo)
[![js oceanprotocol](https://img.shields.io/badge/js-oceanprotocol-7b1173.svg)](https://github.com/oceanprotocol/eslint-config-oceanprotocol)

**Table of Contents**

- [🏄 Usage](#-usage)
  - [Endpoint](#endpoint)
  - [`[POST] /`](#post-)
- [⬆️ Deployment](#️-deployment)
- [🏛 License](#-license)

## 🏄 Usage

API supports passing `http(s)://` & `ipfs://` URLs via a `POST` request. IPFS URLs are mapped to the configured IPFS gateway.

### Endpoint

```text
https://fileinfo.oceanprotocol.com
```

### `[POST] /`

**_Parameters_**

```json
{
  "url": "https://oceanprotocol.com/tech-whitepaper.pdf"
}
```

**_Response_**

_Success_

```json
{
  "status": "success",
  "result": {
    "contentLength": "2989228",
    "contentType": "application/pdf"
  }
}
```

_Error_

```json
{
  "status": "error",
  "message": "Something went wrong."
}
```

## ⬆️ Deployment

Every branch or Pull Request is automatically deployed by [Vercel](https://vercel.com) with their GitHub integration. A link to a deployment will appear under each Pull Request.

## 🏛 License

```text
Copyright 2020 Ocean Protocol Foundation Ltd.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
