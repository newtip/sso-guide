# SSO 项目指导 Agent

> 帮助 PM 和 AE 高效完成 SSO 单点登录项目实施的智能指导工具

## 🎯 功能特性

- **PM 模式**：需求调研指导、12 问清单、需求质量检查、风险提示
- **AE 模式**：场景识别、配置方案、二开评估、服务编排配置、联调检查
- **问题排查模式**：5 大高频问题逐步排查指南

## 🚀 部署到 Vercel

### 方法 1：通过 Vercel 官网（推荐）

1. 访问 https://vercel.com
2. 注册/登录账号（支持 GitHub/GitLab/Bitbucket 登录）
3. 点击 **"Add New Project"**
4. 选择 **"Deploy a prebuilt site"**
5. 上传项目文件（或直接拖拽 `sso-guide` 文件夹）
6. 等待部署完成（约 30 秒）
7. 获得访问链接：`https://sso-guide-xxx.vercel.app`

### 方法 2：通过 Vercel CLI

```bash
# 1. 安装 Vercel CLI
npm i -g vercel

# 2. 登录 Vercel
vercel login

# 3. 进入项目目录
cd /root/.openclaw/workspace/sso-guide

# 4. 部署
vercel

# 5. 生产环境部署
vercel --prod
```

## 📁 项目文件

```
sso-guide/
├── index.html      # 主页面（交互式对话框）
├── vercel.json     # Vercel 配置文件
└── README.md       # 说明文档
```

## 💡 使用指南

### PM 使用流程

1. 选择 **"我是 PM"** 模式
2. 查看 **12 问清单**，发给客户填写
3. 收集完成后，使用 **需求质量检查** 确认
4. 参考 **风险提示** 提前规避问题
5. 使用 **需求文档模板** 整理正式文档

### AE 使用流程

1. 选择 **"我是 AE"** 模式
2. 根据项目情况选择 **对接场景**
3. 查看推荐的 **实现方案**（配置优先）
4. 参考 **服务编排配置** 示例进行配置
5. 联调时使用 **联调检查清单** 逐项确认

### 问题排查流程

1. 选择 **"问题排查"** 模式
2. 选择对应的问题类型
3. 按照步骤逐步排查
4. 如无法解决，联系技术部 SSO 项目组

## 📊 高频问题 TOP5

| 问题 | 快速定位 |
|------|---------|
| 跳转到登录页 | 检查 Token 是否传递、SSO 配置是否开启 |
| 数据库没有用户 | 清理 t_sdata_user_mapping 表后重试 |
| Token 验证失败 | 查看 sdata-run.log，检查网络连通性 |
| 版本不支持 | F12 检查 licenseMode，EOB 需升级 |
| 跨域问题 | 联系运维配置同源或使用 postMessage |

## 📞 技术支持

- **飞书文档**：https://feishu.cn/docx/SXzGdMJV7o93J6xwhakcFdT7nzc
- **联系组**：技术部 SSO 项目组
- **版本**：v1.0.0

## 📝 更新日志

### v1.0.0 (2026-03-06)
- ✨ 初始版本发布
- 🎯 PM/AE/问题排查 三种模式
- 📋 完整的 SSO 设计指南
- 🔍 5 大高频问题排查流程

---

**部署完成后，将 Vercel 提供的链接分享给团队即可使用！**
