---
layout: resume
---

<div class="content-section">
  <div class="section-header">
    <h2>Projects</h2>
  </div>

  <div class="resume-item">
    <h3 class="resume-item-title">Multi-node self-hosted inference platform</h3>
    <div class="resume-item-copy">
      <ul>
      <li>LLM serving across an AMD Strix Halo node (ROCm, gfx1151, 128 GB unified memory) and a dual RTX 3090 node (CUDA), behind an nginx routing and load-balancing proxy; tensor-parallel split for ~2× throughput over layer split, with speculative decoding, KV-cache quantization, and prompt caching benchmarked per backend — the tradeoffs do not transfer; Strix Halo power/curve tuning tooling published at <a href="https://github.com/leo-3889/strixhalo-undervoltfinder">github.com/leo-3889/strixhalo-undervoltfinder</a>.</li>
      <li>Hunted a speculative-decoding/prompt-cache interaction causing silent cold-path fallbacks and shipped a workaround; added an SSE keep-alive shim after client HTTP stacks were found aborting long prefills before first token.</li>
      <li>Calibrated GPU memory allocation and continuous-batching configuration for a vLLM deployment on AMD ROCm and NVIDIA CUDA back-to-back, verified the configuration under sustained load and post-deployment API health.</li>
      </ul>
    </div>
  </div>

  <div class="resume-item">
    <h3 class="resume-item-title">Multi-agent coding system</h3>
    <div class="resume-item-copy">
      <ul>
      <li>Role-scoped subagents with MCP servers for persistent memory and issue tracking, routed through a self-hosted gateway rather than a vendor endpoint. Enforced a write-then-verify loop — render verification on every issue write — after production runs surfaced silent formatting failures, and documented the API constraints as reusable agent rules.</li>
      </ul>
    </div>
  </div>

  <div class="resume-item">
    <h3 class="resume-item-title">LLM observability &amp; release-validation stack</h3>
    <div class="resume-item-copy">
      <ul>
      <li>Designed a local LLM observability architecture spanning inference endpoints, power telemetry, Telegraf, InfluxDB, and Grafana; defined data contracts for endpoint health, inference performance, energy use, and per-token cost and TCO reporting across multiple model runtimes (Ollama, vLLM, llama.cpp, Radiance); maintained public MQTT→Telegraf→InfluxDB→Grafana stack at <a href="https://github.com/leo-3889/OpenDTU-Grafana-Stack">github.com/leo-3889/OpenDTU-Grafana-Stack</a>.</li>
      <li>Audited a 61-panel Grafana dashboard and its data pipeline end to end, identifying calculation, query, display, and service-health defects that blocked acceptance; established release criteria tracing every requirement to an executed test and validating rendered dashboard values, units, and labels against source data.</li>
      <li>Designed migration and rollback plans for telemetry changes while protecting existing dashboards and live data collection; diagnosed ambiguous operational failures through staged isolation across Windows, Linux, Docker, SSH, APIs, and application state.</li>
      </ul>
    </div>
  </div>
</div>

<div class="content-section">
  <div class="section-header">
    <h2>Work Experience</h2>
  </div>

  <div class="resume-item">
    <h3 class="resume-item-title">Senior Solution Architect</h3>
    <h4 class="resume-item-details">Thales, Munich, Germany • 2020 – Present</h4>
    <div class="resume-item-copy">
      <ul>
      <li>Delivered a RAG-grounded metadata classification and enrichment service into a defense customer's accredited environment: retrieval over the customer requirements corpus grounded every generated enrichment; embeddings and inference on locally hosted fine-tuned models where API-based services were not permitted; updates gated by an acceptance suite with customer-validated golden-set accuracy; in production across 3 deployments.</li>
      <li>Designed and deployed production agentic AI systems (MCP, CrewAI, LlamaIndex, fine-tuned open models) automating requirement analysis and solution scoping. Cut spec turnaround by roughly a third across 12 EMEA engagements.</li>
      <li>Positioned AI-enabled deliveries for regulated and accredited environments — data residency, local-only inference, and auditability — aligned with EU AI Act obligations in force from August 2026.</li>
      <li>Owned 6 large enterprise buying cycles a year for Thales Software Monetization — technical qualification, demos, and PoCs with sales and business development, through post-sale integration across SaaS, on-prem data-center, and hybrid deployments.</li>
      <li>Owned cloud architecture end to end from design to production, raising supported user capacity 40%; the resulting blueprints became the EMEA reference for complex integrations.</li>
      <li>Brokered architecture decisions between customer executives up to VP and CTO level, delivery partners, and Thales R&amp;D across EMEA — converting technical constraints into funded business decisions.</li>
      <li>Mentored 3 engineering and integration leads on DevSecOps and AI-assisted development; the approach was adopted across the wider team, and one mentee has since moved into an architect role; interviewed 3 candidates for team hiring.</li>
      </ul>
    </div>
  </div>

  <div class="resume-item">
    <h3 class="resume-item-title">Solution Architect</h3>
    <h4 class="resume-item-details">Rohde &amp; Schwarz, Munich, Germany • 2018 – 2020</h4>
    <div class="resume-item-copy">
      <ul>
      <li>Owned solution architecture for large-scale defense and government communication systems under strict compliance regimes; microservice PoCs built along the way (Spring Boot, RabbitMQ, Docker) — 3 adopted into production roadmaps.</li>
      <li>Introduced event-driven architecture with ML-based telemetry classification and anomaly detection, which became the basis for operational monitoring.</li>
      <li>Led distributed engineering teams across Munich and Singapore as people manager of 3 direct reports, driving architecture reviews and CI/CD adoption for mission-critical systems.</li>
      </ul>
    </div>
  </div>

  <div class="resume-item">
    <h3 class="resume-item-title">Technical Project Manager</h3>
    <h4 class="resume-item-details">Fidor Solutions (BPCE), Munich, Germany • 2016 – 2018</h4>
    <div class="resume-item-copy">
      <ul>
      <li>Launched a digital banking product for the French market on schedule, coordinating cross-continental engineering and delivery teams.</li>
      <li>Cut customer churn 28% with Python churn-prediction models feeding retention campaigns.</li>
      <li>Defined integration strategy for core banking and mobile payments (Apple Pay, Android Pay) under multi-market regulatory constraints.</li>
      </ul>
    </div>
  </div>

  <div class="resume-item">
    <h3 class="resume-item-title">Solutions Architect</h3>
    <h4 class="resume-item-details">Uniscon GmbH, Munich, Germany • 2015</h4>
    <div class="resume-item-copy">
      <ul>
      <li>Defined the reference architecture for a startup cloud platform and owned the technical roadmap as lead of a 6-person cross-functional team; built the microservices backend (Spring, Kafka, Docker, Jetty).</li>
      <li>Cut computation time 50% through hands-on performance optimization; redesigned the REST API layer into the team standard.</li>
      </ul>
    </div>
  </div>

  <div class="resume-item">
    <h3 class="resume-item-title">Full Stack Engineer</h3>
    <h4 class="resume-item-details">Trustonic GmbH, Munich, Germany • 2013 – 2015</h4>
    <div class="resume-item-copy">
      <ul>
      <li>Led full-stack development of a Trusted Execution Environment framework in a 4-person team; migrated 10+ year legacy codebases onto Jenkins pipelines and owned Samsung/SKT technical accounts including on-site delivery and SLAs.</li>
      <li>Shipped an Android system app pre-installed on all Samsung Galaxy smartphones — 50M+ devices, in production for years after release.</li>
      </ul>
    </div>
  </div>

  <div class="resume-item">
    <h3 class="resume-item-title">Full Stack Engineer (R&amp;D)</h3>
    <h4 class="resume-item-details">Dental Wings Inc., Montreal, Canada • 2013</h4>
    <div class="resume-item-copy">
      <ul>
      <li>Led REST API analysis and optimization for a 4-engineer backend team; the resulting specifications were adopted as the team standard and the performance work was prioritized into the product roadmap.</li>
      </ul>
    </div>
  </div>
</div>

<div class="content-section">
  <div class="section-header">
    <h2>Education</h2>
  </div>

  <div class="resume-item">
    <h3 class="resume-item-title">M.Sc. — Engineer Program, IT Networks &amp; Telecommunications</h3>
    <h4 class="resume-item-details">Polytech Engineering School (Grandes Écoles) • 2010 – 2013</h4>
  </div>

  <div class="resume-item">
    <h3 class="resume-item-title">B.Sc. — ITCom (Information Technology and Communication)</h3>
    <h4 class="resume-item-details">Metropolia University of Applied Sciences • 2009 – 2010</h4>
  </div>

  <div class="resume-item">
    <h3 class="resume-item-title">Technical Bachelor Degree (DUT) — Networks and Communications</h3>
    <h4 class="resume-item-details">IUT1, Joseph Fourier University • 2007 – 2009</h4>
  </div>
</div>

<div class="content-section">
  <div class="section-header">
    <h2>Skills &amp; Additional</h2>
  </div>

  <div class="resume-item">
    <h3 class="resume-item-title">Technical Skills</h3>
    <ul>
      <li><strong>AI &amp; agentic systems:</strong> LLM application architecture, RAG, multi-agent workflows, MCP, fine-tuning (PyTorch, Hugging Face), LLM evaluation, guardrails, LLMOps, AI governance in regulated environments, self-hosted inference (llama.cpp, vLLM, CUDA/ROCm)</li>
      <li><strong>Engineering:</strong> Python, TypeScript / Node.js, Java (Spring)</li>
      <li><strong>Platforms:</strong> AWS, Kubernetes, Docker, Kafka, PostgreSQL, GitHub Actions / GitLab CI</li>
      <li><strong>Architecture:</strong> Cloud-native and event-driven design, microservices, API strategy (REST, gRPC)</li>
      <li><strong>Observability &amp; operations:</strong> Telegraf, InfluxDB, Grafana, power/cost telemetry, release validation, staged diagnostics (Windows / Linux / Docker / SSH)</li>
      <li><strong>Leadership:</strong> technical team leadership and people development, pre-sales qualification and customer engagement, executive stakeholder communication, multi-region delivery (EMEA, APAC)</li>
    </ul>
  </div>

  <div class="resume-item">
    <h3 class="resume-item-title">Certifications &amp; Training</h3>
    <ul>
      <li>Generative AI with Large Language Models — DeepLearning.AI</li>
      <li>SAFe Agilist — Scaled Agile</li>
      <li>Certified Scrum Product Owner (CSPO) — Scrum Alliance</li>
      <li>ITIL v4 Foundation — Axelos</li>
      <li>NVIDIA-Certified Professional: Generative AI LLMs (NCP-GENL) — NVIDIA</li>
    </ul>
  </div>

  <div class="resume-item">
    <h3 class="resume-item-title">Languages</h3>
    <ul>
      <li>French (native) · German (fluent) · English (fluent) · Finnish (basic)</li>
    </ul>
  </div>
</div>
