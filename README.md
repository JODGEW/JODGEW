# Hey, I'm Wenhao He :wave:

**Software engineer, New York.** Two years full-stack, building production AI applications — LLM pipelines, agentic RAG, and the evaluation harnesses that tell you whether any of it actually works. I designed, shipped, and operate [ResumeMatch](https://resumematchapp.com) solo.

[![My Skills](https://skillicons.dev/icons?i=py,ts,js,java,react,nextjs,nodejs,fastapi,spring,graphql,postgres,mongodb,aws,azure,docker,kubernetes,kafka,pytorch,git,githubactions)](https://skillicons.dev)

### :computer: About Me

* 🎓 **M.S. Engineering Science (AI)** and **B.S. Computer Science**, University at Buffalo · **AWS Certified Developer – Associate**
* 🏗️ Full-stack at two NYC startups before this — GraphQL ordering systems at **Clipp**, Azure Form Recognizer document intake at **CAN International**
* 🔬 What I care about most: making AI systems *measurable*. Evidence guards, frozen holdouts, offline evals — the unglamorous part that tells you whether the model is actually right.

### 🛠️ What I've Built

**[ResumeMatch](https://resumematchapp.com)** — serverless AI resume analyzer on AWS, live in production, built and operated solo · [frontend](https://github.com/JODGEW/ResumeMatch) · [backend](https://github.com/JODGEW/ResumeMatch-backend)

* Built an offline eval harness (10 resumes × 3 model configs, 60 runs) that caught the AI proposing keywords the source resume didn't support in **22 of 31 edits — 71%**. Shipped a deterministic evidence guard that drops them at generation time; **26 rejections in production** since.
* Cut repeat analyses from a **34s median to 20ms** with a SHA-256-hashed DynamoDB cache, and halved per-run model cost by routing extraction to Haiku 4.5 and only generation to Sonnet 4.6 — **~$0.05 per analysis**.
* `Python · Lambda · Bedrock · Textract · DynamoDB · Cognito · CloudFront · React · TypeScript`

**[Financial Document Intelligence Agent](https://github.com/JODGEW/Financial-Document-Intelligence-Agent)** — governance-first RAG/ReAct agent over SEC filings

* Context-policy admission drops chunks **before the model sees them**, plus Bedrock Guardrails and a per-answer JSONL audit trail across **689 logged runs**.
* Then caught my own trust layer being wrong: it scored claims against 700-char-capped excerpts, so figures deeper in a chunk read as unsupported. The fix moved a frozen 32-case baseline from **6.4% → 2.9%** unsupported claims.
* `Python · FastAPI · React · Bedrock (Haiku 4.5, Titan v2) · LangChain · Chroma`

**[Order Processing System](https://github.com/JODGEW/Order-Processing-System)** — event-driven, built around the failure cases rather than the happy path

* Transactional outbox makes PostgreSQL → Kafka event publication reliable across service outages; a `processed_events` ledger with uniqueness constraints gives consumers idempotency under retry and redelivery.
* `Java · Spring Boot · Kafka · PostgreSQL · Docker · Kubernetes`

**Also shipped:** [Food Map](https://food-map-next.vercel.app) ([repo](https://github.com/JODGEW/Food-Map)) — Next.js 16 dining journal where Clerk issues tokens Supabase trusts as a JWT issuer, so Row-Level Security enforces per-user isolation in Postgres rather than app code · [My blog](https://blog.wenhaohe.com) ([repo](https://github.com/JODGEW/personal-blog)) — Next.js 15 + MongoDB, rewritten from an earlier Express app

### 🚀 What I'm Looking For

I'm seeking opportunities as a **Software Engineer (Full-Stack)**, **Backend Engineer**, or **Applied AI / Machine Learning Engineer** where I can build scalable products, intelligent systems, and cloud-native applications that deliver real user impact.

### 🌐 Connect With Me

- 🔗 [LinkedIn](https://www.linkedin.com/in/wenhao-he-77126a230/)
- 💻 [Personal Website](https://wenhaohe.com)
- 📱 [ResumeMatch App](https://resumematchapp.com)
