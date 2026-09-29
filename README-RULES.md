# Clash 完整规则包

## 文件
- `Clash-Full.ini`：Subconverter 规则生成配置，含国内直连、AI、常见海外服务、海外数字资产/外汇金融分流。
- `list/AI.list`、`list/AI2.list`：海外 AI 服务规则。
- `list/Coinbase.list`：Coinbase 独立规则组；VPN/Tor 或新 IP 可能触发设备重新确认，组内保留手动出口与直连选择。
- `list/Crypto.list`：海外数字资产交易所、钱包和链上浏览器。
- `list/Payments.list`：PayPal、Wise、Revolut、Stripe、Payoneer 等海外支付/汇款服务，独立使用“海外支付”策略组；默认提供手动选择组，便于固定稳定出口。
- `list/Exness.list`：Exness 官网、个人区/交易终端、帮助和合作伙伴域；整个 `ex-markets.pro` 域（主域和全部子域）独立分流。
- `list/Finance.list`：其他海外外汇/经纪商和投资资讯。
- `list/Check.list`、`list/Proxy.list`：海外检测与其他代理规则。

## 上传前要做
1. 把整个目录结构上传，保持 `Clash-Full.ini` 与 `list/` 同级。
2. 规则链接已指向本仓库 `yyyyymmmmm/clash-rules` 的 `main` 分支。若你复制到其他仓库或服务器，请相应更新 `Clash-Full.ini` 中的规则 URL。
3. 重新生成/订阅配置后再应用。此 `.ini` 是 Subconverter 规则模板，不包含代理节点或订阅凭证。

常见国内服务（微信/视频号、QQ/腾讯、支付宝、淘宝/阿里、抖音、小红书、银行/银联及国内 AI）优先直连；OpenAI/Codex、Gemini、Claude、Copilot 等 AI 规则排在中国域名规则前；海外支付、Coinbase、其他数字资产、Exness、其他外汇金融各有独立策略组，敏感登录组默认优先手动选择。未匹配的中国 IP 直连，未匹配的其他流量走自动代理。

此目录只含规则包，不含仓库中设备配置/备份文件。
