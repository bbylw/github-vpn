### 使用 GitHub 项目将代码部署到 Cloudflare Worker，并添加 UUID 变量生成 VPN 点阅连接

本文将引导您通过 GitHub 项目 [worker-vpn](https://github.com/bbylw/github-vpn/blob/main/worker) 将代码部署到 Cloudflare Worker，并添加 UUID 变量来生成 VPN 点阅连接。

#### 1\. 注册和设置 Cloudflare 账户

1.1 如果您还没有 Cloudflare 账户，请访问 Cloudflare 注册页面 创建一个账户。

1.2 登录到 Cloudflare 后，在仪表板中点击“Workers”选项卡。

1.3 如果这是您第一次使用 Cloudflare Workers，您可能需要设置一个 Workers 子域。按照提示完成设置。

#### 2\. 创建一个新的 Cloudflare Worker

2.1 在 Cloudflare Workers 仪表板中，点击“Create a Service”。

2.2 输入服务名称，例如 `vpn-worker-service`，并选择“HTTP handler”作为模板，点击“Create service”。

2.3 创建完成后，您将进入 Worker 的编辑页面。

#### 3\. 从 GitHub 复制代码到 Cloudflare Worker

3.1 在您的浏览器中打开 [worker-vpn 项目](https://github.com/bbylw/github-vpn)。

3.2 打开 [worker](https://github.com/bbylw/github-vpn/blob/main/worker) 文件，并复制其中的所有代码。

3.3 回到 Cloudflare Worker 的编辑页面，将默认代码替换为从 GitHub 复制的代码。

#### 4\. 添加 UUID 变量

4.1 在 Cloudflare Worker 的编辑页面中，添加UUID 变量。

**5\. 部署并测试 Cloudflare Worker**

5.1 点击页面右上角的“Save and Deploy”按钮，将您的 Worker 部署到 Cloudflare。

5.2 部署完成后，点击“Quick Edit”中的“Preview”按钮，测试生成的 VPN 点阅连接是否正常。

5.3 如果一切正常，您将能够通过包含 UUID 的链接访问您的 VPN 服务。

#### 6\. 完成

您的 Cloudflare Worker 现已成功部署并包含了一个自定义 UUID 变量。您可以使用生成的链接访问 VPN 服务。
