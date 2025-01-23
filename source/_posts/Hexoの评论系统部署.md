---
title: Hexoの评论系统部署
date: 2024-12-11 16:13:14
categories:
- Platform
- Hexoの评论系统部署
tags:
---

# 前提条件
- **Waline官方文档**
- **LeanCloud账号**
- **Versel服务端**
- **域名绑定** （非必须）

# LeanCloud注册
 1. [登录](https://console.leancloud.app/login) 或 [注册](https://console.leancloud.app/register) LeanCloud 国际版
 2. 点击左上角 [创建应用](https://console.leancloud.app/apps)
	- App name（必填）
	- 选择免费 **Developer** 开发板  

![创建应用](images/leancloud_create_app.png)<br>
 3. 选择刚创建的应用  

![选择应用](images/select_leancloud_app.png)<br>

 4. 点击 **Settings** 然后 **App Keys**，记录 AppID | AppKey | MasterKey，后面会用到

![选择应用](images/app_clientid_key.png)<br>

# Vercel服务端部署  

<div style="text-align: center;">
  <a href="https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fwalinejs%2Fwaline%2Ftree%2Fmain%2Fexample" target="_blank" style="display: inline-block; padding: 2px 21px; background-color: #000000; color: white; text-decoration: none; border-radius: 8px; font-weight: bold;">
    Deploy
  </a>
  <div style="margin-top: 0px; font-size: 12px; color: #808080;">
    Vercel
  </div>
</div>

 1. 点击**上方按钮**，跳转到 Vercel 进行 Server端部署  

 2. 登录 **GitHub**

![登录GitHub](images/vercel_connect.jpg)<br>

 3. 点击 **Authorize Vercel**  

![搜全Vercel访问GitHub](images/github_authorize_vercel.jpg)<br>

 4. 在 **Git Scope** 选择 **GitHub Account**  

![添加GitHub账号](images/add_github_account.jpg)<br>

 5. **安装 Vercel** 到 **全部** / **指定** 的 Repositories  

![安装Vercel到GitHub Repo](images/install_vercel2github.jpg)<br>

 6. 确保 **Git Scope** 出现你的 **GitHub账户名**，
    然后在 **Private Repository Name** 创建新的repo
    点击 **Create**  

![创建Vercel Repo](images/repos_name.jpg)<br>

 7. 耐心地等待部署  

![开始部署Vercel](images/vercel_deployment.jpg)<br>

8. 成功部署后，将会看到 **Congratulations!** 然后点击 **Continue to Dashboard**

![成功部署](images/vercel_successful.jpg)<br>  

9. 你将看到 **Vercel** 的主页面  

![Vercel主页](images/vercel_main.jpg)<br>

10. 点击 **Settings**
您需要在图中的3号创建三个新的环境变量： **LEAN_ID** 、 **LEAN_KEY** 和 **LEAN_MASTER_KEY**。
每个变量的值对应于从 **LeanCloud** 保存的凭据：
**`APP ID`** 对应于 **`LEAN_ID`** 变量的值，
**`APP Key`** 对应于 **`LEAN_KEY`** 变量的值，
**`Master Key`** 对应于 **`LEAN_MASTER_KEY`** 变量的值。  

![Vercel设置](images/vercel_settings_1.jpg)<br>

11. 一旦环境变量配置完成，您需要重新部署您的应用程序。点击项目顶部的 **`Deployments`** 标签，在列表顶部找到最新的部署记录，然后在右侧的下拉菜单中选择 **`Redeploy`** 。  

![vercel重部署](images/vercel_redeploy.png)<br>

12. 如果一切正常，Vercel 会将您重定向到概览页面以开始重新部署。等待 STATUS 状态更改为 Ready。现在，您可以点击 Visit 访问该网站。此链接就是您的服务器地址。

![重部署完毕](images/vercel_redeploy.png)<br>

