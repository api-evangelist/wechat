# WeChat (wechat)

WeChat (Weixin) is Tencent's flagship super-app — combining messaging, social, payments, mini-apps, official-account publishing, video, enterprise collaboration, and cloud hosting under a single identity used by over a billion people. Its developer surface spans the WeChat Open Platform (third-party app login and authorization), Mini Programs (client and server APIs), Mini Games, Official Accounts and Service Accounts, WeChat Pay (APIv3 for mainland China and Global v3 for cross-border merchants), WeChat Work / WeCom (Enterprise WeChat), WeChat Channels (Video Accounts), WeChat Shop, and WeChat Cloud Hosting.

**URL:** [Visit APIs.yml URL](https://raw.githubusercontent.com/api-evangelist/wechat/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

Messaging, Social, Payments, Mini Programs, Mini Games, Official Accounts, Enterprise Communication, Cloud Hosting, Video, Identity, China, Super App, Tencent

## Timestamps

- **Created:** 2026-05-22
- **Modified:** 2026-05-23

## APIs

### WeChat Mini Programs Server API

Backend HTTPS/JSON APIs that Mini Program operators call from their own servers to authenticate user sessions (`auth.code2Session`), mint global access tokens, send customer-service / template / subscription messages, generate Mini Program codes and QR codes, run content moderation (`security.msgSecCheck`, `security.imgSecCheck`, async media check), pull analytics (retention, visit trends, user portraits, page distribution), manage logistics and plugins, and verify SOTER biometric signatures. Base URL `https://api.weixin.qq.com`.

#### Properties

- [API Reference](https://developers.weixin.qq.com/miniprogram/en/dev/api-backend/)
- [Documentation](https://developers.weixin.qq.com/miniprogram/en/dev/framework/)
- [Getting Started](https://developers.weixin.qq.com/miniprogram/en/dev/framework/quickstart/)

### WeChat Mini Programs Client API

Client-side JavaScript API exposed inside the WeChat runtime to Mini Programs and Mini Games — network (`wx.request`, `wx.downloadFile`, `wx.uploadFile`), storage, UI / navigation, media (audio, video, camera, image), location, device (Bluetooth, NFC, Wi-Fi, sensors), file system, canvas, payment invocation (`wx.requestPayment`), and login (`wx.login`). Apps are built with WXML / WXSS / JS and packaged via the WeChat Developer Tools.

#### Properties

- [API Reference](https://developers.weixin.qq.com/miniprogram/en/dev/api/)
- [Developer Tools (IDE)](https://developers.weixin.qq.com/miniprogram/dev/devtools/devtools.html)
- [TypeScript Typings SDK](https://github.com/wechat-miniprogram/api-typings)

### WeChat Pay APIv3 (Direct-Connect Merchant)

WeChat Pay's third-generation REST API for mainland-China direct-connect merchants. Authenticates with merchant API certificates and platform-key-signed requests over HTTPS/JSON. Covers JSAPI / Native / App / H5 / Mini Program payments, refunds, bill download, merchant transfers, WeChat Pay Score, vouchers, marketing red packets, profit sharing, consumer complaints, and platform certificate rotation. Replaces the legacy XML-based APIv2. Base URL `https://api.mch.weixin.qq.com`.

#### Properties

- [API Reference (EN)](https://pay.weixin.qq.com/wiki/doc/apiv3/en/index.shtml)
- [Merchant Portal Login](https://pay.weixin.qq.com/index.php/core/home/login)
- [Official Java SDK](https://github.com/wechatpay-apiv3/wechatpay-java)
- [Official Go SDK](https://github.com/wechatpay-apiv3/wechatpay-go)
- [Official PHP SDK](https://github.com/wechatpay-apiv3/wechatpay-php)
- [Postman Script](https://github.com/wechatpay-apiv3/wechatpay-postman-script)
- [Certificate Downloader CLI](https://github.com/wechatpay-apiv3/CertificateDownloader)

### WeChat Pay APIv3 (Service Provider / Partner)

WeChat Pay's APIv3 in "service provider" mode, used by payment platforms and ISVs to onboard and operate sub-merchants. Adds combined-order JSAPI/Native/App payments, sub-merchant onboarding ("特约商户进件"), sub-merchant settlement and bill journals, partner-mode refunds, profit sharing across sub-merchants, and consumer-complaint handling on behalf of sub-merchants.

#### Properties

- [API Reference (EN)](https://pay.weixin.qq.com/wiki/doc/apiv3_partner/en/index.shtml)

### WeChat Pay Global v3 API

Cross-border WeChat Pay surface described by Tencent as "a universal version for global institutions and merchants" — for international institutions and merchants accepting payments from WeChat users outside mainland China, with multi-currency settlement, refunds, and reconciliation distinct from the mainland APIv3.

#### Properties

- [Documentation](https://pay.weixin.qq.com/doc/global/v3/en/index.html)
- [Global Portal](https://pay.weixin.qq.com/index.php/public/wechatpay_en)

### WeChat Open Platform — Mobile App Login (OAuth 2.0)

OAuth 2.0 authorization flow exposed by the WeChat Open Platform for native iOS, Android, and HarmonyOS apps. Apps redirect into WeChat for an authorization code, then exchange it via `https://api.weixin.qq.com/sns/oauth2/access_token` for an access token (scope `snsapi_userinfo`), refresh tokens via `/sns/oauth2/refresh_token`, and fetch the profile via `/sns/userinfo`. Access tokens expire in 7200 seconds; refresh tokens last 180 days.

#### Properties

- [Documentation](https://developers.weixin.qq.com/doc/oplatform/Mobile_App/WeChat_Login/Development_Guide.html)
- [Open Platform Portal](https://open.weixin.qq.com/)

### WeChat Open Platform — Website Login (QR OAuth)

Web-based OAuth 2.0 login that renders a WeChat QR code on third-party websites. End users scan in WeChat to authenticate; the site receives a code on its callback URL and exchanges it for a `snsapi_login` access token plus the user's OpenID / UnionID.

#### Properties

- [Documentation](https://developers.weixin.qq.com/doc/oplatform/Website_App/WeChat_Login/Wechat_Login.html)

### WeChat Open Platform — Third-Party Platform API

API surface that lets authorized ISVs operate Official Accounts and Mini Programs on behalf of merchant clients ("代商家调用接口"). Covers merchant authorization onboarding, developing Mini Programs on behalf of merchants (registration, certification, template upload, version management), initiating web authorization on behalf of accounts, handling messages and events, using the JS-SDK on behalf of accounts, cloud development, domain configuration, privacy settings, and merchant-violation notifications.

#### Properties

- [Documentation](https://developers.weixin.qq.com/doc/oplatform/Third-party_Platforms/Authorization_Process_Technical_Description.html)

### WeChat Official Accounts API

HTTPS/JSON APIs for WeChat Official Accounts (Subscription Accounts and Service Accounts) — the publishing surface used by media, brands, and businesses to reach WeChat followers. Surface includes user-info & tagging, message receipt and reply (text, image, voice, video, news), template messages, customer service messages, custom menus, materials and asset management, QR code with scene parameters, web authorization (`snsapi_base` / `snsapi_userinfo`), and the JS-SDK for embedded webpages.

#### Properties

- [Documentation](https://developers.weixin.qq.com/doc/offiaccount/Getting_Started/Overview.html)
- [Admin Portal (mp.weixin.qq.com)](https://mp.weixin.qq.com/)

### WeChat Work (WeCom) API

Server API for Enterprise WeChat / WeCom — Tencent's enterprise collaboration suite. All calls are HTTPS/JSON, UTF-8 encoded, and require an access token. Covers Contacts management (members, departments, tags), messaging & event callbacks, group chat sessions and passive reply, External Contacts (customer management, departing-employee inheritance, customer groups, moments), web OAuth / Web login components / secondary verification, Office Automation (mail, document collaboration, calendar, meetings, cloud drive, livestreaming), enterprise payments (red envelopes, employee payment, external collections / invoicing), conversation-content archive for compliance, school/parent communication, civic / grid services, and the AI & data zone for analytics and knowledge bases. Base URL `https://qyapi.weixin.qq.com`.

#### Properties

- [Documentation](https://developer.work.weixin.qq.com/document/path/90664)
- [Developer Portal](https://developer.work.weixin.qq.com/)
- [Admin Login](https://work.weixin.qq.com/wework_admin/loginpage_wx)
- [Community Python SDK](https://github.com/sbzhu/weworkapi_python)

### WeChat Cloud Hosting API

WeChat Cloud Hosting (微信云托管) is Tencent's cloud-native, ops-free container deployment service tightly integrated into the WeChat ecosystem. Tencent describes it as "a cloud-native, operations-free, highly available service deployment solution that requires no servers and enables deployment in just one minute." Exposes container deployment APIs, serverless MySQL, object storage with CDN and security validation, native token access (no auth layer to call WeChat APIs), the cloud-call service relaying WeChat APIs, message-push routing, WeChat Pay integration without encryption handling, gray deployment and rollback, real-time log search, resource monitoring, custom alerts, and Enterprise WeChat robot notifications. Supports Node.js, Go, Python, and Java containers.

#### Properties

- [Documentation](https://developers.weixin.qq.com/miniprogram/dev/wxcloudrun/src/basic/intro.html)
- [Cloud Hosting Portal](https://cloud.weixin.qq.com/)

### WeChat Channels (Video Accounts) Developer Surface

WeChat Channels (视频号) is WeChat's short-video and livestreaming product. The developer surface — exposed through the Mini Programs platform and Channels merchant tools — covers livestream room creation, livestream-goods linkage, Channels-driven traffic into Mini Programs, and merchant integrations. There is no fully public OpenAPI; most APIs are gated to qualified Channels merchants and partners.

#### Properties

- [Documentation](https://channels.weixin.qq.com/developers)
- [Channels Portal](https://channels.weixin.qq.com/)

### WeChat Shop (微信小店) API

WeChat Shop is the unified merchant storefront tying together Mini Programs, Channels livestreaming, Official Accounts, and WeChat Search. APIs cover product (SPU/SKU) management, order lifecycle, after-sales, logistics, inventory, vouchers, and merchant-side fulfilment hooks for the integrated WeChat commerce graph.

#### Properties

- [Documentation](https://developers.weixin.qq.com/miniprogram/dev/platform-capabilities/industry/mini-shop/)
- [Shop Portal](https://shop.weixin.qq.com/)

## Common Properties

| Type | URL |
|---|---|
| Website | https://www.wechat.com/ |
| Portal | https://weixin.qq.com/ |
| Developer Portal | https://developers.weixin.qq.com/ |
| Documentation | https://developers.weixin.qq.com/doc/ |
| API Reference | https://developers.weixin.qq.com/miniprogram/en/dev/ |
| Getting Started | https://developers.weixin.qq.com/miniprogram/en/dev/framework/quickstart/ |
| Console | https://mp.weixin.qq.com/ |
| WeChat Pay Portal | https://pay.weixin.qq.com/ |
| WeChat Pay Login | https://pay.weixin.qq.com/index.php/core/home/login |
| WeCom Portal | https://work.weixin.qq.com/ |
| WeCom Developer Portal | https://developer.work.weixin.qq.com/ |
| Open Platform Portal | https://open.weixin.qq.com/ |
| Channels Portal | https://channels.weixin.qq.com/ |
| Cloud Hosting Portal | https://cloud.weixin.qq.com/ |
| Shop Portal | https://shop.weixin.qq.com/ |
| GitHub — wechat-miniprogram | https://github.com/wechat-miniprogram |
| GitHub — wechatpay-apiv3 | https://github.com/wechatpay-apiv3 |
| WeUI SDK | https://github.com/Tencent/weui |
| Developer Tools (IDE) | https://developers.weixin.qq.com/miniprogram/dev/devtools/devtools.html |
| Community Support | https://developers.weixin.qq.com/community/ |
| Tencent Support | https://kf.qq.com/ |
| WeChat Service | https://service.weixin.qq.com/ |
| Terms of Service | https://www.weixin.qq.com/agreement?lang=en_US |
| Privacy Policy | https://www.tencent.com/en-us/privacy-policy.html |

## GitHub Organizations & Notable SDKs

- **[github.com/wechat-miniprogram](https://github.com/wechat-miniprogram)** — 74 repos. Highlights: `miniprogram-demo` (JavaScript, 7.2k stars), `weui-miniprogram` (TypeScript, 2.4k), `api-typings` (TypeScript typings, 798), `threejs-miniprogram` (781), `computed` (696), `recycle-view` (637), `glass-easel` multi-backend component framework (307), `minigame-canvas-engine` (300).
- **[github.com/wechatpay-apiv3](https://github.com/wechatpay-apiv3)** — 9 repos. Official WeChat Pay APIv3 SDKs in Java, Go, PHP; Apache HttpClient decorator; Guzzle middleware; Postman script; CertificateDownloader CLI; transferbatch demo.
- **[github.com/Tencent/weui](https://github.com/Tencent/weui)** — 27.4k-star HTML / CSS UI library by the WeChat official design team.

## Notable Findings

- **WeChat Pay APIv3** is now the recommended payment integration path; the legacy XML APIv2 remains live but new integrations should target v3.
- **Three layered surfaces for identity**: native mobile OAuth (`snsapi_userinfo`), website QR OAuth (`snsapi_login`), and the Third-Party Platform API for ISVs operating accounts on behalf of merchants — each with its own access-token lifecycle.
- **WeChat Cloud Hosting** removes a major friction point for Mini Program backends: containers (Node.js, Go, Python, Java) running inside Tencent's WeChat-adjacent infrastructure with native-token access to WeChat APIs (no separate auth layer) and free relay of WeChat server endpoints.
- **English documentation exists** for Mini Programs (`/miniprogram/en/dev/`), WeChat Pay APIv3, and WeChat Pay Global v3 — but Official Accounts, WeCom, Channels, Shop, and Open Platform docs remain Chinese-first.

## Notable Absences

- **No public OpenAPI / Swagger spec** is published for any WeChat surface. All SDKs (including the official `wechatpay-*` libraries) are hand-written against the Chinese reference documentation.
- **No public, machine-readable changelog / RSS feed** for the developer platform — changes are announced through `developers.weixin.qq.com/community/` posts and the in-app Service Notices in `mp.weixin.qq.com`.
- **No global status page** for WeChat / WeChat Pay / WeCom — outage status is communicated via the developer community and per-merchant notices.
- **No public WeChat Pay pricing page** — fees are negotiated per merchant in the merchant agreement, not posted publicly.
- **No Tencent-maintained Python SDK** for WeChat Work / WeCom — the most-used wrapper (`sbzhu/weworkapi_python`) is community-maintained and explicitly disclaims production use.
- **The `github.com/wxopen` organization is empty** (zero public repos) — it is not the canonical home for WeChat Open Platform SDKs despite its suggestive name.

## Maintainers

- Kin Lane — kin@apievangelist.com
- WeChat / Tencent — https://developers.weixin.qq.com/
