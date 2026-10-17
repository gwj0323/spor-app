# Spor · Privacy Policy / 隐私政策 / Privatlivspolitik

**Spor · Danish Public Transit Companion**  
**Package:** `com.spor.mobile` / Desktop  
**Updated:** October 17, 2026 / 2026 年 10 月 17 日 / 17. oktober 2026  
**Developer:** gwj0323  

---

### Language / 语言 / Sprog
- [🇬🇧 English](#english)
- [🇨🇳 中文](#中文)
- [🇩🇰 Dansk](#dansk)

---

## English

Spor is an independent, open-source app created by an individual developer, not a corporation. I don't want your personal data, I don't track you, and there are zero ads or analytics trackers in the app.

*Note: Spor is an independent project using public timetable APIs from Rejseplanen and is not affiliated with Rejseplanen A/S or DSB.*

Here is a straightforward explanation of what the app uses and why:

### 1. Your Location (GPS)
When you tap "Find nearby", your phone checks its GPS position and asks Rejseplanen for stops close to those coordinates. That is all.
- Your location is never stored on any server.
- The app never tracks you in the background.
- Your position is never shared with me or anyone else.

### 2. Notifications & Reminders
When you turn on departure, transfer, or arrival alerts, your phone manages the alarm locally using the system's built-in notification manager. The optional ongoing trip card in the notification shade also runs completely on your phone. No remote push servers are used.

### 3. Calendar
If you tap "Add to Calendar", Spor adds that specific journey to your personal calendar. The app never reads, inspects, or touches your existing calendar entries.

### 4. Commute Habits (Route Recommendations)
The app adapts the order of suggested routes to how you travel (for example, if you prefer Metro over bus, like longer transfer buffers, or usually travel at certain hours).
- This happens **100% on your device**.
- Nothing is sent over the network or stored in the cloud.
- You can wipe all learned habits at any time under **Settings > Commute Habits > Reset Habits**.

### 5. Network Traffic & API Keys
All network requests are encrypted over HTTPS. If you enter your own Rejseplanen accessId (API Key), it stays on your phone inside the app's sandboxed storage. Error messages automatically hide the key (`accessId=***`) so it is never exposed in logs or on screen.

### 6. No Ads, No Trackers
There are zero advertising libraries (like AdMob) and zero analytics SDKs (like Google Analytics or Firebase) in Spor.

### 7. Deleting Your Data
Everything Spor saves (favorite stations, recent searches, preferences, and commute habits) lives only on your device. You can reset habits or clear favorites directly in the app. If you clear the app's data in system settings or uninstall Spor, everything is permanently removed.

### Questions?
Feel free to open an issue or reach out on GitHub:  
[https://github.com/gwj0323/spor-app/issues](https://github.com/gwj0323/spor-app/issues)

---

## 中文

Spor 是一款由独立开发者开发的轻量开源丹麦公交出行应用。我不需要你的个人数据，应用里没有任何广告，也没有任何追踪或统计组件。

*注：Spor 是使用 Rejseplanen 公开开放接口的独立第三方应用，与 Rejseplanen A/S 或丹麦国铁 (DSB) 无官方隶属关系。*

以下是应用具体使用到的权限与数据说明，没有任何隐瞒：

### 1. 位置信息 (GPS)
只有在你主动点击“查找附近”时，应用才会读取你当前的 GPS 坐标，用于向 Rejseplanen 查询周边的站点列表。
- 坐标绝不会保存在任何服务器上；
- 应用不会在后台偷偷定位或追踪你的轨迹；
- 你的位置不会发送给我，也不会分享给任何第三方。

### 2. 出行提醒与通知
当你为某个车次设置发车、换乘或到站提醒时，所有提醒都在你的手机本地由系统自带的闹钟触发。状态栏里的行程卡片也是在手机本地实时计算的，不依赖任何第三方远程推送服务。

### 3. 日历
只有在你主动点击“添加至日历”时，Spor 才会把选中的这趟车次写进你的系统日历。应用绝不会读取、查看或修改你的其他任何日程。

### 4. 出行习惯（推荐排序）
应用会根据你平时的选择习惯（比如更常坐地铁、喜欢换乘时间更充裕的方案、或者常在某些时段出行），自动把你更可能喜欢的路线排在前面。
- 这项计算 **100% 在你的手机本机完成**；
- 没有任何习惯数据或计算参数会通过网络上传；
- 你随时可以在 **“设置 -> 出行习惯 -> 清空习惯记录”** 里一键清除所有记录。

### 5. 网络请求与 API 密钥
应用内所有网络请求均强制通过 HTTPS 加密传输。如果你在设置中填写了自己的 Rejseplanen API Key (accessId)，它只保存在你手机本地。当网络发生异常时，报错信息会自动抹掉密钥部分（显示为 `accessId=***`），防止密钥意外泄露。

### 6. 无广告、无追踪
Spor 内部没有任何商业广告插件（如 AdMob 等），也没有植入任何埋点统计或用户画像 SDK（如 Google Analytics、Firebase 统计等）。

### 7. 清除与删除数据
Spor 的所有数据（收藏的车站、常用路线、搜索历史、出行习惯）都只存放在你手机本地。你可以在应用内随时清空习惯或删除收藏；在手机系统设置里“清除应用数据”或直接卸载 Spor，所有本地数据就会被彻底删除。

### 疑问与反馈
如有任何疑问或建议，欢迎在 GitHub 提交反馈：  
[https://github.com/gwj0323/spor-app/issues](https://github.com/gwj0323/spor-app/issues)

---

## Dansk

Spor er et uafhængigt open source-projekt lavet af en enkelt udvikler, ikke en stor virksomhed. Jeg ønsker ikke dine personlige oplysninger, jeg sporer dig ikke, og der er hverken reklamer eller analysesoftware i appen.

*Bemærk: Spor er et uafhængigt projekt baseret på åbne køreplan-API'er fra Rejseplanen og er ikke tilknyttet eller drevet af Rejseplanen A/S eller DSB.*

Her er en simpel og gennemskuelig forklaring på, hvad appen bruger, og hvorfor:

### 1. Din placering (GPS)
Når du trykker på "Find i nærheden", tjekker telefonen sine GPS-koordinater for at spørge Rejseplanen om stoppesteder i nærheden. Det er det hele.
- Din placering gemmes aldrig på nogen server.
- Appen sporer dig aldrig i baggrunden.
- Din position deles aldrig med mig eller nogen tredjepart.

### 2. Påmindelser og notifikationer
Når du slår påmindelser til for en afgang, et skift eller en ankomst, håndterer telefonen det 100% lokalt via systemets egne alarmer. Den faste rejsevisning i statuslinjen kører også udelukkende lokalt på telefonen. Der bruges ingen eksterne push-servere.

### 3. Kalender
Hvis du trykker på "Føj til kalender", opretter Spor den valgte rejse i din personlige systemkalender. Appen læser, ændrer eller rører aldrig dine øvrige kalenderaftaler.

### 4. Rejsevaner (Rækkefølge af rejseforslag)
Appen tilpasser rækkefølgen af rejseforslag efter dine vaner (f.eks. hvis du oftere tager Metroen frem for bus, foretrækker god skiftetid eller rejser på faste tidspunkter).
- Alt dette sker **100% lokalt på din telefon**.
- Intet sendes over netværket eller gemmes i skyen.
- Du kan til enhver tid slette alle gemte vaner under **Indstillinger > Rejsevaner > Nulstil vaner**.

### 5. Netværk og API-nøgler
Al netværkstrafik foregår krypteret over HTTPS. Hvis du indtaster din egen Rejseplanen-nøgle (accessId), bliver den udelukkende liggende på din telefon. Ved netværksfejl skjuler appen automatisk nøglen (`accessId=***`), så den ikke vises i fejlbeskeder.

### 6. Ingen reklamer, ingen sporing
Der er nul reklame-frameworks (som AdMob) og nul analyseværktøjer (som Google Analytics eller Firebase) i Spor.

### 7. Sletning af data
Alt hvad Spor gemmer (favoritstationer, seneste søgninger, indstillinger og rejsevaner), findes kun på din egen enhed. Du kan slette vaner og favoritter direkte i appen. Rydder du appens data i telefonens indstillinger eller afinstallerer Spor, slettes alle data permanent.

### Spørgsmål?
Du er altid velkommen til at oprette et issue eller skrive på GitHub:  
[https://github.com/gwj0323/spor-app/issues](https://github.com/gwj0323/spor-app/issues)
