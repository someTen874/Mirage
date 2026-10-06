# Mirage

**不充钱的 AI 角色扮演。** 角色你自己写，数据只存在你手机里。

没有会员、没有积分、没有抽卡。这个 App 本身不收任何费用。

---

## 下载

**① 安卓 App** —— 本仓库里的 `Mirage-v3.98.apk`（Android 8.0+）
传到手机，点击安装；系统会问「允许安装未知来源应用」，同意即可。

**② 电脑服务（Windows 10/11 64 位，40 MB）** —— **从发布页下载**：
<https://mirage-app-pages.app.workbuddy.host/>

> 为什么不在这个仓库里：40 MB 的包超过单文件上传限制，传不上去；
> 而且 GitHub 的直链在国内又慢又常打不开，发布页是**国内直连**的。
>
> 下载后 **整个解压**，再双击里面的 `Mirage电脑服务.exe`。它自带推理引擎，
> 会启动本机的 llama.cpp 并把局域网 IP 显示给你。
> ⚠️ 解压出来的 `bin\` 文件夹必须和 exe 待在同一层，别单独把 exe 挪走。

> 电脑端**不含模型文件**（`.gguf` 有几个 GB，塞不进仓库），要自己下一个 —— 见下面「电脑加速」。

---

## 三种算力，自己选

| 方式 | 花不花钱 | 适合谁 | 代价 |
|---|---|---|---|
| **电脑加速** | 免费不限量 | 有电脑（最好带独显） | 要配一次 llama.cpp，之后开机双击脚本 |
| **云端 API** | 用免费额度 | 没有能跑模型的电脑 | 对话内容会发给你选的模型厂商 |
| **手机本地** | 免费 | 想彻底断网 | 手机只能跑很小的模型，明显更笨、更慢 |

三种可以同时开。**同时开着时优先走电脑**（局域网免费），想走云端就把「电脑加速」关掉。

---

## 电脑加速：两步配一次

1. **下模型文件**
   在 Hugging Face 搜任意 `.gguf` 模型（Qwen 系列中文最好，建议 7B~9B 的 Q4 量化）。
   放进 `C:\MNNChatModels\`（没有就自己建一个）。子文件夹也算，只要 `.gguf` 在这个目录树下面就行。

   > 想自己拿 llama.cpp 跑也行，但**用上面那个 zip 就不必** —— 引擎已经打在里面了。

2. **双击 `Mirage电脑服务.exe`**
   窗口里会列出扫到的模型和本机 IP。
   手机上：连**同一个 WiFi** → 「我的 → 模型与算力」→ 打开「电脑加速」→ 点「自动找电脑」。

> 电脑上那个黑窗口**不要关**，关了服务就停了。

**连不上的话按顺序查三件事：**
1. 电脑上那个窗口还开着吗？
2. 手机用的是 WiFi 还是流量？必须和电脑同一个 WiFi。
3. 电脑第一次跑会弹防火墙提示 —— 必须点「允许访问」。

---

## 这个 App 有什么

- **角色**：名字、性格、说话习惯、和你的关系、她在怕什么……十多个栏目都能写，也能导入别人做的角色卡
- **记忆**：她自己记住的事、你让她记住的事，分开管，还有好感度和剧情进度
- **她会过日子**：有自己的状态、会写日记、手机里有朋友圈和购物记录
- **导出**：角色卡、聊天记录、长图
- **算力自备**：自己的电脑 / 免费的云端 key / 手机本地模型

**没有的东西**（说在前面，免得到处找）：没有内置角色池、没有角色社区、没有账号、没有云同步、没有任何收费点。

---

## 反馈与交流

**QQ 交流群：1092499173**

装不上、连不上电脑、发现 bug、想要新功能 —— 都来群里说，这是唯一的反馈入口。
在 QQ 里搜这个号码 → 申请加群。

---

## 使用条款

- **个人使用完全自由** —— 随便用、随便改、随便接你自己的模型、随便导角色卡，不用问谁。
- **禁止倒卖** —— 不许拿这个 App 或它的安装包去卖钱（包括"代装收费"）。
- **禁止二改后收费并声称原创** —— 改了可以自己用、免费分享，但不能拿去卖，也不能说成是你从头做的。

详细条款见 [LICENSE](LICENSE)。

---

## 说明

- 这个仓库**只放安装包，不放源码**。
- 应用内不使用任何账号体系，不上传任何内容。数据全部存在手机的应用私有目录里，卸载即删。
- 走云端 API 时，对话内容会发送到**你自己填写的那家厂商**；用电脑加速时只在你自己家的局域网里走。

---

## English

**Mirage** is a bring-your-own-compute AI roleplay chat app for Android. No subscription, no credits, no character gacha — the app itself is free.

- `Mirage-v3.98.apk` — the Android app
- **Windows panel** (40 MB, bundled llama.cpp engine) — not in this repo (file-size limit); download it from <https://mirage-app-pages.app.workbuddy.host/>. Unzip first; a `.gguf` model is not bundled.

Compute options: your own PC over LAN (free, unlimited) / a free cloud API key / a small model on the phone itself. Character cards, chat history and memories never leave your device unless you configure a cloud backend.

License: free for personal use; reselling or rebranding-and-charging is not permitted. See [LICENSE](LICENSE).

Feedback and bug reports: QQ group `1092499173` (Chinese QQ messenger).
