---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

toc_footers:
  - <a href='https://www.point.red/signup'>Sign Up a new account</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - groups
  - errors

search: true
---

# Introduction

The Point APIs are HTTP-based RESTful APIs that use OAuth 2.0 for authorization. API request and response bodies are formatted in JSON.

# Authentication

> To authorize, use this code:

```shell
curl "api_endpoint_here"
  -H "Authorization: <access_token>"
```

> Make sure to replace `<access_token>` with your API key.

Point uses API `<access_token>` to allow access to the API. You can register a new account [Point Registration](https://www.point.red/signup).

Point expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: Bearer <access_token>`

<aside class="notice">
Important: You cannot run the sample requests in this guide as-is. Replace call-specific parameters such as <access_token> and <id> with your own values.
</aside>
