# Free LLM API Provider
This is a list of free llm providers and their rate usage limits.</br>
免费llm api平台（包括cn平台）

You may also want to read: 
- [**How to Choose Your LLM?**](https://github.com/CYBIRD-D/How-to-Choose-your-LLM-Model-for-translation/blob/main/README_en.md)

## Global Platform

### Google Gemini
https://ai.google.dev/gemini-api/docs/rate-limits#free-tier   
> Last updated: **2025-10-27 UTC** </BR>
> **RPM**: Requests per minute </BR>
> **TPM**: Tokens per minute</BR>
> **RPD** Requests per day</BR>

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

### Github(limited) </br>
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

### Tencent-Hunyuan 腾讯混元** </br>
(Hunyuan-lite free; 1 M free token for other models/per account) </br>
- 首次开通腾讯混元大模型服务后，混元生文将发放一定量级的免费调用额度（100M tokens）
  - 资源包有效期为1年，自开通服务之日起1年内若免费资源包次数未使用完，则过期作废
https://cloud.tencent.com/document/product/1729/97731

-----------

**Volcengine 火山引擎** （500 point 资源点/day） </br>
Tongyi Qwen free (no point cost; 100 time/day)</br>
https://www.volcengine.com/docs/84458/1585102   
https://www.volcengine.com/docs/84458/1585097

**Spark 讯飞星火** </br>
Spark-lite free </br>
https://www.xfyun.cn/doc/spark/HTTP调用文档.html   
https://xinghuo.xfyun.cn/sparkapi?scr=price
