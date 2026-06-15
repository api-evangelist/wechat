# WeChat (wechat)

WeChat (Weixin) is Tencent's flagship super-app, combining messaging, social, payments, mini-apps, official-account publishing, video, enterprise collaboration, and cloud hosting under a single identity. Its developer surface spans the WeChat Open Platform (third-party app login and authorization), Mini Programs (client and server APIs), Mini Games, Official Accounts and Service Accounts, WeChat Pay (APIv3 for mainland China and Global v3 for cross-border merchants), WeChat Work / WeCom (Enterprise WeChat), WeChat Channels (Video Accounts), WeChat Shop, and WeChat Cloud Hosting — addressing over a billion monthly active users primarily in China and across the WeChat international footprint.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/wechat/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/wechat/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- Messaging
- Social
- Payments
- Mini Programs
- Mini Games
- Official Accounts
- Enterprise Communication
- Cloud Hosting
- Video
- Identity
- China
- Super App
- Tencent

## Timestamps

- **Created:** 2026-05-22
- **Modified:** 2026-05-29

## APIs

### WeChat Mini Programs Server API

Backend HTTPS/JSON APIs that Mini Program operators call from their own servers to authenticate user sessions (code2Session), mint access tokens, send customer service and template/subscription messages, generate Mini Program codes / QR codes, run content moderation (msgSecCheck, imgSecCheck, mediaCheckAsync), pull analytics (retention, visit trends, user portraits, page distribution), manage logistics, manage plugins, and verify SOTER biometric signatures. This is the server-side counterpart to the Mini Program JS framework and the primary integration surface for Mini Program publishers.

- **Human URL:** [https://developers.weixin.qq.com/miniprogram/en/dev/api-backend/](https://developers.weixin.qq.com/miniprogram/en/dev/api-backend/)
- **Base URL:** `https://api.weixin.qq.com`

#### Tags

- Mini Programs
- Server API
- Authentication
- Messaging
- Content Moderation
- Analytics
- QR Codes

#### Properties

- [API Reference](https://developers.weixin.qq.com/miniprogram/en/dev/api-backend/)
- [Documentation](https://developers.weixin.qq.com/miniprogram/en/dev/framework/)
- [Getting Started](https://developers.weixin.qq.com/miniprogram/en/dev/framework/quickstart/)
- [Authentication](https://developers.weixin.qq.com/miniprogram/dev/api-backend/open-api/login/auth.code2Session.html)
- [Postman Collection](collections/wechat.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wechat.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### WeChat Mini Programs Client API

Client-side JavaScript API exposed inside the WeChat runtime to Mini Programs and Mini Games. Covers network (wx.request, wx.downloadFile, wx.uploadFile), storage, UI / navigation, media (audio, video, camera, image), location, device (Bluetooth, NFC, Wi-Fi, sensors), file system, canvas, payment invocation (wx.requestPayment), login (wx.login), and the WeChat-provided UI components. Apps are built with WXML / WXSS / JS and packaged via the WeChat Developer Tools.

- **Human URL:** [https://developers.weixin.qq.com/miniprogram/en/dev/api/](https://developers.weixin.qq.com/miniprogram/en/dev/api/)

#### Tags

- Mini Programs
- Mini Games
- Client SDK
- JavaScript
- Devices

#### Properties

- [API Reference](https://developers.weixin.qq.com/miniprogram/en/dev/api/)
- [Documentation](https://developers.weixin.qq.com/miniprogram/en/dev/framework/)
- [I D E Support](https://developers.weixin.qq.com/miniprogram/dev/devtools/devtools.html)
- [SDK](https://github.com/wechat-miniprogram/api-typings)
- [Postman Collection](collections/wechat.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wechat.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### WeChat Pay APIv3 (Direct-Connect Merchant)

WeChat Pay's third-generation REST API for mainland-China direct-connect merchants. Authenticates with merchant API certificates and platform-key signed requests over HTTPS/JSON. Covers JSAPI / Native / App / H5 / Mini Program payments, refunds, bill download, merchant transfers, WeChat Pay Score, vouchers, marketing red packets, profit sharing, consumer complaints, and platform certificate rotation. Replaces the legacy XML-based APIv2.

- **Human URL:** [https://pay.weixin.qq.com/wiki/doc/apiv3/en/index.shtml](https://pay.weixin.qq.com/wiki/doc/apiv3/en/index.shtml)
- **Base URL:** `https://api.mch.weixin.qq.com`

#### Tags

- Payments
- WeChat Pay
- Refunds
- Marketing
- Profit Sharing
- Transfers

#### Properties

- [API Reference](https://pay.weixin.qq.com/wiki/doc/apiv3/en/index.shtml)
- [Documentation](https://pay.weixin.qq.com/wiki/doc/apiv3/en/index.shtml)
- [Login](https://pay.weixin.qq.com/index.php/core/home/login)
- [Portal](https://pay.weixin.qq.com/)
- [SDK](https://github.com/wechatpay-apiv3/wechatpay-java)
- [SDK](https://github.com/wechatpay-apiv3/wechatpay-go)
- [SDK](https://github.com/wechatpay-apiv3/wechatpay-php)
- [Code Examples](https://github.com/wechatpay-apiv3/wechatpay-postman-script)
- [C L I](https://github.com/wechatpay-apiv3/CertificateDownloader)
- [AsyncAPI](asyncapi/wechat-webhooks-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Postman Collection](collections/wechat.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wechat.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### WeChat Pay APIv3 (Service Provider / Partner)

WeChat Pay's APIv3 in "service provider" mode, used by payment platforms and ISVs to onboard and operate sub-merchants. Adds combined-order JSAPI/Native/App payments, sub-merchant onboarding ("特约商户进件"), sub-merchant settlement and bill journals, partner-mode refunds, profit sharing across sub-merchants, marketing tooling, and consumer complaint handling on behalf of sub-merchants.

- **Human URL:** [https://pay.weixin.qq.com/wiki/doc/apiv3_partner/en/index.shtml](https://pay.weixin.qq.com/wiki/doc/apiv3_partner/en/index.shtml)
- **Base URL:** `https://api.mch.weixin.qq.com`

#### Tags

- Payments
- WeChat Pay
- Service Provider
- Sub-Merchants
- Onboarding
- Profit Sharing

#### Properties

- [API Reference](https://pay.weixin.qq.com/wiki/doc/apiv3_partner/en/index.shtml)
- [Documentation](https://pay.weixin.qq.com/wiki/doc/apiv3_partner/en/index.shtml)
- [Postman Collection](collections/wechat.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wechat.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### WeChat Pay Global v3 API

Cross-border WeChat Pay surface for international institutions and merchants accepting payments from WeChat users outside mainland China. Provides a "universal version for global institutions and merchants" with multi-currency settlement, refunds, and reconciliation distinct from the mainland APIv3.

- **Human URL:** [https://pay.weixin.qq.com/doc/global/v3/en/index.html](https://pay.weixin.qq.com/doc/global/v3/en/index.html)

#### Tags

- Payments
- WeChat Pay
- Cross-Border
- International
- Multi-Currency

#### Properties

- [Documentation](https://pay.weixin.qq.com/doc/global/v3/en/index.html)
- [Portal](https://pay.weixin.qq.com/index.php/public/wechatpay_en)
- [Postman Collection](collections/wechat.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wechat.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### WeChat Open Platform — Mobile App Login (OAuth 2.0)

OAuth 2.0 authorization flow exposed by the WeChat Open Platform for native iOS, Android, and HarmonyOS apps. Apps redirect into WeChat to obtain an authorization code, then exchange it via `https://api.weixin.qq.com/sns/oauth2/access_token` for an access token (snsapi_userinfo scope), refresh tokens via `/sns/oauth2/refresh_token`, and fetch profile via `/sns/userinfo`. Access tokens expire in 7200 seconds; refresh tokens last 180 days. Underpins "Login with WeChat" across third-party mobile apps.

- **Human URL:** [https://developers.weixin.qq.com/doc/oplatform/Mobile_App/WeChat_Login/Development_Guide.html](https://developers.weixin.qq.com/doc/oplatform/Mobile_App/WeChat_Login/Development_Guide.html)
- **Base URL:** `https://api.weixin.qq.com`

#### Tags

- Identity
- OAuth
- Login
- Mobile
- Open Platform

#### Properties

- [Documentation](https://developers.weixin.qq.com/doc/oplatform/Mobile_App/WeChat_Login/Development_Guide.html)
- [Portal](https://open.weixin.qq.com/)
- [API Reference](https://developers.weixin.qq.com/doc/oplatform/Mobile_App/WeChat_Login/Authorized_Interface_Calling_UnionID.html)
- [Postman Collection](collections/wechat.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wechat.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### WeChat Open Platform — Website Login (QR OAuth)

Web-based OAuth 2.0 login that renders a WeChat QR code on third-party websites. End users scan the code in WeChat to authenticate; the website receives a code on its callback URL and exchanges it for a snsapi_login access token plus the user's WeChat OpenID / UnionID. Standard way of adding "Sign in with WeChat" to non-WeChat web properties.

- **Human URL:** [https://developers.weixin.qq.com/doc/oplatform/Website_App/WeChat_Login/Wechat_Login.html](https://developers.weixin.qq.com/doc/oplatform/Website_App/WeChat_Login/Wechat_Login.html)

#### Tags

- Identity
- OAuth
- Login
- Web
- QR Code

#### Properties

- [Documentation](https://developers.weixin.qq.com/doc/oplatform/Website_App/WeChat_Login/Wechat_Login.html)
- [Portal](https://open.weixin.qq.com/)
- [Postman Collection](collections/wechat.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wechat.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### WeChat Open Platform — Third-Party Platform API

API surface that lets authorized ISVs operate Official Accounts and Mini Programs on behalf of merchant clients ("代商家调用接口"). Covers merchant authorization onboarding, developing Mini Programs on behalf of merchants (registration, certification, code template upload, version management), initiating web authorization, handling messages and events, using the JS-SDK on behalf of accounts, cloud development integration, domain configuration, privacy settings, and merchant-violation notifications.

- **Human URL:** [https://developers.weixin.qq.com/doc/oplatform/Third-party_Platforms/Authorization_Process_Technical_Description.html](https://developers.weixin.qq.com/doc/oplatform/Third-party_Platforms/Authorization_Process_Technical_Description.html)

#### Tags

- Open Platform
- Third-Party Platform
- ISV
- Delegation
- Mini Programs
- Official Accounts

#### Properties

- [Documentation](https://developers.weixin.qq.com/doc/oplatform/Third-party_Platforms/Authorization_Process_Technical_Description.html)
- [Portal](https://open.weixin.qq.com/cgi-bin/frame?t=home/wx_plugin&lang=zh_CN)
- [Postman Collection](collections/wechat.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wechat.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### WeChat Official Accounts API

HTTPS/JSON APIs for WeChat Official Accounts (Subscription Accounts and Service Accounts) — the publishing surface used by media, brands, and businesses to reach WeChat followers. Surface includes user-info & tagging, message receipt and reply (text, image, voice, video, news), template messages, customer service messages, custom menus, materials and asset management, QR code with scene parameters, web authorization (snsapi_base / snsapi_userinfo), and the JS-SDK for embedded webpages.

- **Human URL:** [https://developers.weixin.qq.com/doc/offiaccount/Getting_Started/Overview.html](https://developers.weixin.qq.com/doc/offiaccount/Getting_Started/Overview.html)
- **Base URL:** `https://api.weixin.qq.com`

#### Tags

- Official Accounts
- Subscription Account
- Service Account
- Messaging
- Templates
- JS SDK

#### Properties

- [Documentation](https://developers.weixin.qq.com/doc/offiaccount/Getting_Started/Overview.html)
- [Portal](https://mp.weixin.qq.com/)
- [AsyncAPI](asyncapi/wechat-webhooks-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Postman Collection](collections/wechat.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wechat.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### WeChat Work (WeCom) API

Server API for Enterprise WeChat / WeCom — Tencent's enterprise collaboration suite. All calls are HTTPS/JSON, UTF-8 encoded, and require an access token. Covers Contacts management (members, departments, tags), messaging & event callbacks, group chat sessions and passive reply, External Contacts (customer management, departing-employee inheritance, customer groups, moments), web OAuth / Web login components / secondary verification, Office Automation (mail, document collaboration, calendar, meetings, cloud drive, livestreaming), enterprise payments (red envelopes, employee payment, external collections / invoicing), conversation-content archive for compliance, school/parent communication, civic / grid services, and the AI & data zone for analytics and knowledge bases.

- **Human URL:** [https://developer.work.weixin.qq.com/document/path/90664](https://developer.work.weixin.qq.com/document/path/90664)
- **Base URL:** `https://qyapi.weixin.qq.com`

#### Tags

- WeCom
- Enterprise WeChat
- Collaboration
- Contacts
- Messaging
- External Contacts
- Office
- Compliance

#### Properties

- [Documentation](https://developer.work.weixin.qq.com/document/path/90664)
- [Developer Portal](https://developer.work.weixin.qq.com/)
- [Login](https://work.weixin.qq.com/wework_admin/loginpage_wx)
- [SDK](https://github.com/sbzhu/weworkapi_python)
- [AsyncAPI](asyncapi/wechat-webhooks-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Postman Collection](collections/wechat.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wechat.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### WeChat Cloud Hosting API

WeChat Cloud Hosting (微信云托管) is Tencent's cloud-native, ops-free container deployment service tightly integrated into the WeChat ecosystem. Documented as "a cloud-native, operations-free, highly available service deployment solution that requires no servers and enables deployment in just one minute." Exposes container deployment APIs, serverless MySQL, object storage with CDN and security validation, native token access (no auth layer needed to call WeChat APIs), the cloud-call service relaying WeChat APIs, message-push routing, WeChat Pay integration without encryption handling, gray deployment and version rollback, real-time log search, resource monitoring, custom alerts, and Enterprise WeChat robot notifications. Supports Node.js, Go, Python, and Java containers plus official templates.

- **Human URL:** [https://developers.weixin.qq.com/miniprogram/dev/wxcloudrun/src/basic/intro.html](https://developers.weixin.qq.com/miniprogram/dev/wxcloudrun/src/basic/intro.html)

#### Tags

- Cloud Hosting
- Containers
- Serverless
- Backend
- MySQL
- Object Storage
- DevOps

#### Properties

- [Documentation](https://developers.weixin.qq.com/miniprogram/dev/wxcloudrun/src/basic/intro.html)
- [Portal](https://cloud.weixin.qq.com/)
- [Postman Collection](collections/wechat.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wechat.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### WeChat Channels (Video Accounts) Developer Surface

WeChat Channels (视频号) is WeChat's short-video and livestreaming product. The developer surface — exposed through the Mini Programs platform and Channels merchant tools — covers livestream room creation, livestream goods linkage, Channels-driven traffic into Mini Programs, and merchant integrations. There is no fully public OpenAPI; most APIs are gated to qualified Channels merchants and partners.

- **Human URL:** [https://channels.weixin.qq.com/developers](https://channels.weixin.qq.com/developers)

#### Tags

- Video Accounts
- Channels
- Live Streaming
- Short Video
- Commerce

#### Properties

- [Documentation](https://channels.weixin.qq.com/developers)
- [Portal](https://channels.weixin.qq.com/)
- [Postman Collection](collections/wechat.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wechat.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### WeChat Shop (微信小店) API

WeChat Shop (微信小店) is WeChat's unified merchant storefront tying together Mini Programs, Channels livestreaming, Official Accounts, and WeChat Search. APIs cover product (SPU/SKU) management, order lifecycle, after-sales, logistics, inventory, vouchers, and merchant-side fulfilment hooks for the integrated WeChat commerce graph.

- **Human URL:** [https://developers.weixin.qq.com/miniprogram/dev/platform-capabilities/industry/mini-shop/](https://developers.weixin.qq.com/miniprogram/dev/platform-capabilities/industry/mini-shop/)

#### Tags

- Commerce
- Shop
- Products
- Orders
- Logistics

#### Properties

- [Documentation](https://developers.weixin.qq.com/miniprogram/dev/platform-capabilities/industry/mini-shop/)
- [Portal](https://shop.weixin.qq.com/)
- [Postman Collection](collections/wechat.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wechat.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://www.wechat.com/)
- [Portal](https://weixin.qq.com/)
- [Developer Portal](https://developers.weixin.qq.com/)
- [Documentation](https://developers.weixin.qq.com/doc/)
- [API Reference](https://developers.weixin.qq.com/miniprogram/en/dev/)
- [Getting Started](https://developers.weixin.qq.com/miniprogram/en/dev/framework/quickstart/)
- [Support](https://developers.weixin.qq.com/community/develop/doc)
- [Hub](https://developers.weixin.qq.com/community/)
- [Console](https://mp.weixin.qq.com/)
- [Portal](https://pay.weixin.qq.com/)
- [Login](https://pay.weixin.qq.com/index.php/core/home/login)
- [Portal](https://work.weixin.qq.com/)
- [Developer Portal](https://developer.work.weixin.qq.com/)
- [Portal](https://open.weixin.qq.com/)
- [Portal](https://channels.weixin.qq.com/)
- [Portal](https://cloud.weixin.qq.com/)
- [Portal](https://shop.weixin.qq.com/)
- [GitHub Organization](https://github.com/wechat-miniprogram)
- [GitHub Organization](https://github.com/wechatpay-apiv3)
- [Code Examples](https://github.com/wechat-miniprogram/miniprogram-demo)
- [SDK](https://github.com/wechat-miniprogram/weui-miniprogram)
- [SDK](https://github.com/wechat-miniprogram/api-typings)
- [SDK](https://github.com/wechat-miniprogram/threejs-miniprogram)
- [SDK](https://github.com/Tencent/weui)
- [SDK](https://github.com/wechatpay-apiv3/wechatpay-java)
- [SDK](https://github.com/wechatpay-apiv3/wechatpay-go)
- [SDK](https://github.com/wechatpay-apiv3/wechatpay-php)
- [SDK](https://github.com/wechatpay-apiv3/wechatpay-apache-httpclient)
- [SDK](https://github.com/wechatpay-apiv3/wechatpay-guzzle-middleware)
- [Code Examples](https://github.com/wechatpay-apiv3/wechatpay-postman-script)
- [C L I](https://github.com/wechatpay-apiv3/CertificateDownloader)
- [I D E Support](https://developers.weixin.qq.com/miniprogram/dev/devtools/devtools.html)
- [Terms of Service](https://www.weixin.qq.com/agreement?lang=en_US)
- [Privacy Policy](https://www.tencent.com/en-us/privacy-policy.html)
- [Support](https://kf.qq.com/)
- [Support](https://service.weixin.qq.com/)
- [Features](undefined)
- [Notes](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
**URL:** https://developers.weixin.qq.com/
