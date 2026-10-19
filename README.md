# 深鲸 Mobile · 鸿蒙原生版（HarmonyOS NEXT）

**手机上的 DeepSeek Harness —— 鸿蒙原生版。** 与桌面端共用同一套会话、模型与权限；局域网扫码即连，外出走自建中继。

> ⏳ **状态：备案中 / 应用市场审核中。** 当前不提供公开下载；上架后会在本仓库、[官网鸿蒙专区](https://deepwhale.org.cn/harmony.html) 与 Releases 更新。
> HarmonyOS 4.x 及以下可先安装 Android APK：[下载](https://deepwhale.org.cn/dl/mobile-apk)。

## 功能（与 Android 版同源）

- 会话与聊天：列表 / 搜索 / 历史消息 / Markdown / 图片查看 / 新建会话
- 图片附件：拍照 / 相册 / 文件；图片压缩后上传；模型不支持读图时先拦下提示
- 模型与强度：切换模型、调推理强度
- 权限预设：仅可查看 / 工作区内修改 / 完全权限 / 自动审查（EXP）
- 停止与排队：运行中可停止；再发进入"排队中"，支持插话 / 编辑 / 删除
- 轨迹：按轮查看思考与工具调用
- 定时任务：查看全部任务与下次触发时间
- 多端同时：Android + HarmonyOS 可同时在线；审批任意一台点一次即生效

## 使用（三步，与 Android 一致）

1. 桌面端「手机连接」→「开启手机访问」（显示二维码 + 6 位配对码）；
2. 手机打开深鲸 → 扫码，或填地址 + 配对码；
3. 进入会话列表即成功；之后重开 App 自动进入（令牌已在本地保存）。

> 不需要公网 IP、不用自己配 nginx/frp：桌面端内置网关与自建中继，局域网直连、外出走中继。

## 技术说明

- 鸿蒙壳：ArkTS + ArkWeb，加载与 Android 版共享的 `/mobile/` Web UI；
- 壳层适配：`onShowFileSelector`（拍照 / 相册 / 文件）、外链交给系统浏览器、系统返回键交给页面（聊天→列表、列表→后台）；
- 安全：配对码一次性 5 分钟有效，配对后换长期令牌；中继只转发字节、不懂内容；会话与文件留在你自己的电脑上。

## 相关

- Android 版（已发布）：https://github.com/feely0208/deepwhale-mobile
- 完整功能说明：https://deepwhale.org.cn/mobile.html
- 使用指南：https://deepwhale.org.cn/mobile-guide.html
- 桌面端：https://github.com/feely0208/deepwhale-desktop

## License

MIT © 温州深鲸智能科技有限公司
