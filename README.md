# Tour & Business in China - Netlify 部署指南

## 项目介绍
这是一个为国际游客提供中国地接服务的网站，专注于北京及全国主要城市的旅游和展会支持服务。

## Netlify 部署步骤

1. **准备工作**
   - 确保您已在GitHub上拥有此项目的仓库
   - 注册Netlify账号（https://app.netlify.com/signup）

2. **连接GitHub仓库**
   - 登录Netlify后，点击"New site from Git"
   - 选择"GitHub"并授权Netlify访问您的仓库
   - 搜索并选择此项目的仓库

3. **配置部署设置**
   - 构建命令：`npm install --legacy-peer-deps && npm run build`（已在netlify.toml中配置）
   - 发布目录：`dist`（已在netlify.toml中配置）
   - 环境变量：NODE_ENV=production, NODE_VERSION=20, NPM_CONFIG_PRODUCTION=false（已在netlify.toml中配置）

4. **开始部署**
   - 点击"Deploy site"按钮
   - Netlify将自动克隆您的仓库并开始构建过程
   - 等待部署完成，通常需要1-3分钟

5. **访问您的网站**
   - 部署成功后，Netlify会为您的网站分配一个随机域名（如：your-site-name.netlify.app）
   - 您可以在项目的"Site settings"中自定义域名

## 部署故障排除

### 常见问题

1. **依赖安装失败**
   - 检查是否有package-lock.json文件（本项目使用npm install而不是npm ci，因此不需要lock文件）
   - 确保package.json中的依赖版本正确

2. **构建失败**
   - 检查项目是否能在本地正常构建：`npm run build`
   - 查看Netlify构建日志，找出具体错误信息

3. **页面路由问题**
   - 本项目使用React Router，netlify.toml中已配置重定向规则确保SPA路由正常工作

## 本地开发

1. **安装依赖**
   ```bash
   npm install
   ```

2. **启动开发服务器**
   ```bash
   npm run dev
   ```

3. **构建项目**
   ```bash
   npm run build
   ```

4. **预览生产构建**
   ```bash
   npm run preview
   ```