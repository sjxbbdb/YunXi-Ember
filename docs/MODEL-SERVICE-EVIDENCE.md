# 模型服务公开页证据（2026-11-23 PST）

> 项目是 YunXi-Ember。本文件只记设计整理者在该日用只读方式打开的公开文档，不是购买建议，也不是账号账单。
> 访问日是 2026-11-23 PST。抓取可能来自缓存。页面自己写了日期的，分开记下。没有写发布日期的，不把访问日说成页面更新日。
> 账号、实际模型版本、签约主体和已购权益都还没核实。这些价格不能用来打开运行。

## Agnes

国际概览 [Overview](https://wiki.agnes-ai.com/en/docs/overview) 把国际 Base URL 写成 `https://apihub.agnes-ai.com/v1`，并称接口是 OpenAI 风格。这不是全兼容，本轮也没有实测。该页抓取文本没有发布日期。

国际模型页 [Agnes 3.0 Flash](https://agnes-ai.com/en/docs/agnes-30-flash) 写模型名 `agnes-3.0-flash`，Chat Completions 为 `POST /v1/chat/completions`，响应结构写成 OpenAI 兼容。同页还列了 Responses 和 Messages。上下文 512K，最大输出 65536 token。刊例价：缓存输入 0.005 美元 / 百万 token，普通输入 0.05，输出 0.15。天使用户试用价这三项为 0。页末写可用性和速率以账户与 API key 为准。抓取文本没有发布日期。

国内模型页 [Agnes 3.0 Flash（中文）](https://wiki.agnes-ai.cn/zh-Hans/docs/agnes-30-flash) 的 Base URL 是 `https://api.agnes-ai.cn/v1`，模型名同为 `agnes-3.0-flash`。刊例价是人民币：缓存输入 0.035 元 / 百万 token，输入 0.35，输出 1.00。试用价为 0。这是另一套标价，不是国际美元价，也不是已核实账单。抓取文本没有发布日期。

[Token Plan 与 Agent Plan](https://agnes-ai.com/en/docs/tokenplan) 本轮读到的现行句子是：Existing Token Plan users retain their benefits. Token Plan may reopen for purchase as capacity permits. 因此不能把 Token Plan 写成现在可以新购。

同一页的既有 Token Plan 表写着文本请求额度：Starter 每 5 小时 1500、每周 15000；Plus 每 5 小时 7500、每周 75000；Pro 每 5 小时 30000、每周 300000。折叠规则所在说明的生效日是 2026-10-29。不能把这张表回填成 2026-10-26 已经证实。页上写 Token Plan API keys 是一种密钥类型。本轮没有在这页找到 Starter 每月 4 美元或 Plus 每月 10 美元。不能证明那两个历史价格从未出现，也不能把它们写成现在可买。

同一页的 Agent Plan 月付卡片本轮读到：Lite 2.99 美元 / 20000 Credits，Plus 14.99 美元 / 100000，Pro 29.99 美元 / 240000，Max 75.00 美元 / 600000，均为每月。年付卡片金额不同，不能把月付数字说成唯一售价。Credits 按模型刊例价换成等值后再乘计划折扣，不是每次调用固定扣一次。页上把 6600 Credits 等于 1 美元写成换算基数，不是每种充值包的固定售价。5 小时窗口重置只恢复该窗口的可用额度，不新增 Credits，也不退回已消耗的 Credits。不能把每月 Credits 理解成每 5 小时重发满额。

[Model Pricing](https://www.agnes-ai.com/en/docs/pricing) 写：All prices are API prices；`M` 是一百万 token。`agnes-3.0-flash` 刊例价与上面的国际模型页相同。试用零价只适用于试用；Agent Plan 按刊例价计 Credits，不使用试用零价。账单以账户记录为准。抓取文本没有发布日期。

[Privacy Policy](https://wiki.agnes-ai.com/en/docs/privacy-policy) 页首写 Last Updated: July 9, 2026。所读第 5 节一类条文：免费服务的交互可能用于训练或改进，退出只在提供退出功能时成立；Enterprise 与 Paid Token Plans 默认不把客户内容用于训练，除非明确授权。联系处只写公司名 Agnes AI。这不是已核实的完整法律主体。

[Terms of Service](https://agnes-ai.com/en/docs/terms-of-service) 页首写 Effective Date: April 1, 2026。第 8.2 节仍写：可用客户数据改进模型，包括训练和微调，除非在设置里退出（if available）。退出后仍可为实现服务而处理数据。

两份文件不能收成「不存储、不审查，或付费就无条件不训练」。隐私政策点名的是 Paid Token Plans，本轮没有读到把 Agent Plan 逐字算进该定义的句子。本轮没有把 `app.agnes-ai.com` 的应用隐私政策当作 API 签约主体证据。不同根域属于同一说法，不足以证明签约主体。

## DeepSeek

[Models & Pricing](https://api-docs.deepseek.com/quick_start/pricing/) 写：请求名 `deepseek-flash` 的模型版本栏是 DeepSeek-V4.1-Flash-1017；`deepseek-v4-pro` 的版本栏是 DeepSeek-V4-Pro-0813。旧名 `deepseek-v4-flash` 仍被接受，但由 Flash-1017 提供并按 Flash 价计。版本栏是文档标识，不等于权重被证明固定，也不等于服务返回的名字永远不变。价格按每百万 token，并区分峰谷。低谷是高峰的一半。高峰是周一到周五的 01:00–04:00 与 06:00–10:00 UTC，不含中国公共假日；其余为低谷。

`deepseek-flash` 每百万 token：缓存命中输入低谷 0.003、高峰 0.006 美元；未命中输入低谷 0.15、高峰 0.3；输出低谷 0.6、高峰 1.2。`deepseek-v4-pro`：缓存命中 0.022 / 0.044，未命中 0.66 / 1.32，输出 1.98 / 3.96。抓取文本没有单独的页面发布日期。

同一页写：自北京时间 2026-11-18 12:00（与 2026-11-17 20:00 PST 是同一时刻）起，调用模型时由服务端触发的搜索和网页抓取不再单独计工具费；返回内容并入上下文，按模型 token 计费。独立 Search API 与 Fetch API 仍是每 1000 次成功请求 0.75 美元。

[Search & Fetch](https://api-docs.deepseek.com/guides/search/) 写独立端点 `POST /v1/tools/search` 与 `POST /v1/tools/fetch`。只有 HTTP 200 且有结果才计这一项：搜索要有非空结果，抓取要有页面内容。失败、超时、空搜索不计这项。模型通过服务端工具自己搜索，按该页不另收工具费，只计模型 token。直接调用这两个 API 仍按上面的成功请求价。直接调用是炉子侧的供应商能力，不是主体获准在外站提交表单。本轮不选搜索供应商，也不启用该 POST。

[新闻页 news261017](https://api-docs.deepseek.com/news/news261017/) 曾写每个端点 0.75 美元 / 1000 次，并写服务端工具计费自 2026-10-31 16:00 UTC 开始。抓取文本没有独立发布日期，URL 含 news261017。它不是当前定价页的规则。项目里「11 月 1 日搜索一律开始收费」只保留为当时的说法。后来的公开规则要区分：模型触发的服务端搜索，和独立 search/fetch API，不是同一笔费用。

## 硅基流动

[Qwen/Qwen3-8B](https://www.siliconflow.cn/models/Qwen%2FQwen3-8B) 的请求模型名是 `Qwen/Qwen3-8B`。目录写输入和输出都是免费 / 百万 token，币种人民币。上下文 131072 token。这是目录标价，不是账号速率或可用性保证。抓取文本没有把目录价写成政策更新日期。

[THUDM/GLM-4-9B-0414](https://www.siliconflow.cn/models/THUDM%2FGLM-4-9B-0414) 的请求模型名是 `THUDM/GLM-4-9B-0414`。目录同样写输入和输出免费 / 百万 token。上下文 32768 token。同样只是目录。

[隐私政策](https://docs.siliconflow.cn/docs/legals/privacy-policy) 写 Update Date: July 30, 2026，运营方栏为 Beijing Siliconflow Technology Co., Ltd.。第 1.4 节写：业务输入和输出只在当次推理所需的短时间处理，不长期保存，不用于预训练或微调，推理结束后销毁或使计算节点不可恢复。同节仍收集 IP、模型名、token 消耗、请求时间和状态码等日志。第 1.5 节写收集调用行为，并对输入提示和输出做自动内容审查，审查不用于训练。不能写成完全不留记录，也不能把「不用于训练」写成没有日志和审查。

## 记账维度和准入

40/40/10/10、保底，以及可赚只来自考试上的确定进步，这些项目比例不改。原政策里保底按 5 小时窗口回补、没用完最多结转一个窗口，也保留。供应商的每月 Credits 不是这个窗口的重发满额。映射还没核定，就是阻塞，不能拿去开跑。

旧的每周固定请求次数，只有实际账号被核实为仍有同一权益和同一限制时，才能当作基数。Starter 约 100 秒一跳、Plus 约 20 秒一跳，是当时按假设周额度做的演算，不是当前运行建议。

Credits、token、供应商请求次数、CPU 秒和货币是不同量纲，不能相加，也不能用试用零价支撑永久保底。

每个已批准的供应商和计划先按它自己的限额分开记。要启用某条消费路径，配置里至少要有：价格证据的版本和有效期、实际权益、重置规则、可用模型子集、适用的数据条款、试用或付费标志。只有已经核实、而且量纲相同的预算，才套用原来的四份比例。跨供应商折算，以及自有器官的 CPU 折算，没配置就不启用。

设计可以同时受多条限额约束。未核实的充值或金额不是授权。不自动开出四个供应商预算，也不宣称供应政策已经完成。把周额度改成更一般的多限额方案，只是还需要可执行配置的设计候选，不是原先已经确认的基数政策。

当前实际套餐、金额、价格版本、兑换、周期和账户权限都未定。相关研究运行继续关闭。
