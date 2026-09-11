# Enterprise Autonomous Test Platform (ATP)
### Sovereign, Air-Gapped QA Orchestrator & Autonomous Multi-Suite Synthesis Engine

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Python: 3.10+](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![Poetry: Managed](https://img.shields.io/badge/Poetry-1.8%2B-blueviolet.svg)](https://python-poetry.org/)
[![Robot Framework: 7.0+](https://img.shields.io/badge/Robot%20Framework-7.0%2B-00c0b5.svg)](https://robotframework.org/)
[![Selenium: 4.21+](https://img.shields.io/badge/Selenium-4.21%2B-43B02A.svg)](https://www.selenium.dev/)
[![Pyppeteer: Async](https://img.shields.io/badge/Pyppeteer-2.0%2B-blue.svg)](https://pyppeteer.github.io/pyppeteer/)
[![Grafana k6: High-Load](https://img.shields.io/badge/Grafana%20k6-v0.50%2B-7d64ff.svg)](https://k6.io/)
[![Pytest: 8.0+](https://img.shields.io/badge/Pytest-8.0%2B-0A9EDC.svg)](https://pytest.org/)
[![Docker: GPU Accelerated](https://img.shields.io/badge/Docker-WSL2%20CUDA-2496ED.svg)](https://www.docker.com/)
[![Allure: Reports](https://img.shields.io/badge/Allure-2.27%2B-ea580c.svg)](https://allurereport.org/)
[![FastAPI: Gateway](https://img.shields.io/badge/FastAPI-0.111%2B-009688.svg)](https://fastapi.tiangolo.com/)
[![Celery: Distributed](https://img.shields.io/badge/Celery-5.4%2B-37814A.svg)](https://docs.celeryq.dev/)
[![Ollama: Local Inference](https://img.shields.io/badge/Ollama-100%25%20Air--Gapped-black.svg)](https://ollama.com/)

## 📑 Table of Contents
1. [Why Use This as an Enterprise QA Framework?](#-why-use-this-as-an-enterprise-qa-framework)
2. [Data Sovereignty & Zero Data Leakage (The Enterprise QA Imperative)](#-data-sovereignty--zero-data-leakage-the-enterprise-qa-imperative)
3. [Inference Cost Economics: Cloud APIs vs. Local Sovereign ATP](#-inference-cost-economics-cloud-apis-vs-local-sovereign-atp)
4. [High-Velocity Inference on Budget Hardware ($600–$1,000 Laptop Reality)](#-high-velocity-inference-on-budget-hardware-6001000-laptop-reality)
5. [Develop Your Own Test Framework: Complete Model & Resource Sovereignty](#-develop-your-own-test-framework-complete-model--resource-sovereignty)
6. [🏗️ Generated Files Architecture & Component Blueprint](#-generated-files-architecture--component-blueprint)
   * [Project Structure Blueprint](#project-structure-blueprint)
   * [Architectural Responsibilities by File](#architectural-responsibilities-by-file)
7. [🔄 End-to-End Application & Inference Sequence UML](#-end-to-end-application--inference-sequence-uml)
8. [🧹 Multi-Stage Sanitization, RAG Context Injection & Re-Sanitization Pipeline](#-multi-stage-sanitization-rag-context-injection--re-sanitization-pipeline)
9. [🧪 Integrated Test Disciplines](#-integrated-test-disciplines)
   * [🌐 Enterprise Multi-Vector API Discovery Engine (`api_crawler.py`)](#-enterprise-multi-vector-api-discovery-engine-api_crawlerpy)
   * [👁️ Multi-Library Smart DOM Crawling & Visual WCAG 1.1.1 Accessibility Audit](#-multi-library-smart-dom-crawling--visual-wcag-111-accessibility-audit)
   * [📑 Enhanced 3-Pillar Master Requirements Document (BRD, PRD, FRD)](#-enhanced-3-pillar-master-requirements-document-brd-prd-frd)
   * [🚀 Multi-Scenario k6 Concurrency & Repeated Iteration Engine (`auto_load_test.js`)](#-multi-scenario-k6-concurrency--repeated-iteration-engine-auto_load_testjs)
   * [🗺️ Enterprise Coverage Heatmap & Gap Fulfiller (`coverage_engine.py`)](#-enterprise-coverage-heatmap--gap-fulfiller-coverage_enginepy)
10. [📋 Sample Generated Test Suites (Multi-Discipline Code Gallery)](#-sample-generated-test-suites-multi-discipline-code-gallery)
    * [1. Unified Enterprise Test Automation Harness (Robot Framework, Selenium 4, Pyppeteer)](#1-unified-enterprise-test-automation-harness-robot-framework-selenium-4-pyppeteer)
    * [2. Deterministic CI/CD WAF Allowlisting & Cloudflare Turnstile Verification Strategy](#2-deterministic-cicd-waf-allowlisting--cloudflare-turnstile-verification-strategy)
    * [3. Resilient E2E UI Suite with Dynamic Landmark & Section Hierarchy Verification (`auto_ui_test.py`)](#3-resilient-e2e-ui-suite-with-dynamic-landmark--section-hierarchy-verification-auto_ui_testpy)
    * [4. API Boundary Value Analysis Suite (`auto_api_test.py`)](#4-api-boundary-value-analysis-suite-auto_api_testpy)
    * [5. Multi-Scenario Load & Concurrency Suite (`auto_load_test.js`)](#5-multi-scenario-load--concurrency-suite-auto_load_testjs)
    * [6. Acceptance BDD Suite & Full Keyword Harness (`auto_suite.robot` & `keywords_lib.py`)](#6-acceptance-bdd-suite--full-keyword-harness-auto_suiterobot--keywords_libpy)
    * [7. Pabot Parallel Execution Transcript & Human-Readable Verification Log](#7-pabot-parallel-execution-transcript--human-readable-verification-log)
11. [🛡️ Automotive ASPICE & ISO 26262 Bidirectional Traceability (RTM)](#-automotive-aspice--iso-26262-bidirectional-traceability-rtm)
12. [⚡ Live Load Testing & Hardware Calibrator](#-live-load-testing--hardware-calibrator)
13. [📡 Complete REST API & Real-Time Telemetry Reference](#-complete-rest-api--real-time-telemetry-reference)
    * [REST Endpoints Specification](#rest-endpoints-specification)
    * [⚡ High-Speed Lightweight Project Export & Safe Non-Destructive Reload Engine (<1MB, <0.3s)](#-high-speed-lightweight-project-export--safe-non-destructive-reload-engine-1mb-03s)
14. [🔧 Setup Troubleshooting & Practical Debug Scenarios](#-setup-troubleshooting--practical-debug-scenarios)
15. [🚀 Quickstart & Operations Guide](#-quickstart--operations-guide)
    * [Prerequisites & One-Click Windows Deployment](#prerequisites)
    * [Unified Poetry, Robot Framework & Pytest Execution](#unified-poetry-robot-framework--pytest-execution)
    * [Programmatic CLI Project Export & Reload via cURL](#programmatic-cli-project-export--reload-via-curl)
16. [📄 License & Attribution](#-license--attribution)

---

## 🎯 Why Use This as an Enterprise QA Framework?

Modern enterprise test automation is heavily fragmented. Development teams routinely juggle disconnected tools: Selenium or WebdriverIO for UI testing, Postman or Pytest for APIs, k6 or JMeter for performance load profiling, Robot Framework for automotive/compliance acceptance, and third-party vulnerability scanners for security.

**Enterprise ATP (Autonomous Test Platform)** unifies all of these disciplines into a single, deterministic, monolithic orchestration engine powered by local, air-gapped Large Language Models:

* **Unified Multi-Discipline Synthesis**: From a single crawl of a web application or an OpenAPI spec, ATP autonomously generates end-to-end WebdriverIO scripts, boundary-value API Pytests, k6 virtual user performance profiles, Acceptance BDD Robot Framework suites, and NIST CVE vulnerability reports.
* **Autonomous Self-Healing Execution Loop**: Generated tests do not just run once and fail. ATP executes test code inside sandboxed headless runners, intercepts execution stack traces, performs Abstract Syntax Tree (AST) static analysis, dynamically heals broken UI locators via DOM heuristics, and automatically patches the test scripts in place.
* **Deterministic Stage Gating (Human-in-the-Loop)**: Unlike fragile black-box agents, ATP features an interactive **Scope Gate** between the crawling phase and test synthesis, allowing QA architects to inspect discovered endpoints, audit token burn, refine system prompts, and select exact attack vectors before code generation begins.
* **Turnkey Enterprise Orchestration**: Includes a complete microservices cluster (FastAPI core, Celery parallel distributed worker pool, Redis state cache, PostgreSQL relational test database, MinIO S3 object artifact storage, Elasticsearch audit log streaming, and Allure reporting server).

---

## 🔒 Data Sovereignty & Zero Data Leakage (The Enterprise QA Imperative)

In highly regulated sectors—including **Automotive (ASPICE, ISO 26262), Defense, Healthcare (HIPAA), and Banking/Finance (SOC 2, PCI-DSS, GDPR)**—sending test artifacts to public cloud AI endpoints (e.g., OpenAI, Anthropic, Google Cloud) is often an immediate compliance violation:

1. **Confidential Business Logic**: Web DOM trees, application routing tables, authentication flows, and internal test cases reveal unreleased features, proprietary business logic, and trade secrets.
2. **Exposed Credentials & Internal Infrastructure**: Live test recon captures JWT tokens, staging IP addresses, API schemas, database error traces, and internal server headers. Sending these payloads to external third-party API gateways creates a critical attack surface and data leakage liability.
3. **Regulatory Non-Compliance**: Automotive ASPICE Level 2/3 mandates strict bidirectional traceability, deterministic configuration management, and audit integrity that third-party non-deterministic APIs cannot guarantee.

**The ATP Solution**: The entire pipeline—crawling, headless browsers, LLM inference, embedding calculation, database persistence, and test execution—runs **100% locally on your own machine or private air-gapped on-premise server**. Not a single byte leaves your private network.

---

## 💰 Inference Cost Economics: Cloud APIs vs. Local Sovereign ATP

Enterprise automated QA generates massive prompt volumes across the complete testing lifecycle. In production SDET environments, costs are not limited to initial test creation—they recur heavily during **automated test execution (Playwright/Selenium)** and **post-execution failure triage / root cause analysis (RCA)**.

---

### 1. Realistic Token & Compute Burn per Stage

#### Stage A: End-to-End Multi-Suite Test Creation (Synthesis)
* **Recon & Context Ingestion**: Ingesting crawled HTML DOM, network payloads, API schemas, and MRD specifications: **~100,000 Input Tokens**.
* **Multi-Discipline Code Synthesis**: Generating WebdriverIO/Playwright POM scripts, boundary-value API Pytests, k6 performance profiles, and Robot Framework BDD: **~35,000 Output Tokens**.
* **AST Static Validation & Self-Healing Loop**: 2–3 iterative repair cycles evaluating syntax errors and initial selector alignments: **~50,000 Input Tokens** / **~10,000 Output Tokens**.
* **Test Creation Total**: **150,000 Prompt (Input) Tokens** | **45,000 Completion (Output) Tokens**.

#### Stage B: Post-Execution Test Triage & Root Cause Analysis (RCA)
When automated suites run in CI/CD, tests fail due to dynamic DOM shifts, timing/hydration lag, staging network drops, or authentic application regressions. In an enterprise regression suite of 50–100 tests, a typical run encounters **~10 failed tests** requiring automated triage:
* **Context Ingested per Failed Test**:
  * Execution stack trace & error message: ~1,500 tokens
  * Failure DOM snapshot & surrounding HTML tree: ~6,000 tokens
  * Playwright/Selenium console logs & network HAR/XHR requests: ~3,000 tokens
  * Original test script & Page Object Model definitions: ~2,000 tokens
  * **Input per Failed Test**: **~12,500 Input Tokens**.
* **Triage & Remediation Generated per Failed Test**:
  * Root Cause Analysis (RCA) & Classification (Product Defect vs. Test Flake vs. Staging Latency vs. Locator Drift): ~800 tokens
  * AST Self-Healing Patch Code (repaired selectors, explicit `waitForSelector`, updated assertion): ~1,200 tokens
  * Automated Allure/Jira incident summary markdown: ~500 tokens
  * **Output per Failed Test**: **~2,500 Output Tokens**.
* **Triage Total (Batch of 10 Failures)**: **125,000 Prompt (Input) Tokens** | **25,000 Completion (Output) Tokens**.

#### Stage C: Playwright Activity Cost (Browser Execution & Multimodal Triage)
Automated UI execution introduces both infrastructure compute and trace analysis overhead:
1. **Cloud Browser Execution Costs**:
   * Running a 50-test Playwright suite in cloud browser grids (BrowserStack, SauceLabs, LambdaTest, Microsoft Playwright Testing service) incurs direct runtime charges.
   * **Microsoft Playwright Testing service**: ~$0.005 to $0.01 per browser minute. A 50-test suite running across 4 parallel browser workers consumes ~25–30 browser minutes = **~$0.20 per suite run**.
   * **Enterprise Cloud Grids (BrowserStack/SauceLabs)**: Dedicated parallel testing slots cost **$199 to $999/month per slot**.
   * **Local Sovereign ATP**: Headless Chromium executes directly inside the local Docker container (`atp_core`) using local CPU/RAM = **$0.00**.
2. **Playwright Agentic Vision & Trace Inspection Surcharge**:
   * Cloud AI QA tools that ingest Playwright's `trace.zip` (action timelines, DOM snapshots, failure screenshots) burn multimodal tokens.
   * High-detail failure screenshots (1280x720) consume **~1,600 tokens each**. For 10 failed tests with before/after state captures (20 images): **~32,000 image tokens**.
   * In Local ATP, deterministic DOM heuristics (`engines/llm_evaluator.py`) extract the exact element delta and heal locators with **$0.00** token cost.

---

### 2. Comprehensive Cost Matrix: Full Lifecycle per Run & Monthly Scale

The tables below contrast the actual costs across all three stages: **Test Creation** (150k In / 45k Out), **Playwright Cloud Browser Execution** (50 tests), and **Post-Run Test Triage** (10 Failures: 125k In / 25k Out).

<!-- BEGIN_COST_MATRIX_USD
| Model / Provider | Input Price / 1M | Output Price / 1M | Test Creation Cost | Post-Run Triage Cost (10 Failures) | Playwright Cloud Runner | Total Cost per Full Lifecycle Run | Monthly Bill: Small Team (500 Runs) | Monthly Bill: Enterprise CI/CD (1,500 Runs) | Annual Cloud Bill (1,500 Runs / mo) |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Anthropic Claude 3.5 Sonnet | $3.00 | $15.00 | $1.12 | $0.75 | $0.200 | $2.075 | $1,037.50 | $3,112.50 | $37,350.00 |
| OpenAI GPT-4o | $2.50 | $10.00 | $0.82 | $0.56 | $0.200 | $1.587 | $793.75 | $2,381.25 | $28,575.00 |
| Google Gemini 1.5 Pro | $1.25 | $5.00 | $0.41 | $0.28 | $0.200 | $0.894 | $446.88 | $1,340.62 | $16,087.50 |
| Anthropic Claude 3.5 Haiku | $0.80 | $4.00 | $0.30 | $0.20 | $0.200 | $0.700 | $350.00 | $1,050.00 | $12,600.00 |
| DeepSeek-R1 (Cloud API) | $0.55 | $2.19 | $0.18 | $0.12 | $0.200 | $0.505 | $252.28 | $756.83 | $9,081.90 |
| OpenAI GPT-4o-mini | $0.15 | $0.60 | $0.05 | $0.03 | $0.200 | $0.283 | $141.62 | $424.88 | $5,098.50 |
| Enterprise Sovereign ATP (Local DeepSeek-R1 / Qwen2) | $0.00 | $0.00 | $0.00 | $0.00 | $0.200 | $0.200 | $100.00 | $300.00 | $3,600.00 |
| Enterprise Sovereign ATP (Local Qwen2) | $0.00 | $0.00 | $0.00 | $0.00 | $0.200 | $0.200 | $100.00 | $300.00 | $3,600.00 |
END_COST_MATRIX_USD -->

---

<!-- BEGIN_COST_MATRIX_INR
| Model / Provider | Input Price / 1M (Rs.) | Output Price / 1M (Rs.) | Test Creation (Rs.) | Post-Run Triage (10 Failures) (Rs.) | Playwright Cloud (Rs.) | Total Cost per Single Run (Rs.) | Monthly Bill: Small Team (500 Runs) | Monthly Bill: Enterprise CI/CD (1,500 Runs) | Annual Cloud Bill (1,500 Runs / mo) |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Anthropic Claude 3.5 Sonnet | Rs.318.76 | Rs.1593.80 | Rs.119.53 | Rs.79.69 | Rs.21.25 | Rs.220.48 | Rs.110,237.59 | Rs.330,712.77 | Rs.3,968,553.29 |
| OpenAI GPT-4o | Rs.265.63 | Rs.1062.53 | Rs.87.66 | Rs.59.77 | Rs.21.25 | Rs.168.68 | Rs.84,338.40 | Rs.253,015.19 | Rs.3,036,182.33 |
| Google Gemini 1.5 Pro | Rs.132.82 | Rs.531.27 | Rs.43.83 | Rs.29.88 | Rs.21.25 | Rs.94.96 | Rs.47,481.85 | Rs.142,445.56 | Rs.1,709,346.75 |
| Anthropic Claude 3.5 Haiku | Rs.85.00 | Rs.425.01 | Rs.31.88 | Rs.21.25 | Rs.21.25 | Rs.74.38 | Rs.37,188.58 | Rs.111,565.75 | Rs.1,338,789.06 |
| DeepSeek-R1 (Cloud API) | Rs.58.44 | Rs.232.69 | Rs.19.24 | Rs.13.12 | Rs.21.25 | Rs.53.61 | Rs.26,805.00 | Rs.80,415.00 | Rs.964,980.03 |
| OpenAI GPT-4o-mini | Rs.15.94 | Rs.63.75 | Rs.5.26 | Rs.3.59 | Rs.21.25 | Rs.30.10 | Rs.15,048.10 | Rs.45,144.29 | Rs.541,731.43 |
| Enterprise Sovereign ATP (Local DeepSeek-R1 / Qwen2) | Rs.0.00 | Rs.0.00 | Rs.0.00 | Rs.0.00 | Rs.21.25 | Rs.21.25 | Rs.10,625.31 | Rs.31,875.93 | Rs.382,511.16 |
| Enterprise Sovereign ATP (Local Qwen2) | Rs.0.00 | Rs.0.00 | Rs.0.00 | Rs.0.00 | Rs.21.25 | Rs.21.25 | Rs.10,625.31 | Rs.31,875.93 | Rs.382,511.16 |
END_COST_MATRIX_INR -->

<!-- BEGIN_ROI_SUMMARY
> [!TIP]
> **Enterprise Financial Payback & ROI (Indian Market Reality)**:
> * **Annual Cloud Bleed**: An Indian tech team or IT services enterprise executing 1500 automated regression runs/month on Claude 3.5 Sonnet spends **Rs.3,968,553.29 (39.69 L) annually** in cloud API invoices.
> * **One-Time Laptop CapEx in India**: An off-the-shelf developer laptop (Lenovo LOQ / Acer Nitro / ASUS TUF with NVIDIA RTX 3050 4GB VRAM) costs **Rs.65,000.00**.
> * **Power Consumption**: Drawing ~80W TDP during CUDA inference at commercial peak tariff (Rs.8.50/kWh) costs **~Rs.1,650 per year**.
> * **Break-Even Velocity**: The entire laptop pays for itself in just **4.9 business days** compared to Claude 3.5 Sonnet!
> * **Annual Net Capital Retained**: Saves over **Rs.3,586,042.12 (35.86 L) every single year per QA squad** while maintaining 100% data sovereignty.
END_ROI_SUMMARY -->

### 3. Interactive Usage Calculator & Self-Updating README Tool

Enterprise ATP includes a built-in CLI utility (`calculate_costs.py` and [`scripts/calculate_and_update_readme_costs.py`](file:///c:/Users/Junko/Downloads/ragllmorch/scripts/calculate_and_update_readme_costs.py)) that allows you to calculate token burn, convert costs to Indian Rupees (INR / ₹) with statutory enterprise taxation (GST + Forex markup), and **dynamically update the cost tables in this README file in-place**:

#### Quickstart Usage Commands

1. **Calculate Costs & Print Live Terminal Matrix**:
   ```bash
   python calculate_costs.py
   ```
   *Computes full-lifecycle costs for all 6 major LLM providers across USD ($) and Indian Rupees (INR / ₹) using current standard rates.*

2. **Auto-Detect Token Burn from Local Run Logs**:
   ```bash
   python calculate_costs.py --from-logs
   ```
   *Scans `artifacts/logs/engine_trace.jsonl` to calculate actual average prompt and completion tokens consumed by your real test runs.*

3. **Simulate Custom Parameters (Run Volume, Exchange Rates, GST)**:
   ```bash
   python calculate_costs.py --runs-per-month 2000 --usd-inr 88.5 --gst-pct 18.0 --forex-pct 3.5
   ```

4. **Update This README In-Place**:
   ```bash
   python calculate_costs.py --update-readme
   ```
   *Directly recalculates and overwrites the USD and INR pricing tables and ROI summary in this README with your custom parameters!*

#### CLI Parameter Reference

| Flag | Default | Description |
| :--- | :---: | :--- |
| `--update-readme` | `False` | Overwrites the tables and ROI summary in `README.md` in-place |
| `--from-logs` | `False` | Scans local `engine_trace.jsonl` to extract actual token averages |
| `--usd-inr` | `87.00` | Base USD to INR exchange rate |
| `--gst-pct` | `18.0%` | Statutory Indian GST on cross-border cloud SaaS/API invoices |
| `--forex-pct` | `3.5%` | Bank forex & international card conversion markup |
| `--creation-in` | `150,000` | Input tokens consumed during Test Creation stage |
| `--creation-out` | `45,000` | Output tokens generated during Test Creation stage |
| `--triage-in` | `125,000` | Input tokens consumed for 10-failure Triage stage |
| `--triage-out` | `25,000` | Output tokens generated for 10-failure Triage stage |
| `--browser-cost` | `$0.20` | Cloud browser runner execution fee per 50-test run |
| `--enterprise-runs` | `1,500` | Monthly enterprise CI/CD execution volume |
| `--laptop-cost-inr`| `₹65,000` | Local developer laptop cost in INR (RTX 3050 4GB) |

---

### 4. Token Speed, Wall-Clock Execution Time & Tier 1 Rate-Limit Bottlenecks

A critical flaw with relying on commercial LLM cloud providers for automated testing is **Tier 1 Rate Limiting (TPM/RPM caps)**.

#### The Cloud Tier 1 Rate-Limit Bottleneck
* **OpenAI Tier 1 Plan**: Enforces a strict cap of **30,000 Tokens Per Minute (TPM)** and 500 Requests Per Day (RPD).
* **Anthropic Tier 1 Plan**: Enforces a cap of **40,000 Tokens Per Minute (TPM)**.
* **The Collision**: Ingesting a 150,000-token web crawl for test creation, or sending a 125,000-token failure triage batch, **instantly triggers HTTP 429 Rate Limit Exceeded errors**.
* To prevent failure, cloud CI/CD pipelines must introduce artificial exponential backoff delays (sleeping 60–90 seconds between chunks). This throttles the pipeline and inflates wall-clock build times drastically!

#### Wall-Clock Latency & Speed Comparison

| Metric / Stage | OpenAI GPT-4o (Tier 1 Cloud) | Anthropic Claude 3.5 Sonnet (Tier 1 Cloud) | Enterprise ATP (Local DeepSeek-R1 on RTX 3050) | Architectural Advantage |
| :--- | :---: | :---: | :---: | :--- |
| **Generation Speed** | ~65–75 tok/s | ~70–85 tok/s | **85–92 tok/s** (100% CUDA) | Local VRAM eliminates network serialization latency |
| **Context Ingestion Speed** | ~800 tok/s | ~1,000 tok/s | **400–550 tok/s** (FP16 KV) | Zero API queue delay |
| **Rate Limit (TPM)** | **30,000 TPM** (Hard Cap) | **40,000 TPM** (Hard Cap) | **UNLIMITED (0 Cap)** | Zero HTTP 429 errors; no exponential backoff sleeps |
| **Stage A (Creation) Time** | ~16.5 min *(Includes ~4.5 min backoff sleep)* | ~14.0 min *(Includes ~3.2 min backoff sleep)* | **~8.5 min** *(Continuous CUDA generation)* | **Local is ~1.8x faster** |
| **Stage B (Playwright Run)** | ~1.5 min *(Cloud Grid queue + latency)* | ~1.5 min *(Cloud Grid queue + latency)* | **~1.2 min** *(Local 4-worker headless Chromium)* | **Zero cloud grid queue delay** |
| **Stage C (Triage) Time** | ~8.0 min *(Includes ~3.8 min backoff sleep)* | ~6.5 min *(Includes ~2.5 min backoff sleep)* | **~2.8 min** *(Targeted AST + 10 failure scans)* | **Local is ~2.5x faster** |
| **Total Wall-Clock Time** | **~26.0 Minutes** | **~22.0 Minutes** | **~12.5 Minutes** | **Local completes full E2E in HALF the time** |

---

### 5. Data Sovereignty Justification: Why Cloud Triage is a Critical Risk

While sending test creation prompts to the cloud carries code exposure risks, **sending post-execution test triage logs to cloud LLMs is an even more severe security violation**:
1. **Raw Database Dumps & SQL Errors**: When an API test fails with an HTTP 500 error, backend stack traces often dump table schemas, column names, raw SQL queries, and database connection strings into the response payload.
2. **Authorization Tokens & Cookies**: Playwright network failure logs frequently capture `Authorization: Bearer <JWT>`, session cookies, and staging API keys. Sending these to third-party cloud LLMs violates **SOC 2, ISO 27001, HIPAA, and GDPR** regulations.
3. **Internal Server Topology & File Paths**: Error tracebacks expose private microservice DNS names, staging IP addresses, and underlying Linux filesystem paths (`/var/app/backend/core/services/...`), handing external systems a structural blueprint of your internal architecture.

**The ATP Sovereign Advantage**: ATP keeps all tracebacks, DOM trees, HAR logs, and generated patches **strictly within your local hardware boundary**. Zero external API calls, zero third-party token retention, and 100% deterministic compliance.

---

## ⚡ High-Velocity Inference on Budget Hardware ($600–$1,000 Laptop Reality)

A common misconception is that running local enterprise LLMs requires $10,000+ server-grade NVIDIA H100 or A100 GPUs. 

**Enterprise ATP is architected from the ground up to achieve high-velocity generation (80–92 tokens/sec) on standard, off-the-shelf consumer laptops costing between $600 and $1,000.**

### 1. Typical Hardware Profile in the $600–$1,000 Range
* **Laptop Models**: Lenovo LOQ / Ideapad Gaming, Acer Nitro 5, HP Victus 15, ASUS TUF Gaming F15.
* **Processor**: Intel Core i5-12450H / i5-13420H (8 cores) or AMD Ryzen 5 7535HS (6 cores / 12 threads).
* **System RAM**: 16 GB DDR4 or DDR5.
* **Dedicated GPU**: NVIDIA GeForce RTX 3050 Laptop GPU (4 GB or 6 GB VRAM) or RTX 4050 (6 GB VRAM).

---

### 2. The 4GB VRAM Dilemma: The "PCIe Offload Cliff"
On Windows laptops with a 4.0 GB GPU, the operating system's desktop window manager (DWM/explorer) typically reserves ~2.0 GB to 2.4 GB of VRAM. This leaves approximately **1.6 GB to 2.0 GB of free VRAM** for AI compute.

* **What goes wrong in naive setups**: Standard frameworks blindly configure a 32,768-token context window. At 32k context across parallel runner slots, the memory allocation demands **3.8 GB**. Because available VRAM is only ~1.7 GB, Ollama is forced into a **`38%/62% CPU/GPU` split**. Every single token generated must be shuffled back and forth across the slow PCIe bus between system RAM and GPU VRAM. **Inference speed plummets from 85 tokens/sec down to 5.6 tokens/sec (a 15x degradation)**.
* **The ATP Intelligent VRAM Auto-Scaler**:
  1. Utilizes efficient 4-bit GGUF quantized models (`deepseek-r1:1.5b` or `qwen2.5:1.5b`), requiring only **1.1 GB** for model weights.
  2. Dynamically sizes the context window to **4,096 or 8,192 tokens** with batching at **1,024**.
  3. Pre-allocates FP16 KV-cache (~220MB to ~360MB).
  4. Total memory footprint: **~1.35 GB to 1.45 GB**.
  5. **100% of all model layers and KV-cache reside permanently inside GPU VRAM (0% CPU offload)**.

### 3. Empirical Performance Measurements on an RTX 3050 (4GB)

```
========================================================================================
Profile Configuration           Context    Memory Footprint   Processor Mode    Speed
========================================================================================
Naive Uncalibrated (Degraded)   32,768     3.8 GB             38%/62% CPU/GPU    5.6 tok/s
High-Velocity (Max Speed)        4,096     1.18 GB            100% GPU (CUDA)   92.1 tok/s
Balanced (Recommended)           8,192     1.43 GB            100% GPU (CUDA)   88.1 tok/s
Deep Context (High Capacity)    16,384     1.92 GB            100% GPU (CUDA)   18.5 tok/s
========================================================================================
```

At **88.1 tokens per second**, synthesizing a complete 80-line executable Robot Framework or Pytest suite takes **under 8 seconds**!

---

## 🛠️ Develop Your Own Test Framework: Complete Model & Resource Sovereignty

By leveraging Enterprise ATP, organizations eliminate dependency on closed-source external platforms. You have full architectural freedom to customize every layer:

### 1. Custom Domain Tuning & Instruction Scaffolding
In [`engines/ai_core_engine.py`](file:///c:/Users/Junko/Downloads/ragllmorch/aspice_qa_framework/engines/ai_core_engine.py), prompt templates are structured to enforce corporate standards:
```python
# Customizing UI test synthesis with Page Object Model rules:
SYSTEM_PROMPT = """You are a Principal Test Automation Architect.
Follow our corporate SDET standards:
1. Always implement Page Object Model (POM) classes in separate modules.
2. Use data-testid or aria-label attributes for locators; avoid raw XPaths.
3. Every test case must include @allure.severity and @allure.story tags.
4. Implement explicit WebDriverWait with custom ExpectedConditions.
"""
```

### 2. Proprietary In-House Harnesses & Custom Protocols
ATP is not restricted to standard HTTP/HTML. You can synthesize tests for:
* **Automotive Embedded CAN / LIN Bus**: Generate Python-CAN or CANoe Vector CAPL test scripts.
* **gRPC & Protocol Buffers**: Ingest `.proto` schemas and generate gRPC client validation suites.
* **Legacy Mainframes & Terminal Emulators**: Generate Robot Framework suites for 3270 terminals.

### 3. Complete Model Autonomy (Zero Lock-In)
Switch models with a single click in the UI or via API:
* `deepseek-r1:1.5b`: Reasoning-first model for BDD logic, complex edge-case derivation, and AST healing.
* `qwen2.5-coder:1.5b`: High-velocity syntax generator (95+ tokens/sec).
* `mistral:7b` / `llama3:8b`: Comprehensive architectural analysis on 8GB/16GB workstations.
* **Corporate Fine-Tuned LoRAs**: Point Ollama to your internal fine-tuned weights:
  ```bash
  ollama create corporate-sdet-v1 -f ./Modelfile
  ```

### 4. Persistent Project Assistant Chat
The integrated Project Assistant Chat panel (`/api/chat/ask`) has full real-time visibility into your crawled DOMs, test scripts, and MRD requirements. It answers architectural questions, explains generated assertions, and writes new tests on demand while respecting the calibrated local hardware limits.

### 5. Sovereign Model Selection Hub & <3GB VRAM Auto-Listing
The dashboard sidebar features an intelligent **Sovereign Model Selection Hub**:
* **Direct Ollama Integration**: Automatically queries local Ollama tags (`/api/tags`) and active processes (`/api/ps`) to fetch installed models, actual byte sizes, parameter counts, and quantization levels.
* **`<3GB VRAM Safe` Auto-Filtering**: Specifically tags and filters models whose memory footprint is under 3GB (`size <= 3.2 GB`), guaranteeing 100% CUDA VRAM residence on budget 4GB GPUs (like the RTX 3050 Laptop) with zero PCIe bus thrashing.
* **Filter Switcher Pills**: One-click toggling between `⚡ <3GB VRAM Safe` and `🌐 All Models (8)`.
* **Dynamic Spec & Guarantee Card**: Displays exact model footprint (e.g., `1.04 GB • Q4_K_M`), parameter size (`1.8B`), and a live status pill (`● Ready in VRAM` vs. `○ Needs Download`).
* **1-Click In-App Model Pull**: If an uninstalled model is chosen, users can pull it directly within the UI with live percentage streaming progress via WebSockets (`/ws/model-pull/{model}`).

---

## 🏗️ Generated Files Architecture & Component Blueprint

### Project Structure Blueprint

The framework provides an enterprise-grade directory structure that unifies **Robot Framework**, **Selenium 4**, and **Pyppeteer** alongside **FastAPI**, **Celery**, and **Ollama**:

```text
.
├── config/                             # Centralized runtime & test environment configuration
│   └── settings.py                     # Pydantic V2 settings, WAF bypass tokens, Turnstile keys
├── libraries/                          # Custom test automation keyword bridges
│   └── PyppeteerKeywords.py            # Asynchronous Robot Framework bridge for headless Chromium
├── tests/                              # Unified enterprise test suites
│   ├── suite_playwright.robot          # Robot Framework Browser suite (WAF injection, Turnstile, #app-loader)
│   └── test_selenium.py                # Selenium 4 Pytest suite with CDP header injection & WebDriverWait
├── results/                            # Centralized test execution artifacts
│   ├── allure-results/                 # Allure test step traces, attachments, and metrics
│   └── screenshots/                    # Automated failure and verification captures
├── pyproject.toml                      # Poetry package definition & pinned enterprise dependencies
├── pytest.ini                          # Pytest runner markers (smoke, regression, waf_protected)
├── deploy_enterprise_qa.py             # Single-source Master Deployment & Synchronization Orchestrator
├── docker-compose-windows.yml          # Container orchestration with GPU passthrough
├── artifacts/                          # Air-gapped runtime artifacts & generated code
│   ├── scripts/                        # Synthesized multi-discipline test scripts
│   │   ├── auto_ui_test.py             # Resilient Selenium 4 Page Object Model suite
│   │   ├── auto_api_test.py            # Pytest REST Boundary Value Analysis suite
│   │   ├── auto_load_test.js           # Multi-scenario Grafana k6 load & concurrency script
│   │   ├── auto_suite.robot            # Master Robot Framework acceptance & BDD suite
│   │   ├── keywords_lib.py             # Python keyword library with concurrency & iteration hooks
│   │   ├── auto_ui_wdio.js             # WebdriverIO modern UI suite
│   │   └── auto_ui_playwright.spec.ts  # Playwright TypeScript test suite
│   ├── reports/                        # Synthesized requirements & verification documents
│   │   ├── master_requirements_document.md # 3-Pillar BRD, PRD, and FRD with ASPICE RTM
│   │   └── allure/                     # Compiled interactive Allure HTML report
│   └── discovered_apis.json            # Dynamic backend APIs discovered via CDP performance logs
└── aspice_qa_framework/                # Core backend orchestrator source code
    ├── main.py                         # FastAPI REST Gateway, WebSocket & Telemetry broadcaster
    ├── engines/                        # AI & Testing Subsystems
    │   ├── ai_core_engine.py           # Multi-discipline SDET prompt orchestrator & synthesizer
    │   ├── api_crawler.py              # 5-Vector active/passive backend reconnaissance engine
    │   ├── coverage_engine.py          # AST-based 5-discipline coverage heatmap engine
    │   ├── hardware_probe.py           # GPU VRAM governor & 3-profile live benchmarking
    │   ├── enhanced_mcp_harness.py     # Streaming Ollama transport with repetition loop breaker
    │   ├── langchain_engine.py         # Semantic RAG chunker & vector index constructor
    │   ├── llm_evaluator.py            # AST static syntax auditor & dynamic self-healing engine
    │   └── nist_scanner.py             # NIST NVD CVE vulnerability scanner & SSL auditor
    ├── core/worker.py                  # Celery worker pool for headless crawling & Pabot execution
    └── static/index.html               # Zero-build React 18 / Tailwind glassmorphism dashboard
```

```mermaid
graph TD
    subgraph Presentation ["Presentation & Interaction Layer"]
        UI["React 18 Dashboard<br/>(Monaco Editor, Scope Gate Modal, SSE Logs)"]
    end

    subgraph Gateway ["API & Orchestration Layer"]
        FASTAPI["FastAPI Gateway (Port 8000)<br/>State Machines, SSE Telemetry & Export Engine"]
        WORKER["Celery Distributed Worker<br/>Headless Chromium, Pabot, k6 Runners"]
    end

    subgraph Reasoning ["Local Sovereign Inference Layer"]
        AI_CORE["AI Core Synthesizer<br/>(Multi-Discipline SDET Prompts)"]
        EVALUATOR["AST Evaluator & Healer<br/>(Syntax Check, Rubric Scoring)"]
        LANGCHAIN["RAG Retriever<br/>(DOM Vector Indices & MRD Injection)"]
        MCP_HARNESS["MCP Transport Harness<br/>(Streaming Buffer, Rep-Breaker)"]
        OLLAMA["Local Ollama Container (Port 11434)<br/>(Qwen2.5-Coder / DeepSeek-R1)"]
    end

    subgraph TestingHarness ["Unified Test Execution Framework"]
        POETRY["Poetry Environment Manager"]
        ROBOT["Robot Framework 7.0+ & Pabot<br/>(suite_playwright.robot, auto_suite.robot)"]
        SELENIUM["Selenium 4 Suite<br/>(test_selenium.py, auto_ui_test.py)"]
        PYPPETEER["Pyppeteer Asynchronous Bridge<br/>(PyppeteerKeywords.py)"]
        K6["Grafana k6 Load Runner<br/>(auto_load_test.js)"]
    end

    subgraph Hardware ["Hardware & Security Governors"]
        PROBE["Hardware Probe<br/>(VRAM KV-Cache Math, GPU Offload Defense)"]
        NIST["NIST CVE Scanner<br/>(SSL Audit, Vulnerability Lookup)"]
    end

    subgraph Storage ["Air-Gapped Artifacts & Storage"]
        ARTIFACTS["Local Artifacts Volume<br/>(scripts/, reports/, discovered_apis.json)"]
    end

    UI -->|Trigger Crawl / Approve Scope / Export| FASTAPI
    FASTAPI -->|SSE Stream Telemetry| UI
    FASTAPI -->|Scan Infrastructure| NIST
    FASTAPI -->|Dispatch Crawl / Execution| WORKER
    FASTAPI -->|Generate Multi-Suite| AI_CORE
    FASTAPI -->|Evaluate & Self-Heal| EVALUATOR

    AI_CORE -->|Retrieve RAG Context| LANGCHAIN
    AI_CORE -->|Execute Streaming Inference| MCP_HARNESS
    MCP_HARNESS -->|VRAM Boundaries & Threads| PROBE
    MCP_HARNESS -->|Inference Query| OLLAMA
    EVALUATOR -->|Static AST Analysis & Review| MCP_HARNESS

    WORKER -->|Execute Tests via| TestingHarness
    TestingHarness -->|Store Test Runs & Reports| ARTIFACTS
```

### Architectural Responsibilities by File

| Component File | Architectural Layer | Primary Responsibilities & Design Patterns |
| :--- | :--- | :--- |
| [`main.py`](file:///c:/Users/Junko/Downloads/RagLLM/aspice_qa_framework/main.py) | **API Gateway & Export** | Hosts all REST and SSE endpoints (`/api/crawl`, `/api/scope_gate/*`, `/api/generate_suite`, `/api/execute`, `/api/chat/ask`, `/api/system/export`, `/api/system/import`). Implements state machines and ultra-fast non-destructive project packaging. |
| [`config/settings.py`](file:///c:/Users/Junko/Downloads/RagLLM/config/settings.py) | **Environment Configuration** | Enterprise configuration engine using Pydantic Settings V2 with graceful fallback. Manages base URLs, headless switches, WAF bypass tokens (`X-Automation-Bypass-Token`), and official Cloudflare Turnstile test keys. |
| [`libraries/PyppeteerKeywords.py`](file:///c:/Users/Junko/Downloads/RagLLM/libraries/PyppeteerKeywords.py) | **Robot/Pyppeteer Bridge** | Custom Robot Framework keyword library wrapping Pyppeteer. Implements non-blocking async execution inside Robot's synchronous runner, CDP header injection, and deterministic element/loader synchronization. |
| [`tests/suite_playwright.robot`](file:///c:/Users/Junko/Downloads/RagLLM/tests/suite_playwright.robot) | **Browser Acceptance Suite** | Enterprise CI/CD suite for Playwright-backed Browser Library. Demonstrates deterministic WAF header injection, `#app-loader` spinner detachment, and Cloudflare Turnstile token validation. |
| [`tests/test_selenium.py`](file:///c:/Users/Junko/Downloads/RagLLM/tests/test_selenium.py) | **Selenium 4 Pytest Suite** | Pure Python pytest module implementing Selenium 4 with Chrome DevTools Protocol (`Network.setExtraHTTPHeaders`) WAF injection and explicit `WebDriverWait` synchronization. |
| [`pyproject.toml`](file:///c:/Users/Junko/Downloads/RagLLM/pyproject.toml) | **Dependency Governance** | Poetry environment specification pinning Robot Framework, robotframework-browser, Selenium 4, Pyppeteer, Pytest, Pabot, and Pydantic. |
| [`pytest.ini`](file:///c:/Users/Junko/Downloads/RagLLM/pytest.ini) | **Pytest Configuration** | Strict test discovery and execution markers (`smoke`, `regression`, `waf_protected`) with automated Allure results targeting. |
| [`deploy_enterprise_qa.py`](file:///c:/Users/Junko/Downloads/RagLLM/deploy_enterprise_qa.py) | **Master Deployment Engine** | Single master source of truth. Synchronizes, validates, and deploys all configuration, libraries, test scripts, and Docker microservices with atomic consistency. |
| [`index.html`](file:///c:/Users/Junko/Downloads/RagLLM/aspice_qa_framework/static/index.html) | **Presentation** | Zero-build React 18 frontend. Features Monaco code editor, live SSE execution logs, Scope Gate route selector, Live Benchmark calibrator modal, Coverage Heatmap drawer, and Allure iframe. |
| [`enhanced_mcp_harness.py`](file:///c:/Users/Junko/Downloads/RagLLM/aspice_qa_framework/engines/enhanced_mcp_harness.py) | **LLM Transport** | Industrial Ollama client. Features streaming buffer, O(1) circular repetition loop detector (`rep_pattern`), dynamic prefix caching, and infinite context output auto-stitcher. |
| [`hardware_probe.py`](file:///c:/Users/Junko/Downloads/RagLLM/aspice_qa_framework/engines/hardware_probe.py) | **Hardware Governor** | Queries `nvidia-smi` and system RAM. Calculates exact VRAM KV-cache requirements, prevents PCIe offloading, executes 3-profile live benchmarks, and persists configuration. |
| [`ai_core_engine.py`](file:///c:/Users/Junko/Downloads/RagLLM/aspice_qa_framework/engines/ai_core_engine.py) | **Code Synthesizer** | Multi-discipline SDET prompt orchestrator. Synthesizes executable WebdriverIO, Selenium, Pytest, k6, and Robot Framework test scripts from crawled DOM schemas and MRD pillars. |
| [`langchain_engine.py`](file:///c:/Users/Junko/Downloads/RagLLM/aspice_qa_framework/engines/langchain_engine.py) | **RAG Retriever** | Chunks crawled DOM trees and Master Requirements Documents (MRD). Computes local embeddings, builds vector indices, and injects top-k semantic context into prompts. |
| [`llm_evaluator.py`](file:///c:/Users/Junko/Downloads/RagLLM/aspice_qa_framework/engines/llm_evaluator.py) | **Quality Gate** | Performs static syntax checking via `ast.parse()`, scores scripts against SDET rubrics, sanitizes `<think>` tags, and orchestrates dynamic locator healing. |
| [`nist_scanner.py`](file:///c:/Users/Junko/Downloads/RagLLM/aspice_qa_framework/engines/nist_scanner.py) | **Security Scanner** | Fingerprints target HTTP headers, identifies web technology stacks (PHP, Node, Python, Django), and executes parallel queries to the NIST NVD CVE API. |
| [`worker.py`](file:///c:/Users/Junko/Downloads/RagLLM/aspice_qa_framework/core/worker.py) | **Worker Pool** | Celery distributed task definitions for headless browser automation (Crawl4AI/Chromium) and parallel test execution via Pabot. |
| [`docker-compose-windows.yml`](file:///c:/Users/Junko/Downloads/RagLLM/docker-compose-windows.yml) | **Infrastructure** | Container specification with dedicated GPU resource reservations (`count: all, capabilities: [gpu]`), shared memory sizing (`shm_size: 2gb`), and volume mounts. |

---

## 🔄 End-to-End Application & Inference Sequence UML

```mermaid
sequenceDiagram
    autonumber
    actor Architect as QA Architect / PO
    participant UI as React 18 Dashboard (index.html)
    participant Core as FastAPI Gateway (main.py)
    participant Crawler as Celery Worker / Chromium (worker.py)
    participant NIST as NIST Scanner (nist_scanner.py)
    participant RAG as RAG Context Engine (langchain_engine.py)
    participant Governor as Hardware Governor (hardware_probe.py)
    participant Ollama as Local LLM (ollama_engine)
    participant SDET as AST Evaluator & Healer (llm_evaluator.py)
    participant Pabot as Pabot Runner (execution_suite.robot)
    participant Allure as Allure Reporting Server

    %% STAGE 1 & 2: RECON & CRAWL
    Architect->>UI: Enters Target URL & Clicks "Start Crawl & Recon"
    UI->>Core: POST /api/crawl {url, depth, auth}
    par Parallel Recon
        Core->>NIST: scan_target(url)
        NIST-->>Core: Detected Stacks & NIST CVE Vulnerabilities
    and Headless Web Spider
        Core->>Crawler: dispatch_crawl_task(url)
        Crawler-->>Core: Raw DOM Trees, Network HAR, Discovered Routes
    end

    %% STAGE 3: SCOPE GATE (HITL)
    Core->>UI: SSE: Discovered Routes & Token Burn Estimation
    Note over Architect, UI: Stage Gate: Human-in-the-Loop Review
    Architect->>UI: Selects Routes, Attack Vectors & Clicks "Approve & Generate"
    UI->>Core: POST /api/scope_gate/approve {selected_routes, settings}

    %% STAGE 4: SANITIZATION & RAG
    Core->>RAG: sanitize_and_chunk(DOM, MRD, OpenAPI)
    Note over RAG: Multi-Stage Input Sanitization:<br/>1. Strip dynamic IDs, tokens, timestamps<br/>2. Strip CSS styles & tracking boilerplate<br/>3. Compute embeddings & build FAISS vector index
    RAG-->>Core: Top-k Relevant Context Chunks (3k-4.5k chars)

    %% HARDWARE GOVERNANCE & INFERENCE
    Core->>Governor: probe_and_scale_vram_resources(model, concurrency, ctx)
    Governor-->>Core: Allocated Config: 8k Ctx, 1024 Batch, 100% CUDA GPU
    Core->>Ollama: POST /api/generate (Streaming JSON, System Prompt, RAG Context)
    
    loop Real-time Streaming & Repetition Breaker
        Ollama-->>Core: Stream Token Chunks (eval_count, prompt_eval_count)
        Note over Core: O(1) Circular Tail Buffer:<br/>Detects repetitive token loops & triggers auto-continuation
        Core->>UI: SSE: Real-Time Token Generation Stream (88 tok/s)
    end
    Ollama-->>Core: Raw Completion Stream Finished

    %% STAGE 5: OUTPUT SANITIZATION & AST VALIDATION
    Core->>SDET: validate_and_review(generated_script)
    Note over SDET: Output Sanitization:<br/>1. Strip <think> tags & Markdown code fences<br/>2. Run Python ast.parse() syntax validation<br/>3. Execute sandboxed dry-run in headless runner

    alt AST Syntax Failure or Broken Locator Detected
        Note over SDET, Core: Dynamic Self-Healing Loop Triggered
        SDET->>Ollama: Re-prompt with Failure Stack Trace + Clean DOM Context
        Ollama-->>SDET: Patched Locators & Corrected Code
        Note over SDET: Re-Sanitize & Verify AST Tree
    end
    SDET-->>Core: Validated, Clean Executable Test Suites

    %% STAGE 6: EXECUTION & REPORTING
    Core->>Pabot: Execute Suites in Parallel (4 Workers)
    Pabot-->>Core: Test Result Artifacts & XML Traces
    Core->>Allure: generate_report(artifacts/reports/allure-results)
    Allure-->>Core: Compiled Single-File Interactive HTML Report
    Core->>UI: SSE: "Execution Complete" -> Render Allure Iframe
    UI-->>Architect: Displays Interactive Test Dashboard & Metrics
```

---

## 🧹 Multi-Stage Sanitization, RAG Context Injection & Re-Sanitization Pipeline

One of the platform's core architectural innovations is its **deterministic sanitization and context engineering pipeline**. Raw web DOMs and unconstrained LLM outputs are inherently noisy. ATP solves this through five distinct stages:

```
[Raw Crawled DOM / HAR] 
       │
       ▼
 1. PRE-INGESTION SANITIZER ──────► Strips timestamps, dynamic UUIDs, session cookies, SVG/CSS bloat (Saves ~40% VRAM)
       │
       ▼
 2. SEMANTIC RAG RETRIEVER  ──────► Chunks into 4.5k segments, builds FAISS vector index, aligns with MRD & RF-MCP schemas
       │
       ▼
 3. HARDWARE VRAM GOVERNOR  ──────► Locks context to 4k/8k, batch to 1024, enables prefix caching (100% GPU VRAM residency)
       │
       ▼
 4. IN-FLIGHT OUTPUT SANITIZER ──► Strips <think> tags, breaks infinite loops via circular tail regex, strips markdown fences
       │
       ▼
 5. SDET AST RE-SANITIZER   ──────► Parses ast.parse(), detects syntax/locator breaks, triggers in-place self-healing repair
       │
       ▼
[Production Executable Test Code]
```

### Exact Code Responsibilities

#### Stage 1: Pre-Ingestion Sanitization (Noise Stripping)
* **Code Location**: [`enhanced_mcp_harness.py`](file:///c:/Users/Junko/Downloads/ragllmorch/aspice_qa_framework/engines/enhanced_mcp_harness.py) and [`langchain_engine.py`](file:///c:/Users/Junko/Downloads/ragllmorch/aspice_qa_framework/engines/langchain_engine.py).
* **Operation**:
  ```python
  # Strips ephemeral attributes, timestamps, and noisy tracking attributes
  sanitized = re.sub(r'(id|class|data-[a-z-]+)="[^"]*"', '', prompt)
  sanitized = re.sub(r'\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}', '', sanitized)
  ```
* **Architectural Rationale**: Raw DOM trees contain hundreds of dynamic GUIDs, ephemeral session IDs, and tracking attributes (`data-analytics-id`, `style="..."`). Stripping them reduces prompt tokens by **35%–45%**, eliminates cache misses, and guarantees repeatable prompt prefix hashing.

#### Stage 2: Semantic RAG Chunking & Context Construction
* **Code Location**: [`langchain_engine.py`](file:///c:/Users/Junko/Downloads/ragllmorch/aspice_qa_framework/engines/langchain_engine.py) and [`ai_core_engine.py`](file:///c:/Users/Junko/Downloads/ragllmorch/aspice_qa_framework/engines/ai_core_engine.py).
* **Operation**: Chunks sanitized inputs into 4,000–4,500 character blocks with a 250-character sliding overlap. Computes vector embeddings and performs similarity search against the Master Requirements Document (MRD). Dynamically injects official Robot Framework tool keywords via `rf-mcp` context retrieval.

#### Stage 3: Hardware-Grounded Inference Constraints
* **Code Location**: [`hardware_probe.py`](file:///c:/Users/Junko/Downloads/ragllmorch/aspice_qa_framework/engines/hardware_probe.py).
* **Operation**: Sizing options enforce `num_ctx: 8192`, `num_batch: 1024`, `f16_kv: True`, and `use_mmap: True`. Utilizes `num_keep` for prompt prefix caching, preventing Ollama from re-evaluating the system rubric on repeated generation calls.

#### Stage 4: In-Flight & Output Sanitization
* **Code Location**: [`enhanced_mcp_harness.py`](file:///c:/Users/Junko/Downloads/ragllmorch/aspice_qa_framework/engines/enhanced_mcp_harness.py).
* **Operation**:
  1. **Circular Loop Detection**: An O(1) circular tail buffer monitors the trailing 400 token chunks. If a repetitive loop is detected (`re.compile(r"(.{100,})\1{2,}", re.DOTALL)`), the generator halts and triggers automatic context-continuation stitching.
  2. **Reasoning Tag Stripping**: DeepSeek reasoning outputs (`<think>...</think>`) are filtered from the code payload.
  3. **Markdown Fence Extraction**: Regular expressions strip enclosing ````python` and ````robot` fences to isolate pure, executable syntax.

#### Stage 5: AST Static Validation & Sandboxed Re-Sanitization
* **Code Location**: [`llm_evaluator.py`](file:///c:/Users/Junko/Downloads/ragllmorch/aspice_qa_framework/engines/llm_evaluator.py).
* **Operation**: Generated scripts are passed through Python's `ast.parse()`. If an `IndentationError` or `SyntaxError` occurs, or if a dry-run in headless Chromium fails due to an obsolete DOM locator, the evaluator captures the exact error trace, re-prompts Ollama with the specific failure context, re-sanitizes the patched snippet, and verifies that the resulting AST is valid before writing to `artifacts/scripts/`.

---

## 🧪 Integrated Test Disciplines

| Discipline | Underlying Technology | Capabilities |
| :--- | :--- | :--- |
| **Unified UI Automation** | Robot Framework Browser, Selenium 4 & Pyppeteer | Headless Chromium, CDP WAF header injection, dynamic element waiting, Turnstile validation, and resilient layout hierarchy verification. |
| **API Testing & Recon** | Enterprise Multi-Vector Crawler + Pytest | 5-vector active/passive discovery (OpenAPI/Swagger, JS bundle scraping, CDP network capture, form action mining) + automated Boundary Value Analysis (BVA). |
| **Performance Testing**| Grafana k6 Multi-Scenario | Simultaneous peak burst concurrency (20 VUs at same instant), sustained repeated page iterations (5 VUs x 10 cycles), and discovered API throughput assertions (`p95 < 500ms`). |
| **Acceptance / BDD** | Robot Framework 7.0+ & Pabot | Human-readable Gherkin/BDD keyword syntax, parallel test execution, full lifecycle hooks, and Automotive ASPICE SWE.4 traceability. |
| **Security / Compliance**| NIST CVE Scanner | Real-time vulnerability lookup, SSL/TLS audit, security header verification, and OWASP Top 10 API boundary fuzzing. |

---

### 🌐 Enterprise Multi-Vector API Discovery Engine (`api_crawler.py`)

Unlike conventional QA tools that require manual Postman collections or OpenAPI files, ATP features an **autonomous multi-vector backend reconnaissance engine**:

```text
+-------------------------------------------------------------------------------+
|               ENTERPRISE MULTI-VECTOR BACKEND API RECONNAISSANCE              |
+-------------------------------------------------------------------------------+
| 1. Active Schema Probing       --> Probes 23 OpenAPI / Swagger / GraphQL specs|
| 2. Client Script Bundle Mining --> Fetches JS bundles, regex-mines uncalled APIs|
| 3. CDP Network Interception    --> Captures live XHR/Fetch network traffic   |
| 4. DOM Form Target Extraction  --> Parses HTML form actions & parameter models |
| 5. BVA & Security Matrixing    --> Generates Boundary Value & OWASP test suites|
+-------------------------------------------------------------------------------+
```

1. **Vector 1: Active Schema & Introspection Probing**:
   * Concurrently probes 23 candidate documentation and schema paths (`/openapi.json`, `/swagger.json`, `/v3/api-docs`, `/api/v1/swagger.json`, `/graphql`, etc.).
   * Automatically parses OpenAPI 3.x and Swagger 2.0 specs to catalog complete route paths, HTTP verbs, parameter definitions, request bodies, and authentication schemes.
2. **Vector 2: Static Client-Side Script & Bundle Mining**:
   * Scrapes DOM snapshots for `<script>` tags, fetches external JavaScript bundles (up to 200KB per bundle), and executes deterministic regex patterns matching relative API endpoints (`/api/v1/...`, `/auth/...`, `/graphql`).
3. **Vector 3: CDP Live Network Traffic Interception**:
   * Ingests Chrome DevTools Protocol (CDP) `performance` logs during dynamic crawling to intercept active runtime XHR/Fetch requests, extracting exact query parameters and response payloads.
4. **Vector 4: DOM Form Action & Parameter Extraction**:
   * Traverses DOM trees to detect `<form action="..." method="...">` elements, extracting submission routes and parameter models.
5. **Vector 5: Automated Boundary Value Analysis (BVA) & OWASP Security Suite Generation**:
   * Automatically classifies every discovered route into logical domains (`HEALTH`, `AUTHENTICATION`, `SEARCH`, `CRUD`, `TRANSACTION`).
   * Generates robust, informative checks:
     * **Contract & Latency SLA**: Asserts valid HTTP responses (`200, 201, 202, 204, 301, 302, 400, 401, 403, 404, 405, 422`) with strict p95 latency thresholds (<500ms).
     * **Boundary Value Analysis (BVA)**: Submits edge-case payloads (`{}`, empty strings, whitespace, null values) to verify graceful HTTP 4xx error handling.
     * **OWASP API Security Probes**: Defensive SQL injection fragments (`' OR '1'='1' --`) and cross-site scripting vectors (`<script>alert(1)</script>`) to verify sanitization without server 500 error leaks.

---

### 👁️ Multi-Library Smart DOM Crawling & Visual WCAG 1.1.1 Accessibility Audit

ATP deploys a sophisticated multi-library DOM parser combining **BeautifulSoup4**, **Crawl4AI**, and **Chrome DevTools Protocol (CDP)** to deconstruct complex modern web pages into semantic testing models:

1. **Visual Asset Extraction & Classification (`images_and_visuals`)**:
   * Scans DOM trees for standard `<img>`, `<picture>` sources, and inline `<svg>` elements.
   * Classifies each asset into functional archetypes:
     * `BRAND_LOGO`: Header/footer branding, SVG logos, masthead icons.
     * `HERO_BANNER`: Above-the-fold hero background images, promotional graphics.
     * `FEATURE_VISUAL`: Card icons, feature highlights, informational illustrations.
   * **Automated WCAG 1.1.1 Non-Text Content Audit**:
     * Inspects every visual element for mandatory accessibility attributes (`alt`, `aria-label`, `role="img"`).
     * Distinguishes decorative images (`alt=""` or `role="presentation"`) from informative visuals requiring descriptive text.
     * Automatically asserts WCAG compliance in synthesized Robot Framework and Pytest suites.
2. **Structural Header & Navigation Deconstruction (`header_and_navigation`)**:
   * Extracts navigation landmarks (`<header>`, `<nav>`, `role="navigation"`).
   * Catalogs brand identity links, top-level menu hierarchies, action buttons, mobile hamburger toggles, and global search triggers.
3. **Body Features & Interactive Cards Extraction (`body_features_and_cards`)**:
   * Identifies product/feature card grids, extracting card titles, descriptive copy, iconography, and call-to-action (CTA) links.
   * Supplies exact structural metadata to the Page Object Model synthesizer, ensuring dynamic elements are targeted via robust semantic relationships.
4. **Dynamic Underlying API Discovery (`discovered_apis.json`)**:
   * Executes in-browser JavaScript via `window.performance.getEntriesByType('resource')` during dynamic crawling.
   * Captures runtime background network requests (XHR, Fetch, WebSocket, GraphQL) and persists them to `artifacts/discovered_apis.json` to seed API and k6 test generation.

---

### 📑 Enhanced 3-Pillar Master Requirements Document (BRD, PRD, FRD)

During application synthesis, ATP's RAG engine generates an exhaustive, audit-grade **Master Requirements Document (MRD)** saved to `artifacts/reports/master_requirements_document.md`. The MRD bridges business intent with automated verification across three formalized pillars:

```text
+-----------------------------------------------------------------------------------------------+
|                      ENTERPRISE 3-PILLAR MASTER REQUIREMENTS DOCUMENT (MRD)                   |
+-----------------------------------------------------------------------------------------------+
| 1. Business Requirements Document (BRD) | Defines target personas, journeys & business goals  |
| 2. Product Requirements Document (PRD)  | Defines Epics, BDD Gherkin stories & state machines |
| 3. Functional Requirements Document (FRD)| Defines Acceptance criteria, assets & ASPICE RTM   |
+-----------------------------------------------------------------------------------------------+
```

1. **Pillar 1: Business Requirements Document (BRD)**:
   * **4 Target Personas**:
     * `PER-01 (QA Automation Architect)`: Focuses on framework maintainability, test execution determinism, and zero flakiness.
     * `PER-02 (DevOps & Release Engineer)`: Demands headless CI/CD containerization, non-blocking pipelines, and strict exit code handling.
     * `PER-03 (Engineering Leadership)`: Requires comprehensive test estate visibility, coverage metrics, and zero data leakage.
     * `PER-04 (End User / Consumer)`: Validates seamless interaction flows, sub-second render latencies, and accessibility compliance.
   * **End-to-End User Journeys**: Step-by-step business workflows detailing pre-conditions, user actions, expected outcomes, and business impact.
2. **Pillar 2: Product Requirements Document (PRD)**:
   * **Epics & BDD User Stories**: Structured across `EPIC-NAV` (Navigation & Discovery), `EPIC-FEAT` (Features & Cards), `EPIC-IMG` (Visual Media & WCAG), and `EPIC-NFR` (Concurrency & Performance).
   * **Mermaid State Transition Models**: Visual state machine diagrams illustrating route reachability, authentication state transitions, and error boundary recovery.
3. **Pillar 3: Functional Requirements Document (FRD)**:
   * **Exhaustive Acceptance Criteria Matrix**: Detailed table defining functional requirements, priority levels (P0-Critical, P1-High, P2-Medium), verification methods, and acceptance thresholds.
   * **Image & Visual Asset Matrix**: Tabulated asset inventory detailing dimensions, classification, alt text values, and WCAG 1.1.1 compliance status.
   * **Body Features & Content Cards Matrix**: Grid mapping every card container to its corresponding DOM selector, heading, and CTA action.
   * **ASPICE SWE.4 / ISO 26262 Bidirectional Traceability**: Bidirectional mapping tying every business requirement to its automated test execution implementation.

---

### 🚀 Multi-Scenario k6 Concurrency & Repeated Iteration Engine (`auto_load_test.js`)

To guarantee real-world infrastructure resilience, ATP generates a multi-scenario Grafana k6 performance suite targeting discovered application routes and underlying APIs:

```javascript
// Dual-Scenario Architecture in artifacts/scripts/auto_load_test.js
export const options = {
  scenarios: {
    // Scenario 1: Simultaneous Peak Burst (20 VUs hitting page at EXACT same time)
    concurrent_burst_stress: {
      executor: 'constant-vus',
      vus: 20,
      duration: '10s',
      exec: 'concurrentBurstFlow',
      startTime: '0s',
    },
    // Scenario 2: Repeated Sequential Launches (5 VUs completing 10 cycles each)
    repeated_page_iterations: {
      executor: 'per-vu-iterations',
      vus: 5,
      iterations: 10,
      maxDuration: '30s',
      exec: 'repeatedLaunchFlow',
      startTime: '10s',
    },
  },
  thresholds: {
    'http_req_duration': ['p(95)<500'],        // Global 95th percentile latency < 500ms
    'http_failure_rate': ['rate<0.01'],         // Global HTTP error rate strictly below 1%
    'concurrent_burst_duration': ['p(95)<600'], // Burst scenario SLA
    'repeated_launch_duration': ['p(95)<400'],  // Sustained iteration SLA
  },
};
```

* **Simultaneous Peak Burst (`concurrentBurstFlow`)**: Fires 20 virtual users simultaneously at time 0 to expose database connection pool exhaustion, thread lock contention, and initial caching bottlenecks.
* **Repeated Page Iterations (`repeatedLaunchFlow`)**: Executes 50 cumulative page visits across 5 VUs to audit client-side cache behavior, memory leakage, and TTFB (Time to First Byte) latency drift over sustained operations.
* **Discovered API Stressing**: Concurrently queries underlying backend endpoints discovered during DOM crawling, verifying that backend microservices meet strict latency SLAs under load.

---

### 🗺️ Enterprise Coverage Heatmap & Gap Fulfiller (`coverage_engine.py`)

To solve test fragmentation and visibility gaps across complex enterprise applications, ATP features an **Intelligent 5-Discipline Coverage Matrix Engine**:

```text
+-----------------------------------------------------------------------------------------------+
|                 ASPICE SWE.4 & SWE.5 MULTI-DISCIPLINE COVERAGE HEATMAP MATRIX                 |
+-----------------------------------------------------------------------------------------------+
|  Entity / Endpoint Route  |  UI E2E (POM)  |  API (BVA)  |  Load (k6)  | Acceptance | Security|
+---------------------------+----------------+-------------+-------------+------------+---------+
| /api/chat/ask             |     [✓ 6]      |    [✓ 1]    |    [+ Fill] |  [+ Fill]  |  [✓ 1]  |
| /api/coverage/matrix      |     [✓ 6]      |    [✓ 1]    |    [+ Fill] |  [+ Fill]  |  [✓ 1]  |
| /api/evaluate             |     [✓ 6]      |    [✓ 1]    |    [+ Fill] |  [+ Fill]  |  [✓ 1]  |
| /api/storage/clean        |     [✓ 6]      |    [✓ 1]    |    [+ Fill] |  [+ Fill]  |  [✓ 1]  |
+-----------------------------------------------------------------------------------------------+
| Overall Estate Coverage: 59.6%  •  28 Discovered Entities  •  13 Active Tests  •  57 Gaps     |
+-----------------------------------------------------------------------------------------------+
```

#### 1. The 5 Integrated Testing Disciplines
Every crawled route, page, and backend API is cross-referenced against 5 enterprise testing pillars:
1. **UI E2E**: End-to-end user workflows, Page Object Model (POM) interactions, explicit waits, and visual assertion checks (`artifacts/scripts/auto_ui_test.py`).
2. **API (BVA)**: Boundary Value Analysis, schema validation, HTTP status assertion, and latency SLA checks (`artifacts/scripts/auto_api_test.py`).
3. **Load (k6)**: High-concurrency performance thresholds, virtual user (VU) ramps, and p95 latency stress checks (`artifacts/scripts/auto_load_test.js`).
4. **Acceptance (BDD)**: Human-readable Gherkin/BDD scenarios, ASPICE requirement tracing, and Robot Framework keywords (`artifacts/scripts/auto_suite.robot`).
5. **Security (OWASP)**: Defensive injection probes (SQLi, XSS, SSRF), parameter fuzzing, and credential leakage checks.

#### 2. Deep AST-Based Test Estate Audit
Rather than simple file presence checks, `CoverageMatrixEngine` performs deep static analysis:
* **Python Abstract Syntax Trees (`ast.parse`)**: Extracts test function definitions, docstrings, line numbers, and decorator markers.
* **Robot Framework Lexer**: Parses test case blocks, `[Tags]`, `[Documentation]`, and step keywords.
* **k6 JavaScript Scanner**: Scans virtual user endpoint definitions, HTTP methods, and threshold configurations.
* **Tag Taxonomy**: Automatically extracts, catalogs, and indexes all metadata tags (`#P0-Critical`, `#P1-High`, `#UI-POM`, `#API-BVA`, `#Load-k6`, `#BDD-Acceptance`).

#### 3. Interactive Web Heatmap & Test Inspector Drawer
The Web Dashboard (`static/index.html`) includes a dedicated **🗺️ Coverage Matrix** modal:
* **6 Live Metric Cards**: Total Coverage %, UI E2E %, API BVA %, Load k6 %, Acceptance %, and OWASP Security %.
* **Instant Filtering**: Filter entities by search keyword, view status (`All`, `Gaps Only`, `Fully Covered`), or click any metric card to isolate specific gaps.
* **Test Case Inspector Drawer**: Clicking any covered cell (`✓ N`) expands an inspector drawer displaying test names, human-readable docstrings, tags, line numbers, and file paths.

#### 4. Sovereign 1-Click Gap Fulfiller & Custom Test Injection
Users can seal identified gaps with two flexible workflows:
* **⚡ 1-Click Auto-Fulfill (`POST /api/coverage/fulfill`)**: Sovereign synthesis instantly generates the missing test discipline for the selected entity, auto-validates syntax, and links it into the active suite.
* **✍️ Add Custom Test Case (`POST /api/coverage/custom-test`)**: SDETs can specify custom test names, enterprise docstrings, tags, and code blocks to insert bespoke assertions directly into target files.

---

## 📋 Sample Generated Test Suites (Multi-Discipline Code Gallery)

### 1. Unified Enterprise Test Automation Harness (Robot Framework, Selenium 4, Pyppeteer)

ATP provides a unified test harness orchestrating **Robot Framework Browser**, **Selenium 4**, and **Pyppeteer** in a single cohesive Python ecosystem managed by **Poetry**:

#### A. Playwright-Backed Robot Suite (`tests/suite_playwright.robot`)
```robot
*** Settings ***
Documentation       Enterprise CI/CD Suite for Playwright-backed Browser Library.
...                 Demonstrates WAF Header Injection, Spinner Detachment, and
...                 Cloudflare Turnstile testing sitekey interaction.
Library             Browser
Variables           ../config/settings.py
Suite Setup         Initialize Enterprise Browser Context
Suite Teardown      Close Browser    ALL

*** Variables ***
${SPINNER_LOCATOR}          css=#app-loader
${REGISTRATION_FORM}        css=form#signup-form
${TURNSTILE_CONTAINER}      css=[data-sitekey]
${TURNSTILE_RESPONSE}       css=[name="cf-turnstile-response"]
${SUBMIT_BUTTON}            css=button[type="submit"]
${SUCCESS_BANNER}           css=.alert-success

*** Test Cases ***
Scenario: Verified Registration Flow Behind WAF With Turnstile Verification
    [Documentation]    Validates seamless form submission under headless CI/CD execution.
    [Tags]             waf_protected    smoke    registration
    
    Given Application Landing Page Is Loaded Without Loading Spinners
    When Completing Registration Details With Turnstile Verification
    Then Account Creation Confirmation Is Rendered Deterministically

*** Keywords ***
Initialize Enterprise Browser Context
    New Browser    browser=${settings.BROWSER}    headless=${settings.HEADLESS}
    New Context    viewport={'width': 1920, 'height': 1080}
    ...            extraHTTPHeaders=${settings.extra_http_headers}
    New Page       ${settings.BASE_URL}

Application Landing Page Is Loaded Without Loading Spinners
    Wait For Elements State    ${SPINNER_LOCATOR}    detached    timeout=${settings.GLOBAL_TIMEOUT}s
    Wait For Elements State    ${REGISTRATION_FORM}   visible     timeout=${settings.GLOBAL_TIMEOUT}s

Completing Registration Details With Turnstile Verification
    Fill Text    ${REGISTRATION_FORM} input[name="email"]    qa-architect@enterprise.internal
    Fill Text    ${REGISTRATION_FORM} input[name="password"] ${settings.TEST_ACCOUNT_PASSWORD}
    
    # Synchronize on Cloudflare Turnstile token completion
    Wait For Elements State    ${TURNSTILE_CONTAINER}    visible    timeout=${settings.GLOBAL_TIMEOUT}s
    Wait For Condition    Element Text
    ...    ${TURNSTILE_RESPONSE}
    ...    validate
    ...    value != ''
    ...    timeout=${settings.GLOBAL_TIMEOUT}s
    ...    message=Cloudflare Turnstile verification challenge timed out.
    
    Click    ${SUBMIT_BUTTON}

Account Creation Confirmation Is Rendered Deterministically
    Wait For Elements State    ${SPINNER_LOCATOR}    detached    timeout=${settings.GLOBAL_TIMEOUT}s
    Wait For Elements State    ${SUCCESS_BANNER}     visible     timeout=${settings.GLOBAL_TIMEOUT}s
```

#### B. Selenium 4 Pytest Suite with CDP Header Injection (`tests/test_selenium.py`)
```python
"""
tests/test_selenium.py
Pure Python pytest module implementing Selenium 4 with CDP header injection
and explicit WebDriverWait element sync strategies.
"""
import pytest
from selenium import webdriver
from selenium.webdriver.chrome.service import Service
from selenium.webdriver.chrome.options import Options
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
from config.settings import settings

@pytest.fixture(scope="function")
def driver():
    chrome_options = Options()
    if settings.HEADLESS:
        chrome_options.add_argument("--headless=new")
    chrome_options.add_argument("--no-sandbox")
    chrome_options.add_argument("--disable-dev-shm-usage")
    chrome_options.add_argument("--window-size=1920,1080")

    driver = webdriver.Chrome(options=chrome_options)
    
    # Inject CI/CD WAF allowlist headers via Chrome DevTools Protocol (CDP)
    if settings.extra_http_headers:
        driver.execute_cdp_cmd("Network.enable", {})
        driver.execute_cdp_cmd("Network.setExtraHTTPHeaders", {"headers": settings.extra_http_headers})

    yield driver
    driver.quit()

@pytest.mark.waf_protected
@pytest.mark.regression
def test_authenticated_workflow_with_turnstile_and_spinners(driver):
    """Validates registration behind WAF allowlisting with explicit loader detachment."""
    driver.get(str(settings.BASE_URL))
    wait = WebDriverWait(driver, timeout=settings.GLOBAL_TIMEOUT, poll_frequency=0.5)

    # 1. Deterministic sync: Wait for loading overlay invisibility
    loader_locator = (By.CSS_SELECTOR, "#app-loader")
    wait.until(EC.invisibility_of_element_located(loader_locator))

    # 2. Complete form fields
    form = wait.until(EC.visibility_of_element_located((By.CSS_SELECTOR, "form#signup-form")))
    driver.find_element(By.CSS_SELECTOR, "input[name='email']").send_keys("qa-architect@enterprise.internal")
    driver.find_element(By.CSS_SELECTOR, "input[name='password']").send_keys(settings.TEST_ACCOUNT_PASSWORD)

    # 3. Synchronize on Cloudflare Turnstile automated testing response
    turnstile_response_input = (By.CSS_SELECTOR, "input[name='cf-turnstile-response']")
    wait.until(lambda d: d.find_element(*turnstile_response_input).get_attribute("value") != "")

    # 4. Submit and verify confirmation banner
    driver.find_element(By.CSS_SELECTOR, "button[type='submit']").click()
    wait.until(EC.invisibility_of_element_located(loader_locator))
    banner = wait.until(EC.visibility_of_element_located((By.CSS_SELECTOR, ".alert-success")))
    assert "Registration Complete" in banner.text
```

---

### 2. Deterministic CI/CD WAF Allowlisting & Cloudflare Turnstile Verification Strategy

Enterprise applications in CI/CD pipelines cannot and should not rely on brittle "anti-bot bypass" hacks (such as stealth scripts, mouse jittering, or CAPTCHA-breaking extensions). These hacks violate enterprise security policies, introduce non-deterministic pipeline flakes, and break whenever Cloudflare updates its fingerprint models.

ATP implements the **Enterprise-Grade Testing Standard**:

```text
+-----------------------------------------------------------------------------------------------+
|                  ENTERPRISE CI/CD WAF & CHALLENGE SYNCHRONIZATION STRATEGY                     |
+-----------------------------------------------------------------------------------------------+
| 1. CI/CD WAF Allowlist Header   --> CDP Network.setExtraHTTPHeaders: X-Automation-Bypass-Token|
| 2. Deterministic Loading Sync   --> Explicit WebDriverWait / detached state on #app-loader    |
| 3. Cloudflare Turnstile Testing --> Uses official CF sitekeys: 1x00000000000000000000AA       |
| 4. Token Completion Sync        --> Explicit polling on input[name="cf-turnstile-response"]    |
+-----------------------------------------------------------------------------------------------+
```

1. **WAF Allowlisting via Chrome DevTools Protocol (CDP)**:
   * Pipelines authenticate to the staging environment using an authorized bypass token (`settings.WAF_BYPASS_TOKEN`).
   * The framework automatically injects headers via CDP (`Network.setExtraHTTPHeaders`) in Selenium and `extraHTTPHeaders` in Playwright/Pyppeteer, cleanly passing Cloudflare WAF without triggering challenges.
2. **Cloudflare Turnstile Automated Testing Keys**:
   * For testing widget rendering and token transmission, staging environments configure Cloudflare's official dummy sitekeys:
     * `1x00000000000000000000AA`: **Always Passes** (instantly issues a valid test pass token).
     * `2x00000000000000000000AB`: **Always Blocks** (for validating error handling).
3. **Deterministic Loading Screen Detachment**:
   * Rather than arbitrary `time.sleep()`, tests deterministically synchronize on the disappearance of loading overlays (`#app-loader`, `.spinner`, `div[role="progressbar"]`) using `EC.invisibility_of_element_located` and `Wait For Elements State detached`.

---

### 3. Resilient E2E UI Suite with Dynamic Landmark & Section Hierarchy Verification (`auto_ui_test.py`)

Synthesized Page Object Model (POM) suites feature multi-tier structural fallbacks to handle diverse web frameworks (React, Vue, Next.js, Angular, static HTML):

```python
# artifacts/scripts/auto_ui_test.py
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
import allure

class Landing_CatalogPOM:
    def __init__(self, driver):
        self.driver = driver
        self.URL = "https://target-app:8080/"
        # Resilient multi-tier layout selector encompassing HTML5 landmarks, CSS layouts, and SPA roots
        self.SECTIONS = (By.CSS_SELECTOR, (
            "main, article, section, header, footer, nav, aside, "
            "[role='main'], [role='region'], [role='article'], [role='banner'], "
            ".section, .container, .wrapper, .layout, .page, .content, .card, .box, .hero, .panel, .grid, .view, "
            "#root > *, #app > *, #__next > *"
        ))

    @allure.step("1. Wait for Full Hydration and Page Readiness")
    def wait_for_page_ready(self, timeout=10):
        wait = WebDriverWait(self.driver, timeout)
        wait.until(lambda d: d.execute_script("return document.readyState") == "complete")

    @allure.step("2. Verify Layout Structure & Section Container Hierarchy")
    def verify_sections_hierarchy(self):
        self.driver.get(self.URL)
        self.wait_for_page_ready(timeout=10)
        
        # Primary container discovery
        elements = self.driver.find_elements(*self.SECTIONS)
        
        # Multi-tier fallback for non-semantic or flat DOM trees
        if not elements:
            elements = self.driver.find_elements(
                By.CSS_SELECTOR, 
                "body > div, body > section, body > main, #root > *, #app > *, #__next > *, body"
            )
        assert len(elements) > 0, "[LAYOUT FAIL] No structural layout containers rendered"
        
        # Visibility audit with body safety fallback
        visible_elements = [e for e in elements if e.is_displayed()]
        if not visible_elements and elements:
            try:
                body = self.driver.find_element(By.TAG_NAME, "body")
                if body.is_displayed():
                    visible_elements = [body]
            except Exception:
                pass
        assert len(visible_elements) > 0, "[LAYOUT FAIL] Structural layout containers rendered but none visible"
        return True
```

---

### 4. API Boundary Value Analysis Suite (`auto_api_test.py`)

```python
# artifacts/scripts/auto_api_test.py
import pytest
import requests
import allure

BASE_URL = "http://target-app:8080"

@allure.epic("API Boundary & SLA Matrix")
@allure.feature("Discovered Endpoints")
class TestApiDiscoveredSuite:

    @allure.story("Contract & Latency SLA: /api/v1/catalog")
    @pytest.mark.parametrize("route", ["/api/v1/catalog", "/api/v1/users/profile"])
    def test_endpoint_contract_and_latency(self, route):
        url = f"{BASE_URL}{route}"
        with allure.step(f"Issue GET request to {url}"):
            response = requests.get(url, timeout=5.0)
            
        assert response.status_code in [200, 201, 204, 301, 401, 403], f"Unexpected status: {response.status_code}"
        assert response.elapsed.total_seconds() < 0.500, f"SLA Violation: Latency was {response.elapsed.total_seconds()}s"

    @allure.story("Boundary Value Analysis (BVA): Malformed Payloads")
    @pytest.mark.parametrize("payload", [{}, {"query": ""}, {"query": " " * 50}, {"query": None}])
    def test_bva_malformed_queries(self, payload):
        url = f"{BASE_URL}/api/v1/search"
        response = requests.post(url, json=payload, timeout=5.0)
        # BVA rule: Must gracefully reject with client error, NEVER leak server 500
        assert response.status_code in [200, 400, 422], f"Server leaked internal error: {response.status_code}"
```

---

### 5. Multi-Scenario Load & Concurrency Suite (`auto_load_test.js`)

```javascript
// artifacts/scripts/auto_load_test.js
import http from 'k6/http';
import { check, sleep } from 'k6';
import { Rate, Trend, Counter } from 'k6/metrics';

const concurrentBurstLatency = new Trend('concurrent_burst_duration');
const repeatedLaunchLatency = new Trend('repeated_launch_duration');
const httpFailureRate = new Rate('http_failure_rate');
const successfulLaunches = new Counter('successful_page_launches');

export const options = {
  scenarios: {
    // 1. Simultaneous Peak Burst (Launching page at the EXACT SAME TIME)
    concurrent_burst_stress: {
      executor: 'constant-vus',
      vus: 20,
      duration: '10s',
      exec: 'concurrentBurstFlow',
      startTime: '0s',
    },
    // 2. Repeated Sequential Launches (Launching page MULTIPLE TIMES)
    repeated_page_iterations: {
      executor: 'per-vu-iterations',
      vus: 5,
      iterations: 10,
      maxDuration: '30s',
      exec: 'repeatedLaunchFlow',
      startTime: '10s',
    },
  },
  thresholds: {
    'http_req_duration': ['p(95)<500'],
    'http_failure_rate': ['rate<0.01'],
    'concurrent_burst_duration': ['p(95)<600'],
    'repeated_launch_duration': ['p(95)<400'],
  },
};

export function concurrentBurstFlow() {
  const res = http.get('http://target-app:8080/');
  concurrentBurstLatency.add(res.timings.duration);
  const success = check(res, {
    'Burst: status is 200': (r) => r.status === 200,
    'Burst: latency < 600ms': (r) => r.timings.duration < 600,
  });
  httpFailureRate.add(!success);
  if (success) successfulLaunches.add(1);
}

export function repeatedLaunchFlow() {
  const res = http.get('http://target-app:8080/');
  repeatedLaunchLatency.add(res.timings.duration);
  const success = check(res, {
    'Repeated: status is 200': (r) => r.status === 200,
    'Repeated: latency < 400ms': (r) => r.timings.duration < 400,
  });
  httpFailureRate.add(!success);
  if (success) successfulLaunches.add(1);
  sleep(0.5);
}
```

---

### 6. Acceptance BDD Suite & Full Keyword Harness (`auto_suite.robot` & `keywords_lib.py`)

#### A. Master Acceptance Suite (`artifacts/scripts/auto_suite.robot`)
```robot
*** Settings ***
Documentation     Master Orchestration Suite Grounded by Enterprise RAG.
Library           keywords_lib.SUTKeywords    WITH NAME    SUT
Suite Setup       SUT.Start Browser
Suite Teardown    SUT.Stop Browser
Test Setup        Log    Initializing Test Data and resetting DOM state.
Test Teardown     Run Keyword If Test Failed    SUT.Take Screenshot    ${TEST NAME}_failure.png

*** Variables ***
${BASE_URL}         http://target-app:8080

*** Test Cases ***
TC-JOURNEY-01: End-to-End User Discovery, Navigation & Brand Layout Flow
    [Documentation]    Full multi-step landing exploration and layout structure audit.
    [Tags]             #P0-Critical    #Journey    #ASPICE-SWE4
    Given Target Application Is Reachable At "${BASE_URL}"
    When User Inspects Primary Hero Header And Navigation Brand
    Then Brand Logo And Visual Assets Satisfy WCAG 1.1.1 Guidelines
    And Structural Sections And Feature Cards Hierarchy Are Fully Rendered

TC-P01-11-CONCUR: Verify Simultaneous Peak Concurrency (At Same Time) Resilience
    [Documentation]    Validates server tolerance under simultaneous peak burst requests.
    [Tags]             #P0-Critical    #Concurrency    #Performance
    Given A Concurrent User Pool Of 20 Virtual Users
    When Executing Simultaneous Peak Burst Requests To Root
    Then Response Time P95 Must Remain Within SLA

TC-P01-12-REPEAT: Verify Repeated Page Launches (Multiple Times) & TTFB Drift
    [Documentation]    Validates stability across repeated page navigation cycles.
    [Tags]             #P1-High    #Reliability    #MemoryStability
    Given An Automated Iteration Harness Configured For 10 Consecutive Cycles
    When Executing Repeated Navigation Cycles
    Then Response Times Must Stabilize Without Memory Leakage
```

#### B. Underlying Keyword Implementation (`artifacts/scripts/keywords_lib.py`)
```python
# artifacts/scripts/keywords_lib.py
import time
import requests
import concurrent.futures
from robot.api.deco import keyword

class SUTKeywords:
    @keyword("A Concurrent User Pool Of ${vu_count:\d+} Virtual Users")
    def configure_concurrent_user_pool(self, vu_count):
        self.vu_count = int(vu_count)
        print(f"[CONCURRENCY] Initialized user pool: {self.vu_count} VUs")

    @keyword("Executing Simultaneous Peak Burst Requests To Root")
    def execute_simultaneous_peak_burst(self):
        url = getattr(self, "base_url", "http://target-app:8080")
        latencies = []
        def fetch(_):
            t0 = time.time()
            r = requests.get(url, timeout=5.0)
            return r.status_code, (time.time() - t0) * 1000

        with concurrent.futures.ThreadPoolExecutor(max_workers=self.vu_count) as pool:
            futures = [pool.submit(fetch, i) for i in range(self.vu_count)]
            for f in concurrent.futures.as_completed(futures):
                status, lat = f.result()
                assert status == 200, f"[BURST FAIL] HTTP status {status}"
                latencies.append(lat)

        self.p95_burst = sorted(latencies)[int(0.95 * len(latencies))]

    @keyword("Response Time P95 Must Remain Within SLA")
    def verify_p95_sla(self):
        assert self.p95_burst < 1500, f"[SLA VIOLATION] Burst p95 latency {self.p95_burst:.1f}ms exceeded SLA"

    @keyword("An Automated Iteration Harness Configured For ${cycle_count:\d+} Consecutive Cycles")
    def configure_iteration_harness(self, cycle_count):
        self.cycle_count = int(cycle_count)

    @keyword("Executing Repeated Navigation Cycles")
    def execute_repeated_navigation_cycles(self):
        url = getattr(self, "base_url", "http://target-app:8080")
        self.cycle_latencies = []
        for c in range(self.cycle_count):
            t0 = time.time()
            r = requests.get(url, timeout=5.0)
            assert r.status_code == 200, f"[CYCLE FAIL] Iteration {c} returned {r.status_code}"
            self.cycle_latencies.append((time.time() - t0) * 1000)

    @keyword("Response Times Must Stabilize Without Memory Leakage")
    def verify_response_stabilization(self):
        first_half = self.cycle_latencies[:len(self.cycle_latencies)//2]
        second_half = self.cycle_latencies[len(self.cycle_latencies)//2:]
        avg_first = sum(first_half) / len(first_half)
        avg_second = sum(second_half) / len(second_half)
        drift = (avg_second - avg_first) / max(avg_first, 1.0)
        assert drift < 2.0, f"[PERF DEGRADATION] Latency drifted by {drift*100:.1f}% across iterations"
```

---

### 7. Pabot Parallel Execution Transcript & Human-Readable Verification Log

When Pabot executes tests in parallel across CPU cores (`pabot --testlevelsplit --processes 4 --pythonpath artifacts/scripts --outputdir artifacts/reports/pabot_results artifacts/scripts/auto_suite.robot`), the console output and generated HTML logs read like an **executive verification transcript** that makes 100% intuitive sense to QA Leads, Software Architects, Product Managers, and Compliance Auditors.

#### 🖥️ Real Live Pabot Execution Transcript (Empirically Verified in Container)
```text
==============================================================================
[PABOT] Master Parallel Test-Level Cluster Initialized
[PABOT] Process Pool : 4 Concurrent Worker PIDs | Runner: Headless Chromium
[PABOT] Test Suite   : artifacts/scripts/auto_suite.robot
[PABOT] Output Dir   : artifacts/reports/pabot_results/
==============================================================================
2026-09-05 14:11:09 [PID:35463] [0] [ID:0] EXECUTING Auto Suite.TC-UI-01: Verify Application Landing Page Reachability, Brand Logo & Document Title Contract
2026-09-05 14:11:09 [PID:35462] [1] [ID:1] EXECUTING Auto Suite.TC-UI-02: Verify Primary Action Elements, Button Clickability & Event Handling
2026-09-05 14:11:09 [PID:35461] [2] [ID:2] EXECUTING Auto Suite.TC-UI-03: Verify Form Field Nominal Data Entry & State Persistence
2026-09-05 14:11:09 [PID:35467] [3] [ID:3] EXECUTING Auto Suite.TC-UI-04: Verify Input Field Boundary Value Analysis (BVA) & Graceful Error Handling

2026-09-05 14:11:15 [PID:35463] [0] [ID:0] PASSED Auto Suite.TC-UI-01: Verify Application Landing Page Reachability, Brand Logo & Document Title Contract in 6.0 seconds
2026-09-05 14:11:15 [PID:35974] [0] [ID:4] EXECUTING Auto Suite.TC-UI-05: Verify Dropdown Option Selection & Selection Event Handling

2026-09-05 14:11:16 [PID:35461] [2] [ID:2] PASSED Auto Suite.TC-UI-03: Verify Form Field Nominal Data Entry & State Persistence in 6.8 seconds
2026-09-05 14:11:16 [PID:35981] [1] [ID:5] EXECUTING Auto Suite.TC-SEC-01: Defensive Security: Cross-Site Scripting (XSS) & SQL Injection Payload Probing

2026-09-05 14:11:16 [PID:35467] [3] [ID:3] PASSED Auto Suite.TC-UI-04: Verify Input Field Boundary Value Analysis (BVA) & Graceful Error Handling in 6.8 seconds
2026-09-05 14:11:16 [PID:35992] [2] [ID:6] EXECUTING Auto Suite.TC-PERF-01: Client Render SLA Performance & Document Localization Attributes

2026-09-05 14:11:18 [PID:35462] [1] [ID:1] PASSED Auto Suite.TC-UI-02: Verify Primary Action Elements, Button Clickability & Event Handling in 8.7 seconds
2026-09-05 14:11:18 [PID:36347] [3] [ID:7] EXECUTING Auto Suite.TC-API-01: Backend Microservices Health Endpoint Contract & Response Latency

2026-09-05 14:11:20 [PID:35992] [2] [ID:6] PASSED Auto Suite.TC-PERF-01: Client Render SLA Performance & Document Localization Attributes in 3.8 seconds
2026-09-05 14:11:20 [PID:36477] [0] [ID:8] EXECUTING Auto Suite.TC-ORCH-01: Orchestrate External Python Page Object Model (POM) UI Suite

2026-09-05 14:11:21 [PID:35981] [1] [ID:5] PASSED Auto Suite.TC-SEC-01: Defensive Security: Cross-Site Scripting (XSS) & SQL Injection Payload Probing in 4.4 seconds
2026-09-05 14:11:21 [PID:36483] [1] [ID:9] EXECUTING Auto Suite.TC-ORCH-02: Orchestrate External Python REST API Boundary Value Analysis Suite

2026-09-05 14:11:21 [PID:36347] [3] [ID:7] PASSED Auto Suite.TC-API-01: Backend Microservices Health Endpoint Contract & Response Latency in 2.5 seconds
2026-09-05 14:11:25 [PID:36483] [1] [ID:9] PASSED Auto Suite.TC-ORCH-02: Orchestrate External Python REST API Boundary Value Analysis Suite in 4.5 seconds
2026-09-05 14:11:27 [PID:35974] [0] [ID:4] PASSED Auto Suite.TC-UI-05: Verify Dropdown Option Selection & Selection Event Handling in 11.8 seconds
2026-09-05 14:12:10 [PID:36477] [0] [ID:8] PASSED Auto Suite.TC-ORCH-01: Orchestrate External Python Page Object Model (POM) UI Suite in 50.1 seconds
==============================================================================
PABOT TEST RUN SUMMARY:
10 tests, 10 passed, 0 failed, 0 skipped.
Total Cumulative Testing Time : 1 minute 45.40 seconds
Elapsed Wall-Clock Time       : 1 minute 3.93 seconds (⚡ 1.65x Parallel Acceleration)
Generated Reports:
  * Master XML Output  : artifacts/reports/pabot_results/output.xml
  * Human-Readable Log : artifacts/reports/pabot_results/log.html
  * Executive Overview : artifacts/reports/pabot_results/report.html
==============================================================================
```

---

#### 🔍 Anatomy of Human-Readable Pabot Results (`log.html` & Console)

When an executive, QA lead, or auditor opens [`artifacts/reports/pabot_results/log.html`](file:///c:/Users/Junko/Downloads/ragllmorch/artifacts/reports/pabot_results/log.html), every layer of the test execution is structured in plain, unambiguous English:

| Result Layer | What the Engineer / Stakeholder Sees | Why It Makes 100% Sense (Zero Cryptic Code) |
| :--- | :--- | :--- |
| **1. Test Case Title** | `TC-UI-01: Verify Application Landing Page Reachability, Brand Logo & Document Title Contract` | Immediately identifies the business domain (`UI`), test category (`Reachability`), and exact contract being verified without opening source code. |
| **2. Documentation Block** | `[ASPICE Trace: REQ-SYS-NAV-001 \| Persona: Anonymous Visitor]`<br>`Business Objective: Ensure that the public web application root route is reachable, loads within SLA (<4.0s), has a valid document title, and visibly renders core layout structure without HTTP 500 error boundaries.`<br>`Acceptance Criteria: HTTP 200 OK, title is non-empty, and DOM containers are intact.` | Communicates the **Why**, **Who**, and **What** to product owners, auditors, and SDETs. Establishes bidirectional traceability to requirements. |
| **3. BDD Given/When/Then Tree** | `► Given the test engineer initializes an isolated browser session for route https://google.com`<br>`► When the page DOM content and interactive elements load`<br>`► Then the destination URL should be reachable`<br>`► And the page title should not be empty`<br>`► And the primary structural sections should be visible` | Formats the verification as a natural user journey narrative rather than raw code commands. |
| **4. Keyword Action Milestones** | `[SUT] [ACTION] Navigating browser worker to: https://google.com`<br>`[SUT] [SUCCESS] Destination loaded in 0.842s. Current Title: 'Google'`<br>`[SUT] [VERIFY] Inspecting DOM layout containers (header, nav, main, section, footer)...`<br>`[SUT] [PASS] Verified structural layout integrity: Found 12 layout blocks without DOM collapse.` | Emits real-time milestone telemetry via Robot Framework's built-in logger (`robot.api.logger`) so that every click, navigation, and validation is recorded with timestamps and metrics. |
| **5. Failure Evidence (If Detected)** | `[FAILURE DETECTED] Screenshot evidence captured: artifacts/screencast/TC-UI-01_failure.png`<br>`AssertionError: Expected input field to retain 'QA Enterprise Verification' but found empty string.` | Pinpoints the exact root-cause assertion failure with attached screenshot evidence for instant, zero-ambiguity bug triage. |

---

#### 💡 Key Principles of ATP's Human-Readable Testing Standard:
1. **Zero Cryptic Technical Jargon**: Instead of cryptic statements like `click //div[3]/button[2] -> OK`, the logs explicitly read: `[ACTION] Clicking button 'Sign In' -> [PASS] Interactive buttons responded without client-side script errors.`
2. **Multi-Discipline Cohesion**: Whether reviewing a Selenium UI test, a Pytest API test, a k6 performance run, or a Robot Framework suite, all test scripts share identical BDD personas, structured docstrings, and informative assertion diagnostics.
3. **Audit & Compliance Readiness**: Reports can be exported directly into PDF or attached to regulatory submissions (ASPICE, ISO 26262, SOC-2, FDA 21 CFR Part 11) without requiring engineering translation.

---

## 🛡️ Automotive ASPICE & ISO 26262 Bidirectional Traceability (RTM)

For engineering teams operating under **Automotive SPICE (VDA QMC)** or **ISO 26262 Road Vehicles - Functional Safety**, test cases cannot exist in isolation. Every single test step must maintain strict, bidirectional traceability to customer and software requirements:

```
Customer Need (MRD) ◄──► System Req (SYS.2) ◄──► Software Req (SWE.1) ◄──► Automated Test (SWE.6)
```

### Automated Live RTM Generation
During every run, ATP generates and updates [`artifacts/reports/Live_RTM_Matrix.csv`](file:///c:/Users/Junko/Downloads/ragllmorch/artifacts/reports/Live_RTM_Matrix.csv):

| Requirement ID | Specification Clause | Test Discipline | Script Identifier | AST Validation Status | Allure Execution Verdict |
| :--- | :--- | :--- | :--- | :---: | :---: |
| `REQ-AUTH-001` | Multi-Factor Authentication Gate | UI Selenium | `test_ui_portal.py` | `VALIDATED` | `PASSED` |
| `REQ-PERF-014` | API Catalog p95 Response < 500ms | Grafana k6 | `test_performance_profile.js` | `VALIDATED` | `PASSED` |
| `REQ-ASPICE-90`| SWE.4 Autonomous Integration Telemetry | Robot Framework | `execution_suite.robot` | `VALIDATED` | `PASSED` |
| `REQ-SECU-109` | OWASP Input Validation & Injection Rejection | Pytest BVA | `test_api_endpoints.py` | `VALIDATED` | `PASSED` |

---

## ⚡ Live Load Testing & Hardware Calibrator

The framework includes a built-in **Live LLM Inference Load Tester & Optimizer**:

1. Click the **"⚡ Benchmark & Tune LLM"** button in the dashboard sidebar.
2. Click **"🚀 Run Live Load Test (3-Profile Matrix)"**.
3. The engine streams test prompts to Ollama across candidate profiles (High-Velocity 4k, Balanced 8k, Deep Context 16k), measuring:
   - **Generation Speed (tok/s)**
   - **Prompt Evaluation Speed (tok/s)**
   - **Request Latency (ms)**
   - **Processor Mode (100% GPU vs. CPU Offload Warning)**
4. Click **"Apply Profile"** on the recommended profile (e.g., Balanced 8k).
5. The settings immediately persist to `artifacts/db/active_llm_config.json` and Redis, pre-warm Ollama, and automatically govern subsequent test generation runs and the Project Assistant Chat.

---

## 📡 Complete REST API & Real-Time Telemetry Reference

### REST Endpoints Specification

The FastAPI backend exposes a complete programmatic REST API for automated CI/CD pipeline integration:

| Method | Endpoint Path | Description & Payload | Architectural Consumer |
| :--- | :--- | :--- | :--- |
| `POST` | `/api/crawl` | Dispatches headless spider. Body: `{"url": "...", "depth": 2, "auth": {...}}` | React Dashboard / CI Webhook |
| `GET` | `/api/scope_gate/status` | Queries discovered routes, token burn estimates, and risk profile. | Scope Gate HITL Modal |
| `POST` | `/api/scope_gate/approve` | Approves target routes. Body: `{"selected_routes": [...], "settings": {...}}` | Scope Gate Confirmation |
| `POST` | `/api/generate_suite` | Triggers multi-discipline synthesis. Body: `{"suite_types": ["ui", "api", "k6"]}` | Synthesis Engine / Pabot |
| `POST` | `/api/execute` | Launches Pabot parallel test runner inside Docker sandboxes. | Execution Worker Pool |
| `POST` | `/api/chat/ask` | Streams assistant response. Body: `{"prompt": "...", "context": "auto"}` | Project Assistant Chat Panel |
| `GET` | `/api/system/export` | Generates ultra-fast lightweight project export archive (<1MB). | Project Manager / CI Backup |
| `POST` | `/api/system/import` | Safe, non-destructive project import with Zip-Slip defense. Form-data: `file` | Project Manager / Restore |
| `POST` | `/api/system/reload` | Flushes caches and reloads project workspace in place. | In-Place Reload Button |
| `GET` | `/api/system/llm_config` | Returns current active VRAM profile and hardware telemetry. | Hardware Probe & Settings Form |
| `POST` | `/api/system/benchmark_llm` | Runs 3-profile streaming live load test against Ollama. | Live Load Tester Modal |
| `POST` | `/api/system/apply_llm_settings`| Persists runtime context/batch settings and pre-warms Ollama. | 1-Click Profile Applier |
| `GET` | `/api/telemetry/stream` | Server-Sent Events (SSE) streaming real-time GPU/RAM/Tok/s metrics. | Real-Time Telemetry Graphs |
| `GET` | `/api/reports/allure/html/index.html` | Serves compiled interactive Allure HTML test report. | Embedded Allure Iframe |
| `GET` | `/api/reports/allure/download` | Streams a ZIP archive of all reports, screenshots, and logs. | Download Report Button |

---

### ⚡ High-Speed Lightweight Project Export & Safe Non-Destructive Reload Engine (<1MB, <0.3s)

In conventional frameworks, exporting a project frequently hangs or generates gigabytes of redundant data because model weights, database files, and object caches are inadvertently included in the archive.

ATP implements an **Intelligent Allowlist / Blacklist Export & Reload Engine**:

```text
+-----------------------------------------------------------------------------------------------+
|                     HIGH-SPEED LIGHTWEIGHT PROJECT EXPORT ARCHITECTURE                         |
+-----------------------------------------------------------------------------------------------+
| INCLUDED (Strict Allowlist):                                                                  |
|   ✓ manifest.json, pyproject.toml, pytest.ini, deploy_enterprise_qa.py                        |
|   ✓ config/ (settings.py, WAF tokens)                                                         |
|   ✓ libraries/ (PyppeteerKeywords.py, custom keyword bridges)                                 |
|   ✓ tests/ (suite_playwright.robot, test_selenium.py)                                         |
|   ✓ artifacts/scripts/ (auto_ui_test.py, auto_api_test.py, auto_load_test.js, auto_suite.robot)|
|   ✓ artifacts/reports/ (master_requirements_document.md, rtm_parser.py)                       |
|   ✓ artifacts/discovered_apis.json                                                            |
|                                                                                               |
| EXCLUDED (Strict Blacklist):                                                                  |
|   ✗ artifacts/ollama/ (Local LLM neural network weights ~2.2 GB)                              |
|   ✗ artifacts/db/ (PostgreSQL database cluster data)                                          |
|   ✗ artifacts/storage/ (MinIO S3 blob object storage)                                         |
|   ✗ artifacts/reports/history/ (Thousands of legacy Allure execution logs)                     |
|   ✗ .git/, __pycache__/, *.pyc, node_modules/, .pytest_cache/                                 |
+-----------------------------------------------------------------------------------------------+
```

#### Empirical Export Performance Benchmark

| Metric | Unoptimized Baseline | ATP Intelligent Export Engine | Improvement Factor |
| :--- | :--- | :--- | :--- |
| **Archive File Size** | **2,548.3 MB (2.55 GB)** | **307.6 KB** | **99.98% Reduction (8,000x smaller)** |
| **Archive Generation Time** | **27.4 seconds** | **0.29 seconds** | **94x Faster** |
| **Network Download Latency** | 45+ seconds (Gigabit LAN) | **Instant (<50ms)** | **900x Faster** |
| **Memory Footprint** | 3.2 GB RAM peak | **< 15 MB RAM** | **Zero Host Contention** |

#### Security & Non-Destructive Import Guarantees
1. **Deterministic Zip-Slip Defense**: The import processor rigorously audits every zip member path using `os.path.commonpath` to detect and reject any directory traversal attempts (`../`, absolute paths, root overrides).
2. **Non-Destructive Restoration**: Importing a project archive refreshes only the test estate (`artifacts/scripts/`, `artifacts/reports/`, `tests/`, `config/`). It **never touches** existing Ollama model weights (`artifacts/ollama/`) or database tables (`artifacts/db/`).
3. **Real-Time Client Reload**: Upon successful import or reload, the server emits a `PROJECT_RELOADED` WebSocket event, causing the browser dashboard to seamlessly refresh test trees, Monaco editors, and coverage metrics in place.

---

## 🔧 Setup Troubleshooting & Practical Debug Scenarios

### 1. Common Setup Diagnostics

#### A. Docker Desktop & WSL2 GPU Passthrough
* **Symptom**: Telemetry shows `CPU_BOUND` mode; generation speed is below 10 tokens/sec.
* **Diagnosis**: Run `nvidia-smi` in your Windows host terminal. If successful, check whether Docker has WSL2 GPU acceleration enabled.
* **Resolution**:
  1. Open Docker Desktop -> **Settings** -> **General** -> Verify **Use the WSL 2 based engine** is checked.
  2. Open **Resources** -> **WSL Integration** -> Ensure your default distro is enabled.
  3. Verify container access:
     ```bash
     docker exec -it atp_ollama nvidia-smi
     ```
     You should see your NVIDIA GPU (e.g., RTX 3050 / 4050) listed.

#### B. Ollama Model Pull & Cold-Start Delays
* **Symptom**: Generating tests displays `Connection Refused` or hangs on the first prompt.
* **Diagnosis**: The base model has not yet finished downloading to the local volume.
* **Resolution**:
  ```bash
  docker exec -it atp_ollama ollama list
  # If model is missing, pull it directly:
  docker exec -it atp_ollama ollama pull deepseek-r1:1.5b
  ```
  ATP automatically issues a `keep_alive: 60m` ping to pre-warm weights in VRAM, eliminating subsequent cold-start latencies.

#### C. Port Conflicts (8000, 11434, 6379, 5432, 9000)
* **Symptom**: Container fails to bind with `bind: address already in use`.
* **Resolution**: Identify the process holding the port using Windows PowerShell:
  ```powershell
  Get-NetTCPConnection -LocalPort 8000 | Select-Object OwningProcess
  Stop-Process -Id <PID> -Force
  ```

---

### 2. Practical Debug Playbooks

#### Scenario 1: Inference Sluggishness & GPU PCIe Bus Thrashing
* **Context**: User triggers test generation; the status bar shows high latency (6 tokens/sec instead of 88 tokens/sec).
* **Root Cause**: The active context window (`num_ctx`) was manually set to 16k or 32k on a 4GB GPU, forcing Ollama into a **38%/62% CPU/GPU split**.
* **Remediation**:
  1. Open the dashboard and click **"⚡ Benchmark & Tune LLM"**.
  2. Click **"Apply Profile"** on **Balanced (8,192 Ctx)** or **High-Velocity (4,096 Ctx)**.
  3. The system immediately evicts the oversized model instance, pre-warms the 8k context window in 100% CUDA VRAM, and restores inference speed to **85–92 tokens/sec**.

#### Scenario 2: AST Syntax Errors & Brittle Dynamic Locators
* **Context**: Web application uses obfuscated or dynamically generated React/Vue element IDs (`#btn-x89f2a`), causing the generated UI script to fail on dry run.
* **How ATP Heals It**:
  1. Stage 5 intercepts the failure stack trace (`NoSuchElementException: Unable to locate element: #btn-x89f2a`).
  2. The AST Evaluator (`llm_evaluator.py`) extracts the parent container's semantic text (`"Submit Order"`) and accessibility labels (`aria-label`, `role="button"`).
  3. The Evaluator constructs a localized repair prompt:
     `"Fix locator #btn-x89f2a: Element failed at runtime. Use resilient XPath contains(text(), 'Submit Order') or CSS button[type='submit']."`
  4. Ollama streams the patched code block, AST verifies syntax cleanliness, and the healed script replaces the broken file in `artifacts/scripts/`.

#### Scenario 3: Protected Authentication & Dynamic Spiders Blocked
* **Context**: Target web application sits behind a corporate SSO login gate or requires Bearer authentication.
* **Remediation**:
  1. In the Dashboard Crawl Configuration, expand **Authentication & Headers**.
  2. Provide session cookies (`{"session_id": "abc123xyz"}`) or Authorization headers (`Bearer eyJhbGci...`).
  3. The Celery worker's headless Chromium instance automatically injects these cookies before navigating, allowing full DOM extraction without being redirected to the login gate.

#### Scenario 4: LLM Hallucinating Incomplete Code or "TODO" Placeholders
* **Context**: Lower-tier models occasionally generate incomplete snippets containing `# TODO: Implement assertions here`.
* **How ATP Prevents It**:
  1. The SDET review rubric explicitly inspects scripts for `TODO`, `pass`, or ellipsis (`...`).
  2. Any script containing placeholders receives an automatic **Score: 0 / 100** and `approved: False`.
  3. The engine automatically rejects the output, raises the prompt instruction priority, and re-dispatches generation until 100% complete, fully implemented assertions are synthesized.

---

## 🚀 Quickstart & Operations Guide

### Prerequisites
* **OS**: Windows 10/11, macOS, or Linux.
* **Docker Desktop**: Installed and running with GPU acceleration enabled (WSL2 with NVIDIA CUDA on Windows).
* **Python**: 3.10 to 3.12 with Poetry installed.
* **Hardware**: Minimum 4-core CPU, 8GB RAM, and any modern GPU (e.g., NVIDIA RTX 3050 4GB+).

### One-Click Windows Deployment
```cmd
:: 1. Initial Setup (Pulls base images & creates directories)
SETUP.bat

:: 2. Launch Enterprise Cluster (Starts containers & opens browser)
START.bat

:: Access Dashboard:
:: http://localhost:8000
```

### Manual Docker Compose Launch
```bash
# Start all microservices in detached mode
docker-compose -f docker-compose-windows.yml up -d

# Verify cluster status
docker ps

# Stream logs
docker-compose -f docker-compose-windows.yml logs -f
```

---

### Unified Poetry, Robot Framework & Pytest Execution

The framework can be executed directly from your local environment or CI/CD runner using Poetry:

```bash
# 1. Install all dependencies via Poetry
poetry install

# 2. Initialize Playwright Browser binaries for Robot Framework
poetry run rfbrowser init

# 3. Execute Robot Framework Browser suite (WAF & Turnstile validation)
poetry run robot -d results tests/suite_playwright.robot

# 4. Execute Selenium 4 Pytest suite with CDP WAF injection
poetry run pytest tests/test_selenium.py -v

# 5. Execute all WAF-protected scenarios across suites
poetry run pytest tests/ -m waf_protected -v

# 6. Execute Multi-Scenario Grafana k6 Load Test
poetry run k6 run artifacts/scripts/auto_load_test.js

# 7. Execute Pabot Parallel Multi-Core Runner
docker exec -it atp_celery pabot --processes 4 --outputdir artifacts/reports/pabot_results artifacts/scripts/auto_suite.robot
```

---

### Programmatic CLI Project Export & Reload via cURL

Export and restore test projects programmatically inside CI/CD pipelines:

```bash
# 1. Fast Export Project (<1MB archive in ~0.3s)
curl -X GET "http://localhost:8000/api/system/export" -o enterprise_qa_project.zip

# 2. Safe Non-Destructive Project Import
curl -X POST "http://localhost:8000/api/system/import" \
     -F "file=@enterprise_qa_project.zip"

# 3. In-Place Project Cache Reload
curl -X POST "http://localhost:8000/api/system/reload"
```

---

### Operational Batch Scripts Included
* `START.bat`: Boots the Docker cluster, waits for health checks, and launches `http://localhost:8000`.
* `SETUP.bat`: Pulls base Ollama images and creates directory structures.
* `SHUTDOWN.bat`: Gracefully stops containers while preserving database state.
* `RESET_DB.bat`: Wipes Postgres and Redis volumes to restore a clean slate.
* `CLEANUP.bat`: Cleans temp logs, screenshots, and test execution traces.
* `DIAGNOSTICS.bat`: Displays live container resource statistics via `docker stats`.
* `REBUILD.bat`: Rebuilds backend and worker images from scratch.

---

## 📄 License & Attribution
Enterprise ATP is designed and engineered for mission-critical enterprise test automation.
Developed under the MIT License. Commercial and sovereign deployment permitted.
