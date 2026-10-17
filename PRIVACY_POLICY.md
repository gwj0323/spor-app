# Privacy Policy / 隐私政策 / Privatlivspolitik

**Spor · Danish Public Transit Companion**  
**Package:** `com.spor.mobile` / Desktop  
**Effective Date:** October 17, 2026 / 2026 年 10 月 17 日 / 17. oktober 2026  
**Developer:** gwj0323  

---

### Language / 语言 / Sprog
- [🇬🇧 English](#privacy-policy-for-spor)
- [🇨🇳 中文 (Chinese)](#spor-隐私政策)
- [🇩🇰 Dansk (Danish)](#privatlivspolitik-for-spor)

---

## Privacy Policy for Spor

> [!NOTE]
> **Independent Disclaimer:** Spor is an independent, open-source public transit companion application developed by gwj0323. Spor utilizes publicly accessible open transit timetable endpoints (Rejseplanen open data) and is not affiliated with, endorsed by, sponsored by, or operated by Rejseplanen A/S or DSB (Danske Statsbaner).

### 1. Overview & Core Principles
Your privacy is fundamental to how Spor is built. We follow a strict **privacy-by-design** approach:
- **No account required:** You can use all features without registration, phone number, email, or login credentials.
- **No tracking or profiling:** We do not track your identity, your commute patterns, or your personal habits.
- **No data monetization:** We do not sell, rent, monetize, or broker any personal data.

### 2. Information We Access and How It Is Used
- **Location Data (`ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION`)**:
  - When you explicitly tap the "Find nearby stations" button, Spor queries your device's GPS coordinates to find stations and stops closest to you.
  - Coordinates are transmitted directly to the transit API over HTTPS solely to fetch nearby stations.
  - **Your location is never stored on any remote server, tracked continuously in the background, or shared with any third party.**
- **Notifications & Alarms (`POST_NOTIFICATIONS`, `SCHEDULE_EXACT_ALARM`)**:
  - Used strictly on-device to notify you when you explicitly schedule a trip departure reminder, transfer alert, or arrival notification.
  - The optional persistent trip notification card tracks your active trip locally on your device.
  - All reminders and alarms are scheduled locally via the operating system's alarm manager and notification system.
- **Calendar Integration**:
  - When you explicitly tap "Add to Calendar", Spor creates a calendar entry with the selected trip's timetable and platform notes in your system calendar.
  - Spor **never reads, inspects, transmits, or modifies** any of your other existing calendar events.
- **On-Device Machine Learning (Commute Habits)**:
  - Spor features a 100% on-device learning engine (`TransitMlEngine`) that adapts route sorting and suggestion order to your personal preferences (e.g. favorite transit modes, preferred transfer buffers, frequent commute hours).
  - All mathematical models (LinUCB Contextual Bandit, RankNet neural network, and Markov transition models) run **entirely offline** on your device processor.
  - Model weights, transition counts, and habit records are stored **exclusively in your device's sandboxed local storage** (`SharedPreferences`).
  - **No telemetry, habit data, or model parameters are ever transmitted over the network.**
  - You can reset or clear all habit records and weights at any time with a single tap in **Settings > Commute Habits > Reset Habits**.

### 3. API Communications & Security
- **Mandatory HTTPS:** All network communications with public transit endpoints are strictly enforced over encrypted HTTPS. Cleartext HTTP requests are blocked.
- **Credential Protection:** If you enter a personal Rejseplanen `accessId` (API Key), it is stored exclusively in your device's local sandboxed storage.
- **Error Sanitization:** All network exception handlers and error banners automatically redact sensitive parameters (such as `accessId=***`) to prevent accidental credential leakage in UI dialogs or local logs.

### 4. Third-Party Services & Analytics
- **Zero Advertising SDKs:** Spor does not include any commercial advertising frameworks (such as Google AdMob, Unity Ads, or Meta Audience Network).
- **Zero Analytics Trackers:** Spor does not embed behavioral analytics or telemetry SDKs (such as Google Analytics, Firebase Analytics, Flurry, or AppsFlyer).
- Real-time departure boards and route proposals are retrieved directly from official Rejseplanen public timetable endpoints via HTTPS.

### 5. Data Retention & User Control
- All user data (favorite stations, saved routes, recent searches, UI settings, and on-device habit models) reside strictly inside the sandboxed storage allocated to Spor on your device.
- You have full control over your data:
  - **Clear Commute Habits:** Settings > Commute Habits > Reset Habits.
  - **Clear Search History & Favorites:** Favorites > Clear / Remove.
  - **Complete Deletion:** Clearing app storage in your device system settings or uninstalling Spor permanently and irreversibly erases all local data.

### 6. Children's Privacy
Spor does not collect any personally identifiable information from anyone, including children under the age of 13. The application is suitable for general audiences of all ages seeking public transit schedules.

### 7. Contact
If you have any questions, feedback, or concerns regarding this Privacy Policy, please open an issue on our GitHub repository:  
[https://github.com/gwj0323/spor-app/issues](https://github.com/gwj0323/spor-app/issues)

---

## Spor 隐私政策

> [!NOTE]
> **独立声明：** Spor 是一款由 gwj0323 独立开发的开源丹麦公共出行助手客户端。Spor 基于公开可用的公共交通开放时刻表接口（Rejseplanen open data）提供查询服务，与 Rejseplanen A/S 或丹麦国家铁路（DSB，Danske Statsbaner）无任何隶属、认可、赞助或运营关系。

### 1. 概述与核心隐私理念
保护您的个人隐私是 Spor 设计与开发的核心基石。我们严格遵循**端到端隐私保护（Privacy by Design）**原则：
- **无需注册账户：** 您无需提供手机号、电子邮箱、真实姓名或任何身份凭证即可使用全部功能。
- **绝不追踪用户身份：** 我们不收集设备唯一标识符（IMEI/MAC）、不记录用户画像、不追踪您的出行轨迹。
- **绝不商业化个人数据：** 我们绝不收集、出售、转让或滥用用户的任何个人数据。

### 2. 我们访问的信息及使用方式
- **位置信息（`ACCESS_FINE_LOCATION`、`ACCESS_COARSE_LOCATION`）**：
  - 仅当您主动点击“查找附近车站”或“探测周边”按钮时，Spor 才会调用系统 GPS 接口获取当前地理经纬度。
  - 坐标信息仅通过加密 HTTPS 直接发送给公共交通接口以获取离您最近的车站时刻表。
  - **您的实时位置绝不会保存在任何远程服务器上、绝不在后台持续追踪定位，亦绝不与任何第三方共享。**
- **通知与闹钟权限（`POST_NOTIFICATIONS`、`SCHEDULE_EXACT_ALARM`）**：
  - 仅用于在您主动开启行程发车提醒、换乘提醒、到站下车提醒或常驻通知栏行程卡时，向系统注册本地提醒。
  - 所有定时提醒均通过设备操作系统自带的本地闹钟与通知机制进行管理，不依赖任何第三方远程推送服务。
- **系统日历集成**：
  - 仅当您在行程方案中主动点击“添加至日历”时，Spor 才会调用系统日历提供程序写入所选班次的时刻表与站台备注。
  - Spor **绝不读取、扫描、修改或上传**您个人日历中的其他日程与事项。
- **端侧智能学习与出行习惯（On-Device ML）**：
  - Spor 内置 100% 运行于本地芯片的端侧学习引擎（`TransitMlEngine`），根据您平时的路线选择偏好（如地铁/S-tog/火车倾向、换乘充裕度、常用时段）自动调整推荐顺序。
  - 所有数学算法（LinUCB 上下文强化学习、RankNet 神经网络、马尔可夫出行链）**完全离线计算**。
  - 学习所得的模型权重、转移计数与出行习惯记录**仅存储于手机本地应用沙盒（`SharedPreferences`）中**。
  - **绝无任何习惯数据、模型参数或出行统计通过网络上传。**
  - 您可以随时在 **“设置 -> 出行习惯 -> 清空习惯记录”** 中一键彻底重置所有学习权重与历史。

### 3. 接口通信与安全防护
- **强制 HTTPS 加密：** 应用内与公共时刻表服务的所有网络通信均严格强制采用 HTTPS 加密传输，自动拦截明文 HTTP 请求。
- **密钥安全存储：** 若您在设置中配置了个人的 Rejseplanen `accessId`（API Key），该密钥仅保存在您本机的私有沙盒存储内。
- **异常敏感信息脱敏：** 应用内所有网络异常捕获机制均自动脱敏抹除 URL 中的密钥参数（`accessId=***`），防止网络波动或报错弹窗导致密钥暴露。

### 4. 第三方服务与数据统计
- **零商业广告 SDK：** Spor 绝不集成任何第三方商业广告联盟框架（如 AdMob、穿山甲、Unity Ads 等）。
- **零行为追踪 SDK：** Spor 绝不嵌入用户行为追踪、遥测或埋点分析组件（如 Google Analytics、Firebase、友盟等）。
- 所有实时发车时刻与换乘方案均通过 HTTPS 直接与 Rejseplanen 开放数据服务通信。

### 5. 数据存储期限与用户自主权
- 应用产生的所有数据（收藏站点、常用路线、搜索历史、个性化外观配置及出行习惯模型）均严格保存在设备本地私有目录中。
- 您拥有对个人数据的完全自主权：
  - **清空出行习惯：** 设置 -> 出行习惯 -> 清空习惯记录。
  - **清空历史与收藏：** 收藏与历史 -> 清空 / 删除。
  - **彻底清除：** 在系统设置中清除本应用存储数据或直接卸载 Spor，即可永久、不可逆地删除全部本地数据。

### 6. 儿童隐私保护
Spor 适合全年龄段用户使用，且绝不主动收集 13 周岁以下儿童的任何个人身份信息。

### 7. 联系与反馈
如果您对本隐私政策有任何疑问、意见或改进建议，欢迎通过我们的 GitHub 开源仓库提交 Issue：  
[https://github.com/gwj0323/spor-app/issues](https://github.com/gwj0323/spor-app/issues)

---

## Privatlivspolitik for Spor

> [!NOTE]
> **Uafhængighedserklæring:** Spor er en uafhængig, open source rejseapplikation udviklet af gwj0323. Spor anvender offentligt tilgængelige køreplan-API'er (Rejseplanen åbne data) og er ikke tilknyttet, godkendt, sponsoreret eller drevet af Rejseplanen A/S eller DSB (Danske Statsbaner).

### 1. Oversigt & grundlæggende principper
Dit privatliv er en hjørnesten i udformningen af Spor. Vi følger et princip om **indbygget databeskyttelse (Privacy by Design)**:
- **Ingen brugerkonto:** Du kan bruge alle funktioner uden oprettelse af bruger, telefonnummer, e-mailadresse eller login.
- **Ingen sporing eller profilering:** Vi sporer ikke din identitet, dine bevægelsesmønstre eller dine personlige vaner.
- **Intet videresalg af data:** Vi sælger, udlejer eller deler aldrig dine personoplysninger med tredjeparter.

### 2. Oplysninger vi tilgår og deres anvendelse
- **Placeringsdata (`ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION`)**:
  - Kun når du aktivt trykker på "Find stationer i nærheden", tilgår Spor enhedens GPS-koordinater for at finde de nærmeste stop.
  - Koordinaterne sendes direkte til transit-API'et via HTTPS udelukkende med henblik på at returnere nærliggende stationer.
  - **Din placering gemmes aldrig på eksterne servere, spores aldrig i baggrunden og deles aldrig med tredjeparter.**
- **Notifikationer & alarmer (`POST_NOTIFICATIONS`, `SCHEDULE_EXACT_ALARM`)**:
  - Anvendes udelukkende på enheden til at give dig besked, når du aktivt tilvælger afgangspåmindelse, skiftepåmindelse eller ankomstpåmindelse.
  - Den valgfrie faste rejsevisning i statuslinjen opdateres lokalt på telefonen.
  - Alle påmindelser styres lokalt via enhedens eget alarmsystem og notifikationstjeneste.
- **Kalenderintegration**:
  - Når du aktivt vælger "Føj til kalender", opretter Spor en begivenhed med rejseplan og sporoplysninger i din personlige systemkalender.
  - Spor **læser, analyserer, videresender eller ændrer aldrig** dine eksisterende kalenderaftaler.
- **Maskinlæring på enheden (Rejsevaner)**:
  - Spor indeholder en maskinlæringsmotor (`TransitMlEngine`), der kører 100% lokalt på enheden, og som tilpasser rækkefølgen af rejseforslag efter dine vaner (f.eks. foretrukne transportmidler, skiftetider og rejsetidspunkter).
  - Matematiske modeller (LinUCB Contextual Bandit, RankNet neuralt netværk og Markov-kæder) afvikles **fuldstændigt offline**.
  - Modelvægte, overgangsstatistikker og rejsevaner gemmes **udelukkende i telefonens lokale sandkasselagring** (`SharedPreferences`).
  - **Ingen vanedata, modelparametre eller statistikker sendes nogensinde over netværket.**
  - Du kan til enhver tid nulstille alle gemte vaner med et enkelt tryk under **Indstillinger -> Rejsevaner -> Nulstil vaner**.

### 3. API-kommunikation & sikkerhed
- **Tvungen HTTPS-kryptering:** Al netværkskommunikation med køreplan-API'er foregår udelukkende via krypteret HTTPS. Ukrypterede HTTP-anmodninger blokeres.
- **Sikker opbevaring af API-nøgle:** Hvis du indtaster en personlig Rejseplanen `accessId` (API-nøgle), opbevares den udelukkende lokalt i appens beskyttede sandkasselagring.
- **Automatisk sløring i fejlmeddelelser:** Alle netværksfejlmeddelelser slører automatisk følsomme parametre (`accessId=***`) for at forhindre utilsigtet eksponering i fejlpaneler eller logs.

### 4. Tredjepartstjenester & analyse
- **Nul reklame-SDK'er:** Spor indeholder ingen kommercielle annoncenetværk (såsom Google AdMob eller Meta Audience Network).
- **Nul analysesporing:** Spor indeholder ingen adfærdssporing eller telemetri-frameworks (såsom Google Analytics eller Firebase).
- Køreplaner og afgangstavler hentes direkte fra Rejseplanens officielle åbne API via HTTPS.

### 5. Datalagring & sletning
- Alle brugerdata (favoritstationer, gemte ruter, søgehistorik, app-udseende og rejsevaner) gemmes udelukkende lokalt på din enhed.
- Du har fuld kontrol over dine data:
  - **Nulstil rejsevaner:** Indstillinger -> Rejsevaner -> Nulstil vaner.
  - **Ryd historik og favoritter:** Favoritter -> Ryd / Fjern.
  - **Komplet sletning:** Sletning af appdata i telefonens systemindstillinger eller afinstallation af Spor sletter alle lokale data permanent og uigenkaldeligt.

### 6. Børns privatliv
Spor indsamler ingen personhenførbare oplysninger fra nogen brugere, herunder børn under 13 år. Appen er velegnet til alle aldersgrupper til opslag af offentlig transport.

### 7. Kontakt
Hvis du har spørgsmål eller bemærkninger til denne privatlivspolitik, er du velkommen til at oprette et issue i vores GitHub-repository:  
[https://github.com/gwj0323/spor-app/issues](https://github.com/gwj0323/spor-app/issues)
