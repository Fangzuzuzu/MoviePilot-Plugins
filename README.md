# MoviePilot-Plugins

MoviePilot 个人插件库，提供 PT 站点签到相关功能扩展。

## 插件列表

### 影巢签到修复 (HdhivesignPlus)

修改自 [madrays/hdhivesign](https://github.com/madrays/MoviePilot-Plugins/tree/main/plugins/hdhivesign)，修复原版自动登录失败问题并增加新功能。

**v1.6.0 更新内容：**
- ✅ 适配影巢 Next.js Server Action 登录机制，修复自动登录失败
- ✅ 修复 `verify=False` 与 cloudscraper 不兼容导致的 SSL 异常
- ✅ 修复类名与 package.json key 不一致导致插件无法安装
- ✅ 改进签到结果判断：HTTP 400 重复签到不再误判为失败
- ✅ 增加详细签到响应日志，方便排查问题

**功能特性：**
- 🔐 自动登录获取 Cookie（支持 Next.js Server Action / Playwright 兜底）
- 📅 每日自动签到，支持 cron 定时
- 🎰 支持「每日签到」和「赌狗签到」两种模式
- 🔄 签到失败自动重试
- 📊 签到历史记录和用户信息展示
- 📢 签到结果通知推送

**使用说明：**
1. 在 MoviePilot 插件市场添加本仓库地址：`https://github.com/Fangzuzuzu/MoviePilot-Plugins`
2. 安装「影巢签到修复」插件
3. 配置用户名和密码（插件会自动登录获取 Cookie）
4. 或者手动填入 Cookie（从浏览器 F12 获取 `token` 和 `csrf_access_token`）
5. 设置签到时间（默认 `0 8 * * *` 即每天早上8点）
6. 启用插件并保存

---

### NodeSeek 论坛签到 (nodeseeksign)

来自 [madrays](https://github.com/madrays/MoviePilot-Plugins)，NodeSeek 论坛每日自动签到。

**功能特性：**
- 📅 自动完成 NodeSeek 论坛每日签到
- 🎲 支持选择随机奖励或固定奖励
- 🔄 自动失败重试机制
- 📊 签到状态显示和历史记录
- 🛡️ 支持绕过 CloudFlare 防护
- 🌐 支持代理配置

**使用说明：**
1. 登录 NodeSeek 论坛后获取 Cookie
2. 在插件设置中填入 Cookie
3. 选择签到奖励类型（随机/固定）
4. 设置签到时间
5. 启用插件并保存

## 安装说明

在 MoviePilot 的插件市场页面，添加第三方仓库地址：

```
https://github.com/Fangzuzuzu/MoviePilot-Plugins
```

添加成功后，在插件列表中找到需要的插件安装即可。

## 许可证

本项目采用 MIT 许可证 - 详见 [LICENSE](LICENSE) 文件