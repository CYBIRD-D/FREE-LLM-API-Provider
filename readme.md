# Free LLM API Provider
> Last reviewed: **2026-10-30** 

This directory tracks **free LLM inference APIs**, their account requirements and rate limits (including CN providers).   
**Free inference**, **one-time trial credits** and **$0/month subscriptions with paid token usage** are not the same thing. Free quotas and model catalogs can change.

免费 LLM API 平台汇总（包括中国大陆平台）。**免费调用、一次性试用额度和按量付费（免月费）应分别判断**。

> **Review status (2026-10-30)**
> Google, NVIDIA, Ollama, Groq, OpenRouter, Cloudflare, Cohere, Z.ai, Mistral, SambaNova, Aion Labs and Tencent Hunyuan were checked against provider documentation. Other provider sections may remain dated snapshots. The embedded price list is synchronized to the standalone pricing tracker dated **2026-10-30**; this repository does not independently live-verify its prices.

<table align="center">
  <tr>
    <td align="center"><img src="./logo/gemini-color.png" alt="Google" height="50" /></td>
    <td align="center"><img src="./logo/nvidia-logo-vert-blk.png" alt="NVIDIA NIM" height="50" /></td>
    <td align="center"><img src="./logo/ollama.png" alt="Ollama" height="50" /></td>
    <td align="center"><img src="./logo/groq.png" alt="Groq" height="50" /></td>
    <td align="center"><img src="./logo/cerebras-color.png" alt="Cerebras" height="50" /></td>
    <td align="center"><img src="./logo/openrouter.png" alt="OpenRouter" height="50" /></td>
  </tr>
  <tr>
    <td align="center"><img src="./logo/cloudflarecolor.png" alt="Cloudflare" height="50" /></td>
    <td align="center"><img src="./logo/zai.webp" alt="Z.ai" height="50" /></td>
    <td align="center"><img src="./logo/github.png" alt="GitHub" height="50" /></td>
    <td align="center"><img src="./logo/mistral-color.png" alt="Mistral" height="50" /></td>
    <td align="center"><img src="./logo/modelscope-color.png" alt="ModelScope" height="50" /></td>
    <td align="center"><img src="./logo/volcengine-color.png" alt="Volcengine" height="50" /></td>
    </td>
  </tr>
</table>


You may also want to read my other posts: 
- [**How to Choose Your LLM For Translation?**](https://github.com/CYBIRD-D/How-to-Choose-your-LLM-Model-for-translation/tree/main)
- [**Local LLMs Collection For Translation**](https://github.com/CYBIRD-D/Local-LLMs-Collection-For-Translation/tree/main)
- [**LLM Timeline**](https://github.com/CYBIRD-D/AI-Model-LLM-Timeline)
- [**LLM API Official Pricing Tracker**](https://github.com/CYBIRD-D/LLM-API-Official-Pricing-Tracker)
---------

**Easy guide** to deploy online LLM api（luna）:
  - Sign up/register in certain platform;
  - Get **this** platform's **Api Key** and **Endpoint Address**
    - Check if there's an available date for the key
  - Put it in the softwares that support it.

## Content/目录
- [Global Platform](#global-platform)
  - [★Google/Gemini & Gemma 4](#google-gemini-googlegemma-4)
  - [★Nvidia(40RPM)](#nvidia)
  - [Ollama](#ollama)
  - [★Groq](#groq)
  - [~~Cerebras~~](#cerebras)
  - [OpenRouter](#openrouter)
  - [Cloudflare](#cloudflare)
  - [Cohere](#cohere)
  - [★Z.ai (GLM-4.5/4.7-Flash)](#zai-glm-4547-flash)
  - [~~GitHub Models~~](#github)
  - [★Mistral](#mistral)
  - [SambaNova](#sambanova)
  - [AionLabs](#aionlabs)
  - [SKT](#skt)
  - [IBM](#ibm)
  - [Scaleway (1M free token/per account)](#scaleway-1m-free-tokenper-account-no-refresh)
- [中国大陆平台](#cn-platform)
  - [魔搭社区（ModelScope）](#魔搭社区modelscope)
  - [硅基流动（SiliconFlow）](#硅基流动siliconflow)
  - [腾讯云 TokenHub](#腾讯云-tokenhub)
  - [火山方舟（Volcengine Ark）](#火山方舟volcengine-ark)
  - [扣子（Coze）](#扣子coze)
  - [快手万擎（StreamLake Vanchin）](#快手万擎streamlake-vanchin)
  - [讯飞星火（iFLYTEK Spark）](#讯飞星火iflytek-spark)
  - [心流（iFlow，已停止服务）](#心流iflow已停止服务)
- [LLM PRICE LIST](#llm-price-list)

-----------

## Global Platform

### Google Gemini / Gemma 4
> Last checked: **2026-10-30**

- [Free-tier model pricing](https://ai.google.dev/gemini-api/docs/pricing) · [Rate limits](https://ai.google.dev/gemini-api/docs/rate-limits) · [Your project's limits in AI Studio](https://aistudio.google.com/rate-limit)
- Endpoint: `https://generativelanguage.googleapis.com`
- **Free-tier examples confirmed on Google's pricing page:** `gemini-3.8-flash`, `gemini-3.5-flash-lite` and **Gemma 4**. Check the Free Tier column for other models.
- **Not free-tier eligible:** `gemini-4-argon`, `gemini-3.1-pro-preview` (other Pro models require individual checks).
- Google does **not** publish a single guaranteed RPM / TPM / RPD quota that applies to every free project. Limits depend on model, project and account tier and are shown in AI Studio. Previously observed numbers (e.g. 5 RPM/20 RPD) are **not universal guarantees**.
- Limits apply **per project** (not per key); RPD quotas reset at **midnight Pacific time**. Free-tier prompts may be used to improve Google products.
- **Alternative, unofficial:** [AI Studio to API Adapter](https://github.com/iBUHub/AIStudioToAPI/blob/main/README_EN.md). Review its security and terms before use.

| Model                     | Requests/minute (RPM) | Tokens/minute (TPM) | Requests/day (RPD) |
|---------------------------|---------------------------|--------------------------|-----------------|
| Gemini 2.5~3.8   Flash    | 5             | 250k                     | 20              |
| Gemini 2.5 Flash Lite     | 10                        | 250k                     | 20              |
| Gemini 3.1/3.5 Flash Lite     | 15                        | 250k                     | 500             |
| **Gemma 4 26B/31B**           | **30**                        | **16k**             | **14.4K**            |
| ~~Gemma 3 (1B/2B/4B/12B/27B)~~  | ~~30~~                  | ~~15k~~                      | ~~14.4k~~           |
~~gemini 2 Flash/Lite~~
~~gemini 2.5/3.1 Pro~~


-------

### Nvidia
> Last checked: **2026-10-30** </br>

https://build.nvidia.com/models </br>
Endpoint (OpenAI-compatible): https://integrate.api.nvidia.com/v1

**Rate limit**: Usually up to **`40`** Requests per minute(RPM)</br>
> Nvidia: Maximum API requests accepted in a given timeframe. </br>
Rate limits may vary by model and traffic from other users may cause throttling. </br>
> For dedicated availability, deploy models as a dedicated endpoint with NVIDIA NIM.

- **Representative catalog below, not a fixed or exhaustive 55-model list.** Verify the **Free Endpoint** label for each model in the [live NVIDIA catalog](https://build.nvidia.com/models).
  - OpenAI/Google/Meta/Microsoft/NVIDIA/Mistral AI/DeepSeek/Moonshot AI/Z.ai/MiniMax etc.
- Free endpoints are for **trial/evaluation**, not guaranteed dedicated production hosting. Check NVIDIA trial privacy terms before submitting sensitive data.
<details>

<summary> 
  
  ## Model List 
</summary>

#### DeepSeek
deepseek-ai/deepseek-v4-flash  
deepseek-ai/deepseek-v4-flash-0731  
deepseek-ai/deepseek-v4-pro  
deepseek-ai/deepseek-v4.1-flash  

#### Google
google/codegemma-7b  
google/gemma-7b  

#### Meta
meta/llama2-70b  
meta/llama-3.1-8b-instruct  
meta/llama-3.1-70b-instruct  
meta/llama-3.2-1b-instruct  
meta/llama-3.2-3b-instruct  
meta/llama-3.3-70b-instruct  
meta/muse-glimmer-30b  

#### Microsoft
microsoft/phi-4-mini-instruct  
microsoft/phi-4-mini-flash-reasoning  

#### MiniMax
minimaxai/minimax-m2.5  
minimaxai/minimax-m2.7  
minimaxai/minimax-m3.1-flash  

#### Mistral
mistralai/mistral-nemotron  
mistralai/mixtral-8x7b-instruct  
mistralai/mixtral-8x22b-instruct  
mistralai/mistral-large-4-1t-a52b  

#### Moonshot / Kimi
moonshotai/kimi-k2-instruct  
moonshotai/kimi-k2-thinking  
moonshotai/kimi-k3  

#### NVIDIA
nvidia/gliner-pii  
nvidia/llama-3.1-nemoguard-8b-content-safety  
nvidia/llama-3.1-nemoguard-8b-topic-control  
nvidia/llama-3.1-nemotron-safety-guard-8b-v3  
nvidia/llama-3.3-nemotron-super-49b-v1  
nvidia/llama-3.3-nemotron-super-49b-v1.5  
nvidia/llama-3.1-nemotron-ultra-253b-v1  
nvidia/nemotron-3-ultra-550b-a55b  
nvidia/nemotron-3.5-lightning-30b-a3b  
nvidia/nemotron-3.5-super-vl-120b-a12b  
nvidia/nemoguard-jailbreak-detect  
nvidia/nemotron-3-nano-30b-a3b  
nvidia/nemotron-3-super-120b-a12b  
nvidia/nemotron-content-safety-reasoning-4b  
nvidia/nvidia-nemotron-nano-9b-v2  
nvidia/riva-translate-4b-instruct-v1.1  
nvidia/riva-translate-4b-instruct-v2  
nvidia/usdcode  

#### OpenAI
openai/gpt-oss-20b  
openai/gpt-oss-120b  

#### Poolside
poolside/laguna-xs-2-1  

#### Qwen
qwen/qwen2.5-coder-32b-instruct  
qwen/qwen3-next-80b-a3b-instruct  
qwen/qwen3-next-80b-a3b-thinking  
qwen/qwq-32b  

#### Sarvam AI
sarvamai/sarvam-m  

#### StepFun
stepfun-ai/step-3.5-flash  
stepfun-ai/step-5-preview  

#### Stockmark
stockmark/stockmark-2-100b-instruct  

#### Thinking Machines
thinking-machines/inkling  

#### Upstage
upstage/solar-10.7b-instruct  

#### Z.ai / GLM
z-ai/glm4.7  
z-ai/glm5.1  
z-ai/glm-5.2  
z-ai/glm-5.3  
z-ai/glm-5.3-flash  


</details>

</br>

--------

### Ollama
> Last checked: **2026-10-30**

- [Official pricing and cloud plans](https://ollama.com/pricing) · [Cloud models](https://ollama.com/search?c=cloud) · [2026-08-31 pricing transition](https://ollama.com/blog/transparent-pricing)
- **Pay as you go ($0/month)** means **no subscription**, not free inference: cloud token usage consumes purchased credits. The old blanket list of “free models” and **3-hour session resets** no longer describes the current published plans.
- Running local models on your own hardware incurs no Ollama cloud token charges.
- Cloud concurrency: **3** for Pay as you go and Pro; **10** for Max and Team. Some legacy accounts may have different conditions.

> **Free** model list

- Gemma4: 31b
- gpt-oss 20b/120b
- nemotron-3-nano 30B/super 120B-A12B/ultra 550B-A55B
- Reflection Beam 501B （limit time)

> **Session usage** reset in 3hours



| Plan | Subscription | Included cloud usage |
|---|---:|---:|
| Pay as you go | $0/month | None advertised; purchase usage credits |
| Pro | $20/month ($200/year) | $60/month |
| Max | $100/month | $300/month |
| Team | $500/month | $1,000/month shared |
| Enterprise | Custom | Custom |

<details>
<summary>Current cloud model pricing (USD per 1M input / 1M output tokens)</summary>

| Model | Input | Output | Combined |
|---|---:|---:|---:|
| deepseek-v4.1-flash (off-peak) | $0.15 | $0.60 | $0.75 |
| deepseek-v4.1-flash (standard) | $0.30 | $1.20 | $1.50 |
| deepseek-v4-pro (off-peak) | $0.66 | $1.98 | $2.64 |
| deepseek-v4-pro (standard) | $1.32 | $3.96 | $5.28 |
| gemma4 | $0.14 | $0.40 | $0.54 |
| glm-5.3 / glm-5.2 | $1.40 | $4.40 | $5.80 |
| glm-5.3-flash | $0.15 | $0.50 | $0.65 |
| gpt-oss:120b | $0.15 | $0.60 | $0.75 |
| gpt-oss:20b | $0.07 | $0.30 | $0.37 |
| kimi-k3 | $3.00 | $15.00 | $18.00 |
| kimi-k2.7-code / kimi-k2.6 | $0.95 | $4.00 | $4.95 |
| minimax-m3.1-flash | $0.15 | $0.60 | $0.75 |
| minimax-m3 | $0.60 | $2.40 | $3.00 |
| minimax-m2.7 | $0.30 | $1.20 | $1.50 |
| mistral-large-4 | $0.70 | $2.10 | $2.80 |
| mistral-large-3 | $0.50 | $1.50 | $2.00 |
| muse-spark-open | $1.25 | $4.25 | $5.50 |
| nemotron-3-nano | $0.06 | $0.24 | $0.30 |
| nemotron-3-super | $0.015 | $0.60 | $0.615 |
| nemotron-3-ultra | $0.10 | $3.00 | $3.10 |

Off-peak pricing applies to eligible models outside **12:00–18:00 UTC on weekdays**, and throughout weekends. See the official table for cached-input prices. This table is **paid cloud pricing**, not a free-tier model listing.

</details>

-------

### Groq
> Last checked: **2026-10-30**

The published free rate-limits table includes GPT-OSS 20B/120B and Qwen3.8 27B. Your account may have different limits.

https://console.groq.com/docs/rate-limits</br>
Endpoint (OpenAI-compatible): https://api.groq.com/openai/v1


<details>
<summary>

#### Model list

</summary>

| Model | Request/Minute | Request/Day | Token/Minute | Token/Day |
| --- | ---: | ---: | ---: | ---: |
| openai/gpt-oss-120b | 30 | 1K | 8K | 200K |
| openai/gpt-oss-20b | 30 | 1K | 8K | 200K |
| qwen/qwen3.8-27b | 30 | 1K | 8K | 200K |

</details>

---------

### ~~Cerebras~~
~~> Last checked: **2026-10-30**~~

**Unusable rate limit** 5$ per account

https://inference-docs.cerebras.ai/support/rate-limits</br>
Endpoint: https://api.cerebras.ai

| Model                                | Requests/Minute |   Tokens/Minute | Tokens/Hour | Tokens/Day |
|--------------------------------------|-----------------|---------------|-------------|------------|
| gpt-oss-120b                         | 5               |  30k          | 1M          | 1M         |
| gemma-4-31b                          | 5               |  30k          | 1M          | 1M         |


</br>

---------

### OpenRouter
> Last checked: **2026-10-30** </br>

https://openrouter.ai/collections/free-models </br>
https://openrouter.ai/pricing </br>

Endpoint (OpenAI-compatible): https://openrouter.ai/api/v1

**Models**: Check the live collection. `openrouter/free` can route to a free model; $0-priced models without `:free` can follow different eligibility rules.
- **Free usage limits**: If you’re using a free model variant (with an ID ending in **`:free`**/ **`(free)`** ) </br>
  you can make up to **`20`** requests/minute.</br>
  - If you have purchased less than **`$10 credits`**, you’re limited to **`50`** `free` model **requests/Day**.
  - If you purchase at least **`$10 credits`**, the daily limit increases to **`1000`** free model requests/day. Failed requests also count. See [official limits](https://openrouter.ai/docs/api-reference/limits) for purchase thresholds.

| Model variant (ID) | Credits purchased        | Rate limit (requests/min) | Daily limit (requests/day) |
|--------------------|--------------------------|---------------------------|----------------------------|
| *:free             | < $10 credits             | 20                        | 50                         |
| *:free             | ≥ $10 credits             | 20                        | 1000                       |


--------

### Cloudflare
> Official pricing page last updated: **2026-10-20** </br>
> Last Check: **2026-09-23** </br>


https://developers.cloudflare.com/workers-ai/platform/pricing/#llm-model-pricing </br>
https://developers.cloudflare.com/workers/platform/pricing/ </br>
- Workers Free: **10,000 Neurons/day** (resets 00:00 UTC); paid overage **$0.011 per 1,000 Neurons**. </br>
> "Neurons are our way of measuring AI outputs across different models, representing the GPU compute needed to perform your request. Our serverless model allows you to pay only for what you use without having to worry about renting, managing, or scaling GPUs."

**Billing requirement:** Certain Kimi, DeepSeek V4/V4.1 and GLM-5.x APIs require Workers Paid or prepaid AI Gateway credits **even with unused free Neurons**. Listed models are not all available without a billing method.

Models list </br>
- Llama
    - Llama2-7b
    - Llama3.1-8b/70b
    - Llama3.2-1b/3b/11b(vision)
    - Llama4-scout-17b-16e
- Qwen
    - qwq-32b
    - qwen2.5-coder-32b
    - **qwen3-30b-a3b**
    - **qwen3.8-27b**
- Mistral
    - Mistral-7b-intruct-v0.1
    - Mistral-small-3.1b-24b
- deepseek-r1-distill-qwen-32b
- deepseek V4 flash/pro and V4.1 flash 1017 
- Gemma
  - gemma-3-12b
  - **gemma-4-26B-A4B**
  - gemma-sea-lion-v4-27b-it
- granite-4.0-h-micro
- **glm-4.7-flash**
- **glm-5.2 / glm-5.3 / glm-5.3-flash**
- **nemotron-3-120b-a12b**
- **kimi-k2.5/k2.6/k2.7-code**
    
 <details>
  <summary>Full list with token cost</summary>  
   
> Pricing page updated October 20, 2026 (reviewed October 30)
>
> Unit: USD per 1M tokens
>
> Ranking method: `Combined = Input + Output`
>
> Free allocation: 10,000 Neurons per day
>
> Free Tokens/day assumes an Input : Output token ratio of `1 : 1.3`.
>
> Free-token estimates use Neurons-per-token rates rather than rounded USD prices; for billing-gated models these are **illustrative, not free account entitlements**.
>
> Cached input is excluded from the free-token calculation.
>
> Identical models from the same family are merged only when their pricing and relevant notes are identical.

| Rank | Provider | Model | Input | Output | Combined | 10K Neurons ≈ Tokens/day (I:O = 1:1.3) | Notes |
|---:|---|---|---:|---:|---:|---:|---|
| 1 | IBM | Granite 4.0 H Micro | $0.017 | $0.112 | **$0.129** | **~1.560M** | — |
| 2 | Meta | Llama 3.2 1B Instruct | $0.027 | $0.201 | **$0.228** | **~878K** | — |
| 3 | Mistral | Mistral 7B Instruct v0.1 | $0.110 | $0.190 | **$0.300** | **~708K** | — |
| 4 | Meta | Llama 3.2 3B Instruct | $0.051 | $0.335 | **$0.386** | **~520K** | — |
| 5 | Qwen | Qwen3 30B-A3B FP8 | $0.051 | $0.335 | **$0.386** | **~520K** | — |
| 6 | Meta | Llama 3/3.1 8B Instruct AWQ | $0.123 | $0.266 | **$0.389** | **~539K** | Identical pricing; merged |
| 7 | Google | Gemma 4 26B-A4B IT | $0.100 | $0.300 | **$0.400** | **~516K** | — |
| 8 | Meta | Llama 3.1 8B Instruct FP8 Fast | $0.045 | $0.384 | **$0.429** | **~465K** | — |
| 9 | Meta | Llama 3.1 8B Instruct FP8 | $0.152 | $0.287 | **$0.439** | **~482K** | — |
| 10 | Z.AI | GLM-4.7 Flash | $0.060 | $0.400 | **$0.460** | **~435K** | — |
| 11 | OpenAI | GPT-OSS 20B | $0.200 | $0.300 | **$0.500** | **~429K** | — |
| 12 | Meta | Llama Guard 3 8B | $0.484 | $0.030 | **$0.514** | **~484K** | Safety classifier; not a general-purpose chat LLM |
| 13 | Meta | Llama 3.2 11B Vision Instruct | $0.049 | $0.676 | **$0.725** | **~273K** | Vision-capable |
| 14 | Google | Gemma 3 12B IT | $0.345 | $0.556 | **$0.901** | **~237K** | — |
| 15 | AI Singapore | Gemma SEA-LION v4 27B IT | $0.351 | $0.555 | **$0.906** | **~236K** | — |
| 16 | Mistral | Mistral Small 3.1 24B Instruct | $0.351 | $0.555 | **$0.906** | **~236K** | — |
| 17 | OpenAI | GPT-OSS 120B | $0.350 | $0.750 | **$1.100** | **~191K** | — |
| 18 | Meta | Llama 3/3.1 8B Instruct | $0.282 | $0.827 | **$1.109** | **~187K** | Identical pricing; merged |
| 19 | Meta | Llama 4 Scout 17B-16E Instruct | $0.270 | $0.850 | **$1.120** | **~184K** | — |
| 20 | Qwen | QwQ 32B | $0.660 | $1.000 | **$1.660** | **~129K** | — |
| 21 | Qwen | Qwen2.5 Coder 32B Instruct | $0.660 | $1.000 | **$1.660** | **~129K** | — |
| 22 | DeepSeek | DeepSeek V4 Flash 0731 | $0.440 | $1.320 | **$1.760** | **~117K** | Cached input $0.014; paid billing method required |
| 23 | NVIDIA | Nemotron 3 120B-A12B | $0.500 | $1.500 | **$2.000** | **~103K** | — |
| 24 | Meta | Llama 3.1/3.3 70B Instruct FP8 Fast | $0.293 | $2.253 | **$2.546** | **~78.5K** | Identical pricing; merged |
| 25 | Moonshot AI | Kimi K2.5 | $0.600 | $3.000 | **$3.600** | **~56.2K** | Cached input $0.100 |
| 26 | Qwen | Qwen3.8 27B | $0.450 | $3.200 | **$3.650** | **~54.9K** | — |
| 27 | Moonshot AI | Kimi K2.6 | $0.950 | $4.000 | **$4.950** | **~41.1K** | Cached input $0.160; paid billing method required |
| 28 | Moonshot AI | Kimi K2.7 Code | $0.950 | $4.000 | **$4.950** | **~41.1K** | Cached input $0.190; paid billing method required |
| 29 | DeepSeek | DeepSeek V4 Pro 0813 | $1.320 | $3.960 | **$5.280** | **~39.1K** | Cached input $0.044; paid billing method required |
| 30 | DeepSeek | DeepSeek R1 Distill Qwen 32B | $0.497 | $4.881 | **$5.378** | **~37.0K** | — |
| 31 | Z.AI | GLM-5.2 | $1.400 | $4.400 | **$5.800** | **~35.5K** | Cached input $0.260; paid billing method required |
| 32 | Meta | Llama 2 7B Chat FP16 | $0.556 | $6.667 | **$7.223** | **~27.4K** | — |

 </details>


---------


### Cohere
> Last web updated: **2026-06-09**</br>
> Last Check: **2026-10-30** </br>

https://docs.cohere.com/docs/rate-limits

Endpoint: https://api.cohere.ai/compatibility

| Endpoint            | Trial rate limit (requests/min)  | Trial monthly cap (calls/month)   |
|---------------------|----------------------------------|----------------------------------|
| Chat API            | 20/min (per model)               | 1000/month                       |

- Chat model includes
  - Command A+
  - Command A Reasoning
  - Command A Translate
  - Command A Vision
  - Command A
  - Command R+
  - Command R
  - Command R7B
  - North Mini Code


> All endpoints are limited to 1,000 calls per month with a trial key

--------

### Z.ai (GLM-4.5/4.7-Flash)

> Last Check: **2026-10-30** </br>

https://docs.z.ai/guides/overview/pricing </br>

Endpoint: https://api.z.ai/api/paas/v4

**Free Models :**
- GLM-4.5-Flash
- GLM-4.7-Flash
- GLM-4.6V-Flash

> No offical rate usage limits

-------


### ~~Github~~

~~https://docs.github.com/en/github-models/use-github-models/prototyping-with-ai-models#rate-limits~~

> GitHub Models has been retired.  
> As of July 30, 2026, GitHub Models has been fully retired. The playground, model catalog, inference API, and bring your own key (BYOK) are no longer available to any customer.  
> GitHub Models was a separate service from GitHub Copilot and is unrelated to GitHub Copilot services.  

---------

### Mistral
> Last checked: **2026-10-30**

[Official rate-limit guide](https://docs.mistral.ai/admin/billing-usage/usage-limits) · [Explanation](https://help.mistral.ai/en/articles/698531-why-am-i-hitting-api-rate-limits-and-how-do-i-increase-them)

Free-mode limits depend on the **organization and model**. The old numeric cap below is a historical community report, **not a guaranteed free-tier entitlement**. Check **Admin Panel → API → Limits**.


Endpoint: https://api.mistral.ai

- From community&reports; **No offcial list**

| Plan / Tier         | Requests/second (RPS) | Tokens/minute (TPM) | Tokens/month      |
|---------------------|---------------------------|--------------------------|------------------------|
| Mistral API Free    | 1/sec                         | 500k                 | 1 billion     |

----------

### SambaNova

> Last checked: **2026-10-30**

https://docs.sambanova.ai/docs/en/models/rate-limits#free-tier


| Model                                | Requests/Minute |  Requests/Day | Tokens/Day |
|--------------------------------------|-----------------|---------------|------------|
| DeepSeek-V3.1                        | 20               |  20          |  200k        |
| Meta-Llama-3.3-70B-Instruct          | 20               |  20          |  200k        |
| gpt-oss-120b                         | 20               |  20          |  200k        |
| DeepSeek-V3.2                        | 20               |  20          |  200k        |
| gemma-4-31B-it                       | 20               |  20          |  200k        |

-----------

### AionLabs

> Last checked: **2026-10-30**

https://www.aionlabs.ai/docs/rate-limits/

https://www.aionlabs.ai/docs/models/

Endpoint: https://api.aionlabs.ai/v1

**Shared free-tier caps:** 15 RPM, 20K TPM, 20K tokens/day ([official rate limits](https://www.aionlabs.ai/docs/rate-limits/)).

| Model                                | Requests/Minute | Tokens/Day |
|--------------------------------------|----------------- |------------|
| Aion-2.0 (DeepSeek V3.2 finetune)                     | 15               |  20k        |
| Aion-2.5 (Improve of Aion-2.0)                        | 15               |  20k        |
| Aion-3.0 (GLM)                                        | 15               |  20k        |
| Aion-3.0 Mini (Deepseek)                              | 15               |  20k        |
| Aion-3.5 (GLM)                                        | 15               |  20k        |
| Aion-3.5 Mini (GLM)                                   | 15               |  20k        |
| Aion-RP 1.0 (8B) (llama-3.1-8b fineune/openweight)    | 15               |  20k        |

------

### SKT 
Free Api for **A.X 4.0** (7B/72B, based on Qwen2.5) </br>
**Korean⇌EN** </br>
https://github.com/SKT-AI/A.X-4.0/blob/main/apis/README.md


### IBM
> Last Check: **2026-10-08** </br>


https://www.ibm.com/products/watsonx-ai/pricing

| Plan / Tier         | Requests/second (RPS) |  Tokens/month      |
|---------------------|---------------------------|------------------------|
| watsonx.ai Free tier </br> (Foundation Models)| 2/sec                        | 300k     |


-----------


### Scaleway (1M free token/per account-no refresh)
https://www.scaleway.com/en/docs/generative-apis/faq/#how-does-the-free-tier-work

--------


### ~~Together AI (certain free-endpoint:no text models now)~~ 
~~> Last updated: **2025-11-17**~~

~~https://www.together.ai/models~~
~~- Llama3-70b </br>~~
~~https://www.together.ai/models/llama-3-3-70b-free </br>~~
~~https://www.together.ai/models/deepseek-r1-distilled-llama-70b-free  </br>~~

**NO FREE TIER** Now </br>
https://support.together.ai/articles/1862638756-changes-to-free-tier-and-billing-july-2025

-----------

</br>

## CN Platform

> **最后核查：2026 年 10 月 30 日**
>
> 本节区分**持续免费推理**、**定期发放的额度**、**一次性试用 Token/代金券**和**非模型 API 的产品积分**。免费模型、使用限制、活动及地区政策可能随时变化，请以登录后的平台控制台为准。本次核查依据平台文档及公告，**未使用实际账号逐一测试 API**。

### 魔搭社区（ModelScope）

**免费方式：** 每日魔粒积分，可用于模型推理；并非无限次免费 API。

**官方资料：** [API-Inference 调用限制](https://modelscope.cn/docs/model-service/API-Inference/limits) · [魔粒体系公告（2026-08-10）](https://www.modelscope.cn/posts/435591) · [魔粒使用说明](https://www.modelscope.cn/magicube/usage)

**API 地址（兼容 OpenAI）：** `https://api-inference.modelscope.cn/v1`

- 使用 API-Inference 需要绑定**已完成实名认证的阿里云账号**。
- 根据现行魔粒体系，每日登录可领取 **200 魔粒**，绑定阿里云账号可额外获得 **50 魔粒/天**；参与社区活动还可能获得额外积分。
- 模型推理消耗参考：轻量模型约 **0.5 魔粒/次**，主流模型约 **1 魔粒/次**，旗舰模型约 **2 魔粒/次**。实际以具体模型的计费规则为准。
- 旧版规则列有**所有模型合计 2,000 次/天、单模型最多 500 次/天**，部分大型模型限制更严格。这些数字不能直接当作当前账号每天可获得的免费调用次数；还需考虑魔粒余额、模型限额及并发限制。
- 免费共享推理资源主要用于体验和开发测试，不保证生产环境服务等级；使用前请查看账号剩余积分及模型限制。

---

### 硅基流动（SiliconFlow）

**免费方式：** 部分模型长期标价为 0 元；另有活动代金券，两者应分开计算。

**官方资料：** [免费模型及限流规则](https://docs.siliconflow.cn/docs/userguide/faqs/rate-limit-and-upgradation) · [免费与 Pro 模型说明](https://docs.siliconflow.cn/docs/userguide/faqs/misc) · [2026 年代金券活动公告](https://www.siliconflow.cn/developer-talk/od7wj9rr23p95uhihmhrombp)

**API 地址（兼容 OpenAI）：** `https://api.siliconflow.cn/v1`

- 完成**实名认证**后，可调用模型列表中当前明确标注为**免费**的模型，相关推理费用为 **0 元**。
- 免费模型有**按模型区分的调用速率限制**。部分付费版本带有 `Pro/` 前缀，但不能仅凭模型大小或是否带有该前缀判断是否免费，应以模型详情页的实际价格为准。
- **活动代金券：** 官方 2026 年「推荐官」活动（**2026-01-15 至 2026-12-31**）提供实名认证后领取的 **16 元通用代金券**，须在活动中心**主动领取**，领取后 **180 天内有效**；邀请奖励另行计算。
- 仓库此前所写「中国手机号新用户注册即送 **2,000 万 tokens**」未能确认仍为当前普遍适用的注册权益，因此不再作为确定额度展示。

---

### 腾讯云 TokenHub

**免费方式：** 新用户一次性试用 Token；**不属于持续免费的模型 API**。

**官方资料：** [TokenHub 中国站新用户免费体验](https://cloud.tencent.com/document/product/1823/130053) · [TokenHub API 快速入门](https://cloud.tencent.com/document/product/1823/130058) · [旧混元平台停服公告](https://cloud.tencent.com/announce/detail/2287)

- **腾讯混元旧 API 平台已停止服务：** 旧平台于 **2026-06-30** 停止新购和创建密钥，于 **2026-09-30** 关闭原控制台及 API 服务。新的模型接入应使用 **TokenHub**，其提供混元及第三方模型。
- **中国大陆站：** 官方新用户活动说明列出语言模型 **100 万 tokens** 的试用额度，**领取后一年内有效**；活动公布的结束日期为 **2026-12-31**。这属于**一次性试用权益**，部分模型或账号可能有单独限制。
- 需要完成腾讯云**实名认证**。免费资源包可通过模型列表或开通页面领取，部分权益可能在首次调用时自动发放；最终以控制台显示为准。
- **避免意外扣费：** 如不希望试用额度耗尽后产生费用，请关闭后付费模式。未开启后付费时，免费额度用尽后调用将停止。
- **中国站与国际站不可混用：** 腾讯云国际站 TokenHub 的试用有效期为 **90 天**，部分模型开通还可能要求 **1 美元余额预授权**，与中国站的规则不同。
- 此前的旧版「Hunyuan-lite 免费」和旧混元平台 **100 万 tokens / 一年**资源包属于历史权益，不能作为已经停服的旧 API 仍可使用的依据。

---

### 火山方舟（Volcengine Ark）

**免费方式：** 模型推理 API 一次性体验额度；与扣子的积分体系不同。

**官方资料：** [安心体验模式](https://docs.volcengine.com/docs/ark/free-tokens-only-mode?lang=zh) · [模型开通与免费额度管理](https://docs.volcengine.com/docs/ark/activation-management?lang=zh)

- **安心体验模式：** 符合条件的**新用户**可通过该模式使用 **50 万 tokens** 模型推理体验额度；额度用尽后，符合条件的推理服务会**暂停而不是继续扣费**。
- 该模式须在**首次开通模型推理服务时**选择。已通过其他模式开通服务的账号可能不再符合条件；**关闭安心体验模式后不能重新开启**。
- 此模式的免费额度仅覆盖适用范围内的**模型推理 Token**。工具、插件、知识库等其他功能可能单独计费。
- 平台还可能提供其他按模型、活动或账号发放的免费资源包，具体数量与适用条件请查看控制台。
- 旧版「**500 资源点/天**」及豆包模型资源点消耗表属于**扣子（Coze）**的计费体系，**不是火山方舟 API 的免费额度或定价**，因此已从本节移除。

---

### 扣子（Coze）

**免费方式：** AI 应用与智能体平台积分；**不等同于通用模型推理 API 免费额度**。

**官方资料：** [2026 年订阅体系升级公告](https://docs.volcengine.com/docs/coze/button-subscription-package-upgrade?lang=zh) · [现行订阅套餐](https://docs.volcengine.com/docs/coze/Subscriptionpackage?lang=zh) · [积分规则](https://docs.volcengine.com/docs/coze/integral?lang=zh)

- **2026-01-18** 的套餐升级将「资源点」更名为「积分」。升级公告提出个人免费版**每日签到领取 1,500 积分**（**当天有效**），取代此前的 500 资源点/天。
- **现行资料存在口径差异：** 当前套餐表未将每月订阅积分列入个人免费版；积分规则又明确列出**新用户一次性获得 1,500 积分**（**30 天有效**），相关常见问题仍提及每日签到奖励。因此，不能在未查看账号活动页面的情况下保证所有用户每天都能固定领取 1,500 积分。
- 扣子积分主要用于平台产品和功能，**不能直接换算成火山方舟 API 的免费 Token 数量**。
- 原仓库中按旧版扣子资源点计算的豆包、DeepSeek、Kimi 模型消耗表已移除，以免把过期计费规则当作现行价格。

---

### 快手万擎（StreamLake Vanchin）

**免费方式：** 新用户或活动提供的模型在线推理试用资源包。

**官方资料：** [免费推理额度说明（2025-12-12 更新）](https://streamlake.com/document/WANQING/mdsor5767ob7s796sp6) · [模型计费说明](https://streamlake.com/document/WANQING/mdsorb4ejjptsmfyrn)

- 需要完成**注册、认证和服务开通**，方可使用符合条件的免费推理资源包。
- 免费资源包通常按**具体模型**发放，同一主账号下共享；未确认所有新用户均能领取相同数量的 Token，因此不填写统一免费额度。实际余额请在**费用中心 → 资源包**中查看。
- 资源包可抵扣符合条件的**在线推理输入、输出及缓存命中 Token**，但**不能抵扣批量推理**。
- **注意超额费用：** 免费额度过期或用尽后继续调用，可能产生按量计费账单。建议及时查看用量，并在支持的情况下限制或关闭后付费调用。

---

### 讯飞星火（iFLYTEK Spark）

**免费方式：** 部分模型标价为 0 元，另有独立的活动赠送额度。

**官方资料：** [Spark Lite HTTP API 文档](https://www.xfyun.cn/doc/spark/HTTP%E8%B0%83%E7%94%A8%E6%96%87%E6%A1%A3.html) · [Spark-X2.5 模型说明](https://www.xfyun.cn/doc/spark/Spark-X2.5%E6%A8%A1%E5%9E%8B%E4%BB%8B%E7%BB%8D.html) · [星火模型与价格页面](https://spark.xfyun.cn/sparkapi)

- **Spark Lite：** 官方 HTTP API 文档标注支持**免费使用**。
- **Spark Lite 经典 API 地址（兼容 OpenAI）：** `https://spark-api-open.xf-yun.com/v1/`。
- **Spark-X2.5-1.7B**（模型 ID：`spark-x2.5-1.7b`）：现行模型列表标价为 **0 元/百万 tokens**。
- **Spark-X2.5-4B**（模型 ID：`spark-x2.5-4b`）：模型列表出现 **0 元/百万 tokens / 限时免费**标注，**不可视为永久免费**。X2.5 系列属于星火模型平台，调用前需另行确认适用的 API 地址及鉴权方式。
- 旧版「首次开通后，所有模型共享 **20 万免费 tokens，有效期一年**」未能找到明确的现行依据，故不再将其列为确定权益。

---

### 心流（iFlow，已停止服务）

**状态：原免费 LLM API 与托管模型库已于 2026 年 4 月 17 日停止服务，不再属于当前可用的免费模型 API 平台。**

**官方资料：** [2026-03-20 停服公告](https://vibex.iflow.cn/t/topic/4819) · [2026-04-17 停服通知](https://vibex.iflow.cn/t/topic/5753)

- 原有 **iFlow API 服务及托管模型库**于 **2026-04-17** 关闭，相关 iFlow CLI 内置模型访问也随之停止。
- iFlow CLI 仍可配置**其他平台的兼容 API**，但这不代表原心流托管模型服务恢复。
- 本条仅作**历史记录**，不应再列为可用免费 API 推荐项。

---

## [LLM PRICE LIST](https://github.com/CYBIRD-D/LLM-API-Official-Pricing-Tracker)

### LLM API Pricing — 2026-10-30

> **Updated from the [LLM API Official Pricing Tracker](https://github.com/CYBIRD-D/LLM-API-Official-Pricing-Tracker) (source table dated 2026-10-30).** This is a synchronized reference, not a live price feed. Provider prices and promotions can change; check the individual Pricing Source before purchasing.
>
> - **Unit:** USD per 1 million tokens.
> - **Combined = Input + Output:** the price of 1M uncached input tokens **plus** 1M output tokens (not the cost per 1M total tokens).
> - **Cached Input:** `—` means the cache price is **unknown / not listed**, not zero.
> - **Order:** lowest Combined cost first. Ties use the lowest directly comparable confirmed Cached Input price.
> - **Promotions, regular/future prices and peak/off-peak rates** occupy separate rows when present in the source tracker. Faster or priority API variants are also included where the source lists separately priced variants.
> - **Context tiers:** use the default/lowest tier for ranking; higher-tier rates appear in Notes.
> - **Models:** same-family variants are combined only when the upstream tracker treats their prices and conditions as equivalent.
> - **Qwen:** Alibaba Cloud Model Studio Singapore / International pricing.
> - **Table layout preserved:** Rank, Provider, Model, Input, Cached Input, Output, Combined, Notes and Pricing Source. Open/Closed status and parameter counts can be found in the [full tracker](https://github.com/CYBIRD-D/LLM-API-Official-Pricing-Tracker#price-leaderboard).

| Rank | Provider | Model | Input | Cached Input | Output | Combined | Notes | Pricing Source |
|---:|---|---|---:|---:|---:|---:|---|---|
| 1 | Qwen | Qwen3.7 Flash | $0.03 | — | $0.13 | **$0.16** | ≤32K; 32K–256K: $0.10/$0.40; 256K–1M: $0.20/$0.80 | [Source](https://www.alibabacloud.com/help/en/model-studio/model-pricing) |
| 2 | Meta / OpenRouter | Muse Spark 1.2/1.3 Contributor | $0.10 | $0.002 | $0.20 | **$0.30** | 1M context; prompts/outputs may be used to improve Meta products | [Source](https://openrouter.ai/meta/muse-spark-1.3-contributor) |
| 3 | Qwen | Qwen3.5 Flash | $0.10 | — | $0.40 | **$0.50** | International | [Source](https://www.alibabacloud.com/help/en/model-studio/model-pricing) |
| 4 | Anthropic | Claude Haiku 5.5 | $0.10 | $0.01 | $0.50 | **$0.60** | ≤100K; >100K: $0.50 input / $0.05 cache / $2.50 output | [Source](https://platform.claude.com/docs/en/models/haiku-5-5/overview) |
| 5 | OpenAI | GPT-6 Luna | $0.10 | $0.01 | $0.50 | **$0.60** | 1.05M context; >272K: $0.20/$0.75 | [Source](https://developers.openai.com/api/docs/pricing) |
| 6 | Qwen | Qwen3.8 Flash | $0.15 | — | $0.47 | **$0.62** | International; 1M context | [Source](https://www.alibabacloud.com/help/en/model-studio/model-pricing) |
| 7 | GLM / Z.AI | GLM-5.3-Flash | $0.15 | $0.03 | $0.50 | **$0.65** | Standard price | [Source](https://docs.z.ai/guides/overview/pricing) |
| 8 | DeepSeek | DeepSeek V4.1 Flash 1017 — Off-peak | $0.15 | $0.003 | $0.60 | **$0.75** | 1M context; 1017 update (unchanged API rates); off-peak pricing | [Source](https://api-docs.deepseek.com/quick_start/pricing/) |
| 9 | MiniMax | MiniMax M3.1 Flash | $0.15 | $0.015 | $0.60 | **$0.75** | 1M context; model weights now publicly available; multimodal input | [Source](https://www.minimax.io/blog/minimax-m31f) |
| 10 | Mistral | Mistral Small 4 | $0.15 | $0.015 | $0.60 | **$0.75** | 256K context | [Source](https://docs.mistral.ai/models/mistral-small-4-0-26-03) |
| 11 | OpenAI | GPT-5.6 Luna | $0.20 | $0.02 | $1.20 | **$1.40** | >272K: $0.40/$1.80 | [Source](https://developers.openai.com/api/docs/pricing) |
| 12 | Meta / OpenRouter | Muse Glimmer 30B | $0.30 | $0.04 | $1.10 | **$1.40** | 131K context | [Source](https://openrouter.ai/meta/muse-glimmer-30b) |
| 13 | OpenAI | GPT-5.4 nano | $0.20 | $0.02 | $1.25 | **$1.45** | — | [Source](https://developers.openai.com/api/docs/pricing) |
| 14 | DeepSeek | DeepSeek V4.1 Flash 1017 — Peak | $0.30 | $0.006 | $1.20 | **$1.50** | 1M context; 1017 update (unchanged API rates); peak pricing | [Source](https://api-docs.deepseek.com/quick_start/pricing/) |
| 15 | MiniMax | MiniMax M2.7 | $0.30 | $0.06 | $1.20 | **$1.50** | ~205K context; cache write $0.375/MTok | [Source](https://platform.minimax.io/docs/guides/pricing-paygo) |
| 16 | MiniMax | MiniMax M3 | $0.30 | $0.06 | $1.20 | **$1.50** | ≤512K prompt; >512K: $0.60 input / $0.12 cache / $2.40 output; permanent 50% discount | [Source](https://platform.minimax.io/docs/guides/pricing-paygo) |
| 17 | Qwen | Qwen3.7 Plus (Promo) | $0.32 | — | $1.28 | **$1.60** | International alias; 20% off; regular $0.40/$1.60 | [Source](https://www.alibabacloud.com/help/en/model-studio/model-pricing) |
| 18 | Google | Gemini 3.1 Flash-Lite | $0.25 | $0.025 | $1.50 | **$1.75** | — | [Source](https://ai.google.dev/gemini-api/docs/pricing) |
| 19 | Qwen | Qwen3.6 Flash | $0.25 | — | $1.50 | **$1.75** | ≤256K; International | [Source](https://www.alibabacloud.com/help/en/model-studio/model-pricing) |
| 20 | Qwen | Qwen3.7 Plus (Regular Price) | $0.40 | — | $1.60 | **$2.00** | ≤256K | [Source](https://www.alibabacloud.com/help/en/model-studio/model-pricing) |
| 21 | MiniMax | MiniMax M3 — Priority | $0.45 | $0.09 | $1.80 | **$2.25** | ≤512K prompt; faster priority serving; >512K: $0.90/$0.18/$3.60; permanent 50% discount | [Source](https://platform.minimax.io/docs/guides/pricing-paygo) |
| 22 | DeepSeek | DeepSeek V4 Pro — Off-peak | $0.66 | $0.022 | $1.98 | **$2.64** | Off-peak pricing | [Source](https://api-docs.deepseek.com/quick_start/pricing/) |
| 23 | Google | Gemini 3.5 Flash-Lite | $0.30 | $0.03 | $2.50 | **$2.80** | — | [Source](https://ai.google.dev/gemini-api/docs/pricing) |
| 24 | Mistral | Mistral Large 4 | $0.70 | $0.07 | $2.10 | **$2.80** | 1M context; Oct 29 open release; current official standard API price | [Source](https://docs.mistral.ai/models/mistral-large-4-0) |
| 25 | Qwen | Qwen3.5 Plus | $0.40 | — | $2.40 | **$2.80** | ≤256K; International | [Source](https://www.alibabacloud.com/help/en/model-studio/model-pricing) |
| 26 | MiniMax | MiniMax M2.7 Highspeed | $0.60 | $0.06 | $2.40 | **$3.00** | Same open M2.7 model, faster serving; ~205K context; cache write $0.375/MTok | [Source](https://platform.minimax.io/docs/guides/pricing-paygo) |
| 27 | xAI | Grok Build 0.1 | $1.00 | $0.20 | $2.00 | **$3.00** | <200K; ≥200K: $2/$4 | [Source](https://docs.x.ai/developers/pricing) |
| 28 | Qwen | Qwen3.6 Plus | $0.50 | — | $3.00 | **$3.50** | ≤256K; International | [Source](https://www.alibabacloud.com/help/en/model-studio/model-pricing) |
| 29 | xAI | Grok 4.20/4.3 | $1.25 | $0.20 | $2.50 | **$3.75** | <200K; ≥200K: $2.50/$5 | [Source](https://docs.x.ai/developers/pricing) |
| 30 | GLM / Z.AI | GLM-5 | $1.00 | $0.20 | $3.20 | **$4.20** | — | [Source](https://docs.z.ai/guides/overview/pricing) |
| 31 | Google | Gemini 3.6/3.8 Flash (Promo) | $0.75 | $0.075 | $3.75 | **$4.50** | Introductory price through Dec 31, 2026; 3.7 retired (redirects to 3.8) | [Source](https://ai.google.dev/gemini-api/docs/pricing) |
| 32 | Kimi | Kimi K2.6 | $0.95 | $0.16 | $4.00 | **$4.95** | ~262K context | [Source](https://www.kimi.com/) |
| 33 | Kimi | Kimi K2.7 Code | $0.95 | $0.19 | $4.00 | **$4.95** | ~262K context | [Source](https://www.kimi.com/) |
| 34 | GLM / Z.AI | GLM-5-Turbo | $1.20 | $0.24 | $4.00 | **$5.20** | 200K context; agent-tuned Turbo variant | [Source](https://docs.z.ai/guides/overview/pricing) |
| 35 | OpenAI | GPT-5.4 mini | $0.75 | $0.075 | $4.50 | **$5.25** | — | [Source](https://developers.openai.com/api/docs/pricing) |
| 36 | DeepSeek | DeepSeek V4 Pro — Peak | $1.32 | $0.044 | $3.96 | **$5.28** | Peak pricing | [Source](https://api-docs.deepseek.com/quick_start/pricing/) |
| 37 | Meta / OpenRouter | Muse Spark 1.1/1.2/1.3 | $1.25 | $0.15 | $4.25 | **$5.50** | 1M context; standard data policy | [Source](https://openrouter.ai/meta/muse-spark-1.3) |
| 38 | Meta / OpenRouter | Muse Spark Open | $1.25 | $0.15 | $4.25 | **$5.50** | 1M context; released Oct 15; public weights (safety post-trained, same base as Muse Spark 1.3) | [Source](https://openrouter.ai/meta/muse-spark-open) |
| 39 | GLM / Z.AI | GLM-5.1 | $1.40 | $0.26 | $4.40 | **$5.80** | 200K context | [Source](https://docs.z.ai/guides/overview/pricing) |
| 40 | GLM / Z.AI | GLM-5.2/5.3 | $1.40 | $0.26 | $4.40 | **$5.80** | 1M context | [Source](https://docs.z.ai/guides/overview/pricing) |
| 41 | OpenAI | GPT-6.1 Terra | $1.00 | $0.05 | $5.00 | **$6.00** | 1.05M context; >272K prompt: $2 input / $0.10 cache / $7.50 output; 30m cache write $1.25 | [Source](https://developers.openai.com/api/docs/models/gpt-6.1-terra) |
| 42 | xAI | Grok 4.5 | $2.00 | $0.30 | $6.00 | **$8.00** | <200K; ≥200K: $4/$12 | [Source](https://docs.x.ai/developers/pricing) |
| 43 | xAI | Grok 4.6 | $2.00 | $0.50 | $6.00 | **$8.00** | <200K; ≥200K: $4/$12 | [Source](https://docs.x.ai/developers/pricing) |
| 44 | xAI | Grok 4.7 | $2.00 | $0.50 | $6.00 | **$8.00** | 500K context; ≥200K: $4/$12 | [Source](https://docs.x.ai/developers/pricing) |
| 45 | Qwen | Qwen3.8 Max | $2.00 | — | $6.00 | **$8.00** | International; 1M context | [Source](https://www.alibabacloud.com/help/en/model-studio/model-pricing) |
| 46 | Google | Gemini 3.6/3.8 Flash (Regular Price) | $1.50 | $0.15 | $7.50 | **$9.00** | Standard price from Jan 1, 2027; 3.7 retired (redirects to 3.8) | [Source](https://ai.google.dev/gemini-api/docs/pricing) |
| 47 | Mistral | Mistral Medium 3.5 | $1.50 | $0.15 | $7.50 | **$9.00** | 256K context | [Source](https://docs.mistral.ai/models/) |
| 48 | Kimi | Kimi K2.7 Code Highspeed | $1.90 | $0.38 | $8.00 | **$9.90** | ~262K; same K2.7 Code model, faster output | [Source](https://www.kimi.com/) |
| 49 | Qwen | Qwen3.7 Max | $2.50 | — | $7.50 | **$10.00** | International; 1M context | [Source](https://www.alibabacloud.com/help/en/model-studio/model-pricing) |
| 50 | Anthropic | Claude Sonnet 5.5 | $2.00 | $0.10 | $10.00 | **$12.00** | Cache read reduced to $0.10 on Oct 7 | [Source](https://platform.claude.com/docs/en/about-claude/pricing) |
| 51 | Google | Gemini 4 Argon (Promo) | $2.00 | $0.10 | $10.00 | **$12.00** | 1M context; implicit caching only; offer through Nov 30, 2026 | [Source](https://cloud.google.com/blog/products/ai-machine-learning/gemini-4-argon-available-on-google-cloud) |
| 52 | OpenAI | GPT-6.1 Sol | $2.00 | $0.10 | $10.00 | **$12.00** | 1.05M context; >272K: $4/$0.20/$15 | [Source](https://developers.openai.com/api/docs/pricing) |
| 53 | Anthropic | Claude Sonnet 5 | $2.00 | $0.20 | $10.00 | **$12.00** | — | [Source](https://platform.claude.com/docs/en/about-claude/pricing) |
| 54 | OpenAI | GPT-6 Sol | $2.00 | $0.20 | $10.00 | **$12.00** | 1.05M context; >272K: $4/$0.40/$15 | [Source](https://developers.openai.com/api/docs/pricing) |
| 55 | Kimi | Kimi K3.1 Pro | $2.00 | $0.20 | $10.00 | **$12.00** | 1M context; 5-min cache write $2/MTok; planned Open release by Nov 4 (not yet released) | [Source](https://platform.kimi.ai/) |
| 56 | Google | Gemini 3.1 Pro Preview | $2.00 | $0.20 | $12.00 | **$14.00** | ≤200K; >200K: $4/$18 | [Source](https://ai.google.dev/gemini-api/docs/pricing) |
| 57 | OpenAI | GPT-5.6 Terra | $2.00 | $0.20 | $12.00 | **$14.00** | >272K: $4/$18 | [Source](https://developers.openai.com/api/docs/pricing) |
| 58 | OpenAI | GPT-5.4 | $2.50 | $0.25 | $15.00 | **$17.50** | >272K long-context surcharge | [Source](https://developers.openai.com/api/docs/pricing) |
| 59 | Anthropic | Claude Sonnet 4.6 | $3.00 | $0.30 | $15.00 | **$18.00** | — | [Source](https://platform.claude.com/docs/en/about-claude/pricing) |
| 60 | Kimi | Kimi K3 | $3.00 | $0.30 | $15.00 | **$18.00** | 1M context | [Source](https://www.kimi.com/) |
| 61 | Anthropic | Claude Opus 5.5 | $4.00 | $0.20 | $20.00 | **$24.00** | 1M context | [Source](https://platform.claude.com/docs/en/about-claude/pricing) |
| 62 | Google | Gemini 4 Argon (Regular Price) | $4.00 | $0.20 | $20.00 | **$24.00** | 1M context; implicit caching only; from Dec 1, 2026 | [Source](https://cloud.google.com/blog/products/ai-machine-learning/gemini-4-argon-available-on-google-cloud) |
| 63 | Kimi | Kimi K3.1 Pro Highspeed | $4.00 | $0.20 | $20.00 | **$24.00** | Same K3.1 Pro model, 2–3× faster; 1M context; 5-min cache write $4/MTok | [Source](https://platform.kimi.ai/) |
| 64 | Meta | Muse Wonder | $4.00 | $0.20 | $20.00 | **$24.00** | 1M context; Meta Model API / OpenRouter; Wonder Full is subscription-only | [Source](https://dev.meta.ai/models/muse-wonder) |
| 65 | OpenAI | GPT-5.6 Sol (Promo) | $4.00 | $0.40 | $20.00 | **$24.00** | Promo available at least through Nov 21, 2026; regular $5/$30 | [Source](https://developers.openai.com/api/docs/pricing) |
| 66 | Anthropic | Claude Opus 4.7/4.8/5 | $5.00 | $0.50 | $25.00 | **$30.00** | — | [Source](https://platform.claude.com/docs/en/about-claude/pricing) |
| 67 | OpenAI | GPT-5.5 | $5.00 | $0.50 | $30.00 | **$35.00** | — | [Source](https://developers.openai.com/api/docs/pricing) |
| 68 | OpenAI | GPT-5.6 Sol (Regular Price) | $5.00 | $0.50 | $30.00 | **$35.00** | Original price; currently $4/$20 promo | [Source](https://developers.openai.com/api/docs/pricing) |
| 69 | Anthropic | Claude Fable 5.1 | $10.00 | $0.25 | $50.00 | **$60.00** | 1M context; low 0.025x cache-read multiplier | [Source](https://platform.claude.com/docs/en/about-claude/pricing) |
| 70 | Anthropic | Claude Fable 5 | $10.00 | $1.00 | $50.00 | **$60.00** | — | [Source](https://platform.claude.com/docs/en/about-claude/pricing) |
| 71 | OpenAI | GPT-6 Astra | $10.00 | $1.00 | $50.00 | **$60.00** | 1.05M context; >272K: $20/$2/$75 | [Source](https://developers.openai.com/api/docs/pricing) |
| 72 | OpenAI | GPT-5.4/5.5 Pro | $30.00 | — | $180.00 | **$210.00** | Maximum-compute tier | [Source](https://developers.openai.com/api/docs/pricing) |

> **DeepSeek peak/off-peak:** Peak hours are **01:00–04:00 UTC and 06:00–10:00 UTC**; all other hours are off-peak. For **DeepSeek V4.1 Flash 1017**, the source tracker gives **$0.15 input / $0.003 cached input / $0.60 output** (off-peak) and **$0.30 / $0.006 / $1.20** (peak). DeepSeek V4 Pro rates are listed in their own peak and off-peak rows above.
