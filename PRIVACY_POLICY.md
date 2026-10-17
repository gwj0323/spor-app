# Privacy Policy / 隐私政策 / Privatlivspolitik

**Application:** Spor (`com.spor.mobile` / Desktop)  
**Effective Date:** October 17, 2026 / 2026 年 10 月 17 日 / 17. oktober 2026  
**Data Controller / Developer:** gwj0323  

---

### Table of Contents / 目录 / Indholdsfortegnelse
- [English (EN)](#privacy-policy-for-spor)
- [中文 (ZH)](#spor-隐私政策)
- [Dansk (DA)](#privatlivspolitik-for-spor)

---

## Privacy Policy for Spor

### 1. Introduction and Scope
This Privacy Policy outlines how the application **Spor** ("the Application", package identifier `com.spor.mobile`, including mobile and desktop clients) handles data. Spor is committed to safeguarding user privacy in accordance with applicable data protection laws, including the General Data Protection Regulation (Regulation (EU) 2016/679, "GDPR").

> [!NOTE]
> **Independent Service Disclaimer:** Spor is an independently developed open-source client application. Spor accesses public transit timetable interfaces provided by Rejseplanen open data. Spor is not affiliated with, endorsed by, sponsored by, or operated by Rejseplanen A/S, DSB (Danske Statsbaner), or any public transit authority.

### 2. Principles of Data Processing
Spor is engineered under the principle of **data minimization** (GDPR Article 5(1)(c)):
- **No User Account Requirement:** The Application does not require user registration, account creation, email verification, or authentication credentials.
- **No Remote User Identification:** The Application does not collect hardware identifiers (such as IMEI, MAC address, or Android Advertising ID) and does not perform user profiling.
- **No Commercial Data Transfer:** No user data is sold, rented, leased, or disclosed to commercial third parties or data brokers.

### 3. Categories of Data Processed and Purposes

#### 3.1 Geolocation Data
- **Permissions:** `ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION`.
- **Purpose and Handling:** Geolocation coordinates (latitude and longitude) are accessed exclusively upon explicit user invocation (e.g., selecting "Find Nearby Stations"). The coordinates are transmitted directly to the Rejseplanen API endpoint over encrypted HTTPS solely to retrieve transit stops in the vicinity.
- **Retention:** Geolocation data is processed ephemerally in volatile memory for the duration of the network request. It is **never retained on remote servers, logged to persistent remote databases, tracked continuously in the background, or linked to user identity**.

#### 3.2 Notifications and Alarms
- **Permissions:** `POST_NOTIFICATIONS`, `SCHEDULE_EXACT_ALARM`.
- **Purpose and Handling:** Used exclusively to schedule local alerts for scheduled trip departures, intermediate transfer times, and arrival notifications, or to display an optional persistent notification card during an active journey.
- **Execution:** All scheduling and dispatching are executed **entirely on-device** using the operating system's local alarm and notification services. No remote push messaging servers are utilized.

#### 3.3 Device Calendar Integration
- **Purpose and Handling:** When the user explicitly initiates the "Add to Calendar" action, the Application formats the chosen itinerary (departure, arrival, transit line, and platform information) and requests the operating system's calendar provider to insert the event.
- **Scope:** Access is strictly write-directed for the specific transit event selected. The Application **does not inspect, read, analyze, export, or modify any existing calendar events**.

#### 3.4 On-Device Commute Preference Learning
- **Purpose and Handling:** The Application includes an on-device personalization engine (`TransitMlEngine`) that adapts the presentation order of journey proposals to accommodate user preferences (such as preferred transport modes, transfer buffer durations, and frequent commute time windows).
- **Processing Architecture:** All mathematical computations and model parameter updates are conducted **strictly on-device**. No habit records, feature vectors, or model parameters are ever transmitted to external servers or cloud infrastructure.
- **Storage and Control:** Preference weights and historical counters are stored solely within the Application’s sandboxed local container (`SharedPreferences`). Users may completely reset all learned preferences and commute history at any time via **Settings > Commute Habits > Reset Habits**.

### 4. Technical and Organizational Security Measures
- **Mandatory Transport Layer Security (TLS):** All outbound communications with public transit API endpoints are strictly enforced over HTTPS (TLS 1.2/1.3). Unencrypted HTTP connections are programmatically prohibited.
- **Secure Local Storage:** Any personal API credentials (such as a user-configured Rejseplanen `accessId`) are maintained strictly within the platform's isolated application sandbox.
- **Credential Masking in Error Logs:** All network exception handlers automatically redact sensitive query parameters (e.g., converting `accessId=...` to `accessId=***`) to prevent unintended credential leakage in diagnostic outputs or interface alerts.

### 5. Third-Party Libraries, Analytics, and Advertising
- **Advertising Frameworks:** Spor contains **no third-party commercial advertising SDKs** (e.g., Google AdMob, Unity Ads, Meta Audience Network).
- **Analytics and Tracking SDKs:** Spor contains **no behavioral tracking, user telemetry, or analytics SDKs** (e.g., Google Analytics, Firebase Analytics, Flurry, AppsFlyer).
- All transit scheduling data is obtained through direct HTTPS requests to public transit open data endpoints.

### 6. Data Retention and Deletion Rights
In compliance with GDPR Articles 15–17:
- **Right to Erasure:** Users retain complete sovereignty over locally stored data. Search histories, saved stations, and commute habits can be cleared on-demand within the Application interface.
- **Complete Deletion:** Clearing application storage via device system settings or uninstalling the Application results in the permanent and irreversible deletion of all local configuration files, preferences, and cached records.

### 7. Children's Privacy
The Application does not knowingly collect, process, or solicit personal data from children under the age of 16. The Application provides public transit timetable information suitable for general audiences.

### 8. Amendments to This Policy
This Privacy Policy may be updated to reflect changes in legal requirements or application functionality. Revisions will be documented with an updated "Effective Date" and published in the repository.

### 9. Contact Information
For inquiries, legal notices, or technical questions concerning this Privacy Policy, please submit an issue through the project repository:  
[https://github.com/gwj0323/spor-app/issues](https://github.com/gwj0323/spor-app/issues)

---

## Spor 隐私政策

### 1. 前言与适用范围
本隐私政策阐明了应用程序 **Spor**（以下简称“本应用”，应用包名 `com.spor.mobile`，涵盖移动端及桌面端）关于数据收集、使用与保护的规范。本应用致力于严格遵循适用的数据保护法律法规，包括《通用数据保护条例》（Regulation (EU) 2016/679，简称“GDPR”）及相关法律要求。

> [!NOTE]
> **独立服务声明：** Spor 是一款由独立开发者开发的开源公共出行助手客户端。本应用基于 Rejseplanen 开放数据平台提供的公开时刻表接口运行，与 Rejseplanen A/S、丹麦国家铁路（DSB，Danske Statsbaner）或任何公共交通运营机构均无任何从属、授权、赞助或官方运营关系。

### 2. 数据处理的基本原则
本应用严格贯彻**数据最小化原则**（GDPR 第 5 条第 1 款 (c) 项）：
- **无需账户体系：** 用户无需注册、登录或提供手机号码、电子邮箱等任何个人身份凭据即可完整使用本应用所有功能。
- **无远程身份识别：** 本应用不收集设备硬件唯一识别码（如 IMEI、MAC 地址、Android 广告标识符等），亦不进行任何跨应用、跨设备的用户画像构建。
- **无商业化数据转让：** 本应用绝不向任何第三方商业机构或数据分析经纪商出售、转让、共享或出租用户数据。

### 3. 处理的数据类型与使用目的

#### 3.1 地理位置信息
- **涉及系统权限：** `ACCESS_FINE_LOCATION`（精确位置）、`ACCESS_COARSE_LOCATION`（大致位置）。
- **处理目的与流程：** 仅当用户主动触发“查找附近车站”等相关交互操作时，本应用方会临时调用设备系统定位服务获取经纬度坐标。该坐标仅通过 HTTPS 加密信道直接向 Rejseplanen 接口发起查询，用于获取临近公共交通站点列表。
- **数据留存：** 位置信息仅在单次网络查询期间在系统瞬时内存中处理，**绝不在任何远程服务器中保存，不记录历史活动轨迹，不进行后台常驻定位，亦不与任何第三方实体共享**。

#### 3.2 通知与定时提醒权限
- **涉及系统权限：** `POST_NOTIFICATIONS`（发送通知）、`SCHEDULE_EXACT_ALARM`（精确闹钟排程）。
- **处理目的与流程：** 仅用于在用户主动设定特定车次的发车预警、换乘提醒、到站下车提醒，或启用实时行程常驻卡片时，在设备本地进行提醒调度。
- **技术实现：** 所有提醒排程均**完全在用户设备本地**由操作系统底层闹钟管理器与通知服务执行，不依赖任何外部云端推送服务器。

#### 3.3 系统日历写入集成
- **处理目的与流程：** 当用户在行程详情中主动点击“添加至日历”时，本应用生成包含车次时刻、起止站与站台备注的日程对象，并调用系统日历服务接口将该日程写入本地日历应用中。
- **权限范围：** 该功能仅为单向写入用户指定行程。本应用**绝不读取、扫描、分析、导出或修改用户日历中现存的其他任何日程或私人记录**。

#### 3.4 端侧出行偏好分析（出行习惯）
- **处理目的与流程：** 本应用集成了端侧计算引擎（`TransitMlEngine`），旨在根据用户历史路线选择偏好（例如公共交通方式倾向、换乘安全裕量偏好及常用出行时间窗口），自动对查询所得的行程候选方案进行本地化排序优化。
- **计算架构：** 所有数学推断与模型更新**严格在用户本地设备处理器内离线运算**，绝无任何偏好特征向量、模型参数或出行统计数据经由网络外传至云端。
- **存储与控制权：** 偏好权重与计数指标仅持久化于设备本地受保护的应用沙盒环境（`SharedPreferences`）中。用户可随时通过 **“设置 -> 出行习惯 -> 清空习惯记录”** 彻底重置并删除所有本地偏好数据。

### 4. 信息安全与技术防护机制
- **强制传输层加密（TLS/HTTPS）：** 本应用与公共交通数据接口之间的所有外部网络通信均强制采用 TLS 加密传输（HTTPS），严禁明文 HTTP 协议连接。
- **凭据沙盒隔离：** 若用户在设置中配置个人 Rejseplanen `accessId`（API 密钥），该密钥严格存储于系统为本应用分配的独立私有沙盒目录内。
- **敏感参数日志脱敏：** 应用内所有网络异常捕获机制均自动对敏感查询参数实施动态脱敏处理（统一转换为 `accessId=***`），杜绝在界面弹窗或本地排错日志中暴露认证凭证。

### 5. 第三方 SDK、分析与广告声明
- **无商业广告组件：** 本应用未集成任何第三方商业广告 SDK（如 Google AdMob、穿山甲、Unity Ads 等）。
- **无行为统计与追踪组件：** 本应用未嵌入任何用户行为分析、遥测或追踪 SDK（如 Google Analytics、Firebase、友盟等）。
- 所有实时时刻表与换乘数据均直接由 Rejseplanen 开放数据官方接口通过加密网络提供。

### 6. 数据存储期限与数据主体权利
依据 GDPR 第 15 至 17 条规定：
- **删除权（被遗忘权）：** 用户对本地存储数据享有完全控制权。搜索历史、收藏路线与出行习惯记录均可在应用界面内随时单项或全量清空。
- **彻底清除机制：** 用户通过操作系统“清除应用数据”或执行卸载操作，将永久、不可逆地删除本应用存储于本地设备上的所有配置、缓存及历史数据。

### 7. 未成年人隐私保护
本应用不以任何形式主动收集或处理未满 16 周岁未成年人的个人数据。本应用提供的公共交通时刻表查询服务面向全体公众，内容适合全年龄段使用。

### 8. 隐私政策的变更与生效
本隐私政策可能随法律法规更新或应用功能迭代进行相应修订。所有修订均将在本页面更新“生效日期”并通过代码仓库公开发布。

### 9. 联系方式与反馈途径
如您对本隐私政策有任何法律疑问、合规咨询或建议，请通过官方开源代码仓库提交 Issue 与开发者取得联系：  
[https://github.com/gwj0323/spor-app/issues](https://github.com/gwj0323/spor-app/issues)

---

## Privatlivspolitik for Spor

### 1. Indledning og anvendelsesområde
Denne privatlivspolitik beskriver, hvordan applikationen **Spor** ("Applikationen", pakkeidentifikator `com.spor.mobile`, herunder mobil- og desktopklienter) behandler data. Spor forpligter sig til at beskytte brugernes privatliv i overensstemmelse med gældende databeskyttelseslovgivning, herunder Europa-Parlamentets og Rådets forordning (EU) 2016/679 ("GDPR").

> [!NOTE]
> **Uafhængighedserklæring:** Spor er en uafhængigt udviklet open source-klientapplikation. Spor benytter offentligt tilgængelige køreplan-API'er leveret af Rejseplanen åbne data. Spor er ikke tilknyttet, godkendt, sponsoreret eller drevet af Rejseplanen A/S, DSB (Danske Statsbaner) eller andre offentlige trafikselskaber.

### 2. Principper for databehandling
Applikationen er udviklet i overensstemmelse med princippet om **dataminimering** (GDPR art. 5, stk. 1, litra c):
- **Intet krav om brugerkonto:** Applikationen kræver ingen brugerregistrering, oprettelse af konto, e-mailbekræftelse eller loginoplysninger for fuld anvendelse af funktionaliteten.
- **Ingen fjernidentifikation:** Applikationen indsamler ikke entydige hardwareidentifikatorer (såsom IMEI, MAC-adresse eller annonce-ID) og foretager ingen profilering.
- **Intet kommercielt videresalg:** Ingen data sælges, udlejes, overdrages eller deles med kommercielle tredjeparter eller datamæglere.

### 3. Behandlede datakategorier og formål

#### 3.1 Lokationsdata (Geolokalisering)
- **Anvendte tilladelser:** `ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION`.
- **Formål og håndtering:** Lokationskoordinater (breddegrad og længdegrad) tilgås udelukkende efter aktiv brugerhandling (f.eks. ved tryk på "Find i nærheden"). Koordinaterne transmitteres direkte til Rejseplanens API-endepunkt via krypteret HTTPS med det ene formål at hente stoppesteder i nærområdet.
- **Opbevaring:** Lokationsdata behandles udelukkende midlertidigt i enhedens arbejdshukommelse under forespørgslen. Data **gemmes aldrig på eksterne servere, logføres ikke, spores ikke kontinuerligt i baggrunden og kobles ikke til en personidentitet**.

#### 3.2 Notifikationer og alarmer
- **Anvendte tilladelser:** `POST_NOTIFICATIONS`, `SCHEDULE_EXACT_ALARM`.
- **Formål og håndtering:** Anvendes udelukkende til at planlægge lokale alarmer for afgange, skift og ankomster, eller til at vise et valgfrit fast rejsekort i statuslinjen under en aktiv rejse.
- **Afvikling:** Al planlægning og afsendelse af påmindelser afvikles **100% lokalt på enheden** via operativsystemets interne alarm- og notifikationstjeneste. Der anvendes ingen eksterne push-servere.

#### 3.3 Integration med enhedens kalender
- **Formål og håndtering:** Når brugeren aktivt vælger "Føj til kalender", formaterer Applikationen den valgte rejse (afgangs- og ankomsttider, linje og sporoplysninger) og anmoder systemets kalendertjeneste om at indsætte begivenheden.
- **Afgrænsning:** Adgangen er strengt skriveorienteret for den specifikt valgte rejse. Applikationen **læser, scanner, analyserer, videresender eller ændrer aldrig eksisterende kalenderaftaler**.

#### 3.4 Maskinlæring på enheden (Rejsevaner)
- **Formål og håndtering:** Applikationen indeholder en lokal maskinlæringsmotor (`TransitMlEngine`), der tilpasser visningsrækkefølgen af rejseforslag efter brugerens præferencer (f.eks. transportmiddelpræferencer, skiftetidsintervaller og faste rejsetidspunkter).
- **Behandlingsarkitektur:** Alle matematiske beregninger og opdateringer af modelvægte foregår **udelukkende lokalt på enhedens processor**. Ingen præferencedata, egenskabsvektorer eller statistikker transmitteres til eksterne servere eller cloudtjenester.
- **Lagring og kontrol:** Vægte og overgangsstatistikker opbevares udelukkende i enhedens sandkasselagring (`SharedPreferences`). Brugeren kan til enhver tid nulstille alle gemte vaner via **Indstillinger > Rejsevaner > Nulstil vaner**.

### 4. Tekniske og organisatoriske sikkerhedsforanstaltninger
- **Obligatorisk kryptering (TLS/HTTPS):** Al ekstern netværkskommunikation med køreplan-API'er er strengt tvunget over krypteret HTTPS (TLS 1.2/1.3). Ukrypteret HTTP-trafik er programmatisk blokeret.
- **Sikker lokal lagring:** Eventuelle brugerdefinerede API-nøgler (såsom en personlig Rejseplanen `accessId`) opbevares udelukkende i applikationens isolerede lokale sandkasse.
- **Sløring i fejlmeddelelser:** Alle netværksfejlhåndteringer slører automatisk følsomme parametre (f.eks. `accessId=***`) for at forhindre utilsigtet eksponering i systemmeddelelser eller logs.

### 5. Tredjeparts-SDK'er, analyse og annoncering
- **Annoncenetværk:** Spor indeholder **ingen tredjeparts kommercielle annonce-SDK'er** (såsom Google AdMob eller Meta Audience Network).
- **Analysesoftware:** Spor indeholder **ingen adfærdssporing, telemetri eller analyse-frameworks** (såsom Google Analytics eller Firebase).
- Alle køreplan- og afgangsdata hentes via direkte HTTPS-kald til Rejseplanens åbne køreplan-API.

### 6. Opbevaring, sletning og rettigheder efter GDPR
I overensstemmelse med GDPR artikel 15-17:
- **Ret til sletning:** Brugeren har fuld kontrol over lokalt gemte data. Søgehistorik, favoritstationer og rejsevaner kan slettes direkte i brugerfladen.
- **Fuldstændig sletning:** Sletning af applikationsdata via enhedens systemindstillinger eller afinstallation af Applikationen sletter permanent og uigenkaldeligt alle lokale konfigurationsfiler, præferencer og data.

### 7. Børns privatliv
Applikationen indsamler eller anmoder ikke bevidst om personoplysninger fra børn under 16 år. Applikationens indhold er velegnet til alle aldersgrupper med behov for køreplanopslag.

### 8. Ændringer af denne privatlivspolitik
Nærværende privatlivspolitik kan løbende opdateres i overensstemmelse med gældende lovgivning eller tekniske ændringer i Applikationen. Ændringer offentliggøres i kildekodearkivet med angivelse af opdateret ikrafttrædelsesdato.

### 9. Kontaktinformation
Ved spørgsmål eller henvendelser vedrørende denne privatlivspolitik kan der oprettes et issue i projektets GitHub-arkiv:  
[https://github.com/gwj0323/spor-app/issues](https://github.com/gwj0323/spor-app/issues)
