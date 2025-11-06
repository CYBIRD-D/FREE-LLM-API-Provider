# Free LLM API Provider
This is a list of free llm providers and their rate usage limits.</br>
免费LLM api平台（包括cn平台）

You may also want to read: 
- [**How to Choose Your LLM?**](https://github.com/CYBIRD-D/How-to-Choose-your-LLM-Model-for-translation/blob/main/README_en.md)

## Global Platform

### Google Gemini
https://ai.google.dev/gemini-api/docs/rate-limits#free-tier   
> Last updated: **2025-10-27 UTC** </br>
> **RPM**: Requests per minute </br>
> **TPM**: Tokens per minute</br>
> **RPD** Requests per day</br>

| Model                     | Requests/minute (RPM) | Tokens/minute (TPM) | Requests/day (RPD) |
|---------------------------|---------------------------|--------------------------|-------------------------|
| Gemini 2.5 Pro            | 2                         | 125,000                  | 50                      |
| Gemini 2.5 Flash          | 10                        | 250,000                  | 250                     |
| Gemini 2.5 Flash Preview  | 10                        | 250,000                  | 250                     |
| Gemini 2.5 Flash-Lite     | 15                        | 250,000                  | 1,000                   |
| Gemini 2.5 Flash-Lite Preview | 15                    | 250,000                  | 1,000                   |
| Gemini 2.0 Flash          | 15                        | 1,000,000                | 200                     |
| Gemini 2.0 Flash-Lite     | 30                        | 1,000,000                | 200                     |

</br>

-------

### Nvidia
https://build.nvidia.com/explore/discover

**Rate limit**: Usually up to **`40`** Requests per minute(RPM)</br>
> Nvidia: Maximum API requests accepted in a given timeframe. </br>
Rate limits may vary by model and traffic from other users may cause throttling. </br>
> For dedicated availability, deploy models as a dedicated endpoint with NVIDIA NIM.

</br>

--------

### OpenRouter</br>
https://openrouter.ai/models?q=free

**Models**: Based on what OpenRouter provide as Free
- **Free usage limits**: If you’re using a free model variant (with an ID ending in `:free`), you can make up to **`20`** requests/minute.</br>
  The following per-day limits apply:
  - If you have purchased less than **`10 credits`**, you’re limited to **`50`** `free` model requests/Day.
  - If you purchase at least **`10 credits`** , your daily limit is increased to **`1000`** `free` model requests/Day.

| Model variant (ID) | Credits purchased        | Rate limit (requests/min) | Daily limit (requests/day) |
|--------------------|--------------------------|---------------------------|----------------------------|
| *:free             | < 10 credits             | 20                        | 50                         |
| *:free             | ≥ 10 credits             | 20                        | 1000                       |


--------

### Ollama </br>
https://ollama.com/cloud

- **Models**：So far Ollama cloud support:
  - deepseek-v3.1: 671b-cloud
  - gpt-oss: 20b-cloud
  - gpt-oss: 120b-cloud
  - kimi-k2: 1t-cloud
  - qwen3-coder: 480b-cloud
  - glm-4.6: cloud
  - minimax-m2: cloud
 
> "Ollama's cloud includes hourly and daily limits to avoid capacity issues. Usage-based pricing will soon be available to consume models in a metered fashion. "</br>
> No exact rate limit number.

</br>

---------

### Cloundflare </br>
https://developers.cloudflare.com/workers-ai/platform/pricing/#llm-model-pricing </br>
- Workers Free	**`10,000 Neurons`** per day </br>
> Last updated: **Oct 27, 2025** </br>
> "Neurons are our way of measuring AI outputs across different models, representing the GPU compute needed to perform your request. Our serverless model allows you to pay only for what you use without having to worry about renting, managing, or scaling GPUs."

| Model | Neurons/1M Input token | Neurons/1M Output token | Input:Output=1:1 </br>（Overall/k token） |
|------|-----------------------|-----------------------|-------------------------------|
| `@cf/meta/llama-3.2-1b-instruct` | 2457  | 18252  | 966  |
| `@cf/meta/llama-3.2-3b-instruct` | 4625  | 30475  | 570  |
| `@cf/meta/llama-3.1-8b-instruct-fp8-fast` | 4119  | 34868  | 513  |
| `@cf/meta/llama-3.2-11b-vision-instruct` | 4410  | 61493  | 303  |
| `@cf/meta/llama-3.1-70b-instruct-fp8-fast` | 26668 | 204805 | 86   |
| `@cf/meta/llama-3.3-70b-instruct-fp8-fast` | 26668 | 204805 | 86   |
| `@cf/deepseek-ai/deepseek-r1-distill-qwen-32b` | 45170 | 443756 | 41   |
| `@cf/mistral/mistral-7b-instruct-v0.1` | 10000 | 17300  | 733  |
| `@cf/mistralai/mistral-small-3.1-24b-instruct` | 31876 | 50488  | 243  |
| `@cf/meta/llama-3.1-8b-instruct` | 25608 | 75147  | 199  |
| `@cf/meta/llama-3.1-8b-instruct-fp8` | 13778 | 26128  | 501  |
| `@cf/meta/llama-3.1-8b-instruct-awq` | 11161 | 24215  | 565  |
| `@cf/meta/llama-3-8b-instruct` | 25608 | 75147  | 199  |
| `@cf/meta/llama-3-8b-instruct-awq` | 11161 | 24215  | 565  |
| `@cf/meta/llama-2-7b-chat-fp16` | 50505 | 606061 | 30   |
| `@cf/meta/llama-guard-3-8b` | 44003 | 2730   | 428  |
| `@cf/meta/llama-4-scout-17b-16e-instruct` | 24545 | 77273  | 196  |
| `@cf/google/gemma-3-12b-it` | 31371 | 50560  | 244  |
| `@cf/qwen/qwq-32b` | 60000 | 90909  | 133  |
| `@cf/qwen/qwen2.5-coder-32b-instruct` | 60000 | 90909  | 133  |
| `@cf/openai/gpt-oss-120b` | 31818 | 68182  | 200  |
| `@cf/openai/gpt-oss-20b` | 18182 | 27273  | 440  |
| `@cf/aisingapore/gemma-sea-lion-v4-27b-it` | 31876 | 50488  | 243  |
| `@cf/ibm-granite/granite-4.0-h-micro` | 1542  | 10158  | 1709 |





---------

### Github </br>
https://docs.github.com/en/github-models/use-github-models/prototyping-with-ai-models#rate-limits

| Tier / Model                                             | Request/Mintute </br> (Copilot Free) | Request/Day </br> (Copilot Free) | Tokens/request </br> (in/out) | Concurrent requests </br> (Copilot Free) |
|----------------------------------------------------------------|--------------------|--------------------|-----------------------------|------------------------------------|
| Low tier models                                                | 15                 | 150                | 8000 in / 4000 out          | 5                                  |
| High tier models                                               | 10                 | 50                 | 8000 in / 4000 out          | 2                                  |
| DeepSeek-R1 / DeepSeek-R1-0528 / MAI-DS-R1                     | 1                  | 8                  | 4000 in / 4000 out          | 1                                  |
| xAI Grok-3                                                     | 1                  | 15                 | 4000 in / 4000 out          | 1                                  |
| xAI Grok-3-Mini                                                | 2                  | 30                 | 4000 in / 8000 out          | 1                                  |

---------

### Mistral </br>
https://docs.mistral.ai/deployment/laplateforme/tier/

- From community&reports; **No offcial list**

| Plan / Tier         | Requests/second (RPS) | Tokens/minute (TPM) | Tokens/month      |
|---------------------|---------------------------|--------------------------|------------------------|
| Mistral API Free    | 1                         | 500k                 | 1 billion     |


----------

### IBM </br>
https://www.ibm.com/products/watsonx-ai/pricing

| Plan / Tier         | Requests/second (RPS) |  Tokens/month      |
|---------------------|---------------------------|------------------------|
| watsonx.ai Free tier </br> (Foundation Models)| 2                         | 300k     |


-----------

### Cohere </br>
https://docs.cohere.com/docs/rate-limits

| Endpoint            | Trial rate limit (requests/min) | Trial monthly cap (calls/month) |
|---------------------|----------------------------------|----------------------------------|
| Chat                | 20                               | 1000                             |
| Generate (legacy)   | 5                                | 1000                             |
| Default (anything not covered above)  | 	500                                | 1000                             |

> All endpoints are limited to 1,000 calls per month with a trial key

--------

### Z.ai (GLM-4.5-Flash) </br>
https://docs.z.ai/guides/overview/pricing

> No offical rate usage limits
-------

### Groq </br>
https://console.groq.com/docs/rate-limits

| Model ID                                   | Request/Minute | Request/Day | Token/Minuite  | Token/Day   |
|-------------------------------------------|-----|-------|------|-------|
| allam-2-7b                                | 30  | 7K    | 6K   | 500K  | 
| groq/compound & groq/compound-mini        | 30  | 250   | 70K  | -     | 
| llama-3.1-8b-instant                      | 30  | 14.4K | 6K   | 500K  |
| llama-3.3-70b-versatile                   | 30  | 1K    | 12K  | 100K  | 
| meta-llama/llama-4-maverick-17b-128e-instruct | 30  | 1K    | 6K   | 500K  | 
| meta-llama/llama-4-scout-17b-16e-instruct | 30  | 1K    | 30K  | 500K  |
| moonshotai/kimi-k2-instruct </br> moonshotai/kimi-k2-instruct-0905  | 60  | 1K    | 10K  | 300K  |
| openai/gpt-oss-20b & gpt-oss-120b        | 30  | 1K    | 8K   | 200K  | 
| qwen/qwen3-32b                           | 60  | 1K    | 6K   | 500K  |


-------

### Celebras </br>
https://inference-docs.cerebras.ai/quickstart

| Model                                | Requests/Minute | Requests/Hour | Requests/Day | Tokens/Minute | Tokens/Hour | Tokens/Day |
|--------------------------------------|-----------------|---------------|--------------|---------------|-------------|------------|
| gpt-oss-120b                         | 30              | 90            | 14.4K        | 60K           | 1M          | 1M         |
| llama3.1-8b                          | 30              | 90            | 14.4K        | 60K           | 1M          | 1M         |
| llama-3.3-70b                        | 30              | 90            | 14.4K        | 60K           | 1M          | 1M         |
| qwen-3-32b                           | 30              | 90            | 14.4K        | 60K           | 1M          | 1M         |
| qwen-3-235b-a22b-instruct-2507       | 30              | 90            | 14.4K        | 60K           | 1M          | 1M         |
| qwen-3-235b-a22b-thinking-2507       | 30              | 90            | 14.4K        | 60K           | 1M          | 1M         |
| qwen-3-coder-480b                    | 10              | 100           | 100          | 150K          | 1M          | 1M         |

---------

### Together AI (certain free-endpoint: search in the model)</br>
- Llama3-70b
https://www.together.ai/models/llama-3-3-70b-free    
https://www.together.ai/models/deepseek-r1-distilled-llama-70b-free  </br>

**NO FREE TIER** Now </br>
https://support.together.ai/articles/1862638756-changes-to-free-tier-and-billing-july-2025

--------

</br>

## CN Platform </br>
### ModelScope(魔搭社区） </br>
https://modelscope.cn/docs/model-service/API-Inference/limits </br>
- 需要须首先绑定阿里云账号。对应云账号需已通过实名认证后，才可正常使用API-Inference
- 每位魔搭注册用户，当前每天允许进行总数为**2000次的API-Inference**调用，其中每**单个模型上限不超过500次**，具体每个模型的限制可能随时动态调整。
- 在每个模型每天不超过500次调用的基础上，平台可能对于部分模型再进行**单独的限制**
  - 例如，deepseek-ai/DeepSeek-R1-0528，deepseek-ai/DeepSeek-V3.2-Exp等**规格较大模型**，当前限制**单模型每天100次调用额度**。其他模型的API调用，也可能会有类似的限制并进行动态调整

-------

### Tencent-Hunyuan 腾讯混元 </br>
(Hunyuan-lite free; 1 M free token for other models/per account) </br>
- 首次开通腾讯混元大模型服务后，混元生文将发放一定量级的免费调用额度（100M tokens）
  - 资源包有效期为1年，自开通服务之日起1年内若免费资源包次数未使用完，则过期作废
- Hunyuan-lite 为免费模型
https://cloud.tencent.com/document/product/1729/97731

-----------

### Volcengine 火山引擎(平台） （500 point 资源点/day） </br>
Tongyi Qwen free (no point cost; 100 time/day)</br>
https://www.volcengine.com/docs/84458/1585102   
https://www.volcengine.com/docs/84458/1585097

- 个人免费版为 **`500资源点/天`**
- 目前（2025.11.03），扣子模型中仅豆包模型、DeepSeek 模型和 Kimi-K2 模型收费。使用 Kimi（8K）等其他扣子提供的模型暂不收取费用，但每日调用次数有一定限制 **`（100次/天）`**

| 模型名称 | 条件</br>（千tokens） | 输入单价</br>(资源点/ktok) | 输出单价</br>(资源点/ktok) | 合计单价</br>(资源点/ktok) | 500资源点可用总tokens (ktok) |
| --- | --- | --- | --- | --- | --- |
| 豆包·1.6·视觉理解·250815（Doubao-Seed-1.6-vision） | [0,32] | 0.8 | 8 | 8.8 | 56.82 |
| 豆包·1.6·视觉理解·250815（Doubao-Seed-1.6-vision） | (32,128] | 1.2 | 16 | 17.2 | 29.07 |
| 豆包·1.6·深度思考 / 豆包·1.6·深度思考·250715（Doubao-Seed-1.6-thinking） | [0,32] | 0.8 | 8 | 8.8 | 56.82 |
| 豆包·1.6·深度思考 / 豆包·1.6·深度思考·250715（Doubao-Seed-1.6-thinking） | (32,128] | 1.2 | 16 | 17.2 | 29.07 |
| 豆包·1.6·自动深度思考（Doubao-Seed-1.6） | [0,32]&[0,0.2] | 0.8 | 2 | 2.8 | 178.57 |
| 豆包·1.6·自动深度思考（Doubao-Seed-1.6） | [0,32]&(0.2,+∞] | 0.8 | 8 | 8.8 | 56.82 |
| 豆包·1.6·自动深度思考（Doubao-Seed-1.6） | (32,128] | 1.2 | 16 | 17.2 | 29.07 |
| 豆包·1.6·极致速度 / 豆包·1.6·极致速度·250828 / 豆包·1.6·极致速度·250715（Doubao-seed-1.6-flash） | [0,32] | 0.15 | 1.5 | 1.65 | 303.03 |
| 豆包·1.6·极致速度 / 豆包·1.6·极致速度·250828 / 豆包·1.6·极致速度·250715（Doubao-seed-1.6-flash） | (32,128] | 0.3 | 3 | 3.3 | 151.52 |
| 豆包·1.5·Pro·视觉深度思考（Doubao-1.5-thinking-vision-pro） | 默认 | 3 | 9 | 12 | 41.67 |
| 豆包·1.5·Pro·视觉理解-250328（Doubao-1.5-vision-pro） | 默认 | 3 | 9 | 12 | 41.67 |
| 豆包·1.5·Pro·视觉理解（Doubao-1.5-vision-pro-32k） | 默认 | 3 | 9 | 12 | 41.67 |
| 豆包·1.5·Pro·深度思考·128K / 豆包·1.5·Pro·视觉推理·128K（Doubao-1.5-thinking-pro） | 默认 | 4 | 16 | 20 | 25.00 |
| 豆包·1.5·Pro·角色扮演 / 豆包·1.5·Pro·角色扮演·250715（Doubao-1.5-pro-32k） | 默认 | 0.8 | 2 | 2.8 | 178.57 |
| 豆包·1.5·Pro·32k（Doubao-1.5-pro-32k） | 默认 | 0.8 | 2 | 2.8 | 178.57 |
| 豆包·1.5·Pro·256k（Doubao-1.5-pro-256k） | 默认 | 5 | 9 | 14 | 35.71 |
| 豆包·1.5·Lite·32k（Doubao-1.5-lite-32k） | 默认 | 0.3 | 0.6 | 0.9 | 555.56 |
| 豆包·GUI·Agent模型（Doubao-1.5-UI-TARS） | 默认 | 3.5 | 12 | 15.5 | 32.26 |
| 豆包·通用模型·Lite（Doubao-lite-32k） | 默认 | 0.3 | 0.6 | 0.9 | 555.56 |
| 豆包·工具调用 / 豆包·角色扮演·Pro（Doubao-pro-32k） | 默认 | 0.8 | 2 | 2.8 | 178.57 |
| DeepSeek-V3.1 | 默认 | 4 | 12 | 16 | 31.25 |
| DeepSeek-V3 / DeepSeek-V3 工具调用 / DeepSeek-V3-0324 | 默认 | 2 | 8 | 10 | 50.00 |
| DeepSeek-R1 / DeepSeek-R1 工具调用 / DeepSeek-R1-250528 | 默认 | 4 | 16 | 20 | 25.00 |
| Kimi-K2 | 默认 | 4 | 16 | 20 | 25.00 |

- 使用豆包 1.6 模型时，输入 token 单价和输出 token 单价均由输入长度决定。例如调用豆包·1.6·自动深度思考模型时，当 1 个请求的输入长度为 200 千tokens，输出长度为 14 千token 时，满足条件输入长度 (128, 256]，将采用计费项 **Doubao-Seed-1.6-256k（输入）**和 Doubao-Seed-1.6-256k（输出）。
- Doubao-Seedance-1.0-lite、Doubao-Seedance-1.0-pro 模型各自为每个扣子账号（主账号+子账号）提供累计 100 万tokens 免费额度。免费额度耗尽后如需继续使用，会从账号中扣减资源点。

-----------

### Spark 讯飞星火 </br>
Spark-lite free </br>
- 首次开通后，免费包（个人）有200k免费额度（所有模型),有效期为一年</br>
https://www.xfyun.cn/doc/spark/HTTP调用文档.html   
https://xinghuo.xfyun.cn/sparkapi?scr=price



