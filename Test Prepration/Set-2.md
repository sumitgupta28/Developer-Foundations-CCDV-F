--- QUIZ ---

1. An enterprise architecture team is designing prompts for complex legal contract analysis. To ensure Claude parses sub-clauses, identifies risk vectors, and outputs structured findings without skipping ambiguous sections, which prompting approach is most effective?

* A) Ask Claude to perform the complete analysis in one single-sentence prompt to minimize token overhead.
* B) Implement multi-step task decomposition combined with explicit thinking directives for intermediate reasoning before generating structured XML output.
* C) Enforce high temperature settings so Claude creatively interprets ambiguous clauses.
* D) Repeat the contract text three times in the prompt to force internal attention layers to highlight key clauses.

2. During an automated validation run of Claude-generated Python code, a CI job fails because Claude invoked `pandas.DataFrame.to_parquet_stream()`, a method that does not exist in the pandas library. How should the team classify and address this failure?

* A) Classify it as a context length failure and resolve it by doubling the output token limit.
* B) Classify it as a model hallucination and resolve it by providing explicit library version specs and API reference documentation in the prompt context.
* C) Classify it as a syntax error and resolve it by setting the model temperature to maximum.
* D) Classify it as an authentication error and re-generate API keys.

3. A high-frequency logistics company requires real-time routing triage for 500,000 package events per hour. The system requires low sub-second latency and minimal cost per request while extracting origin, destination, and priority tags into strict JSON schemas. Which model selection strategy is optimal?

* A) Claude Opus operating in research mode.
* B) Claude Haiku optimized for high-throughput, low-latency structured extraction.
* C) Claude Sonnet with extended visual artifacts rendering enabled.
* D) Claude Opus configured with maximum multi-turn chat persistence.

4. A developer is building an interactive long-session coding assistant using Claude. After 30 consecutive conversation turns, the developer notices response latency increasing and Claude occasionally violating initial system instructions. What context management strategy best resolves this?

* A) Persist the full raw transcript indefinitely and increase the top-p parameter after turn 20.
* B) Periodically summarize active context, clear historical turn logs, and re-inject core system instructions into a clean session window.
* C) Switch to a smaller model while retaining the degraded transcript history.
* D) Append "Do not forget original instructions" to every new user prompt in the active session.

5. An organization plans to integrate Claude into its incident response management workflow to automate post-mortem generation from incident chat logs and telemetry data. Which solution design pattern ensures both automated efficiency and operational accuracy?

* A) Fully automate direct deployment of post-mortems to external stakeholders without human intervention.
* B) Use Claude to summarize logs and draft post-mortems into an interactive document Artifact, requiring mandatory review by an Incident Commander prior to publication.
* C) Pipeline raw incident logs into Claude continuously without filtering sensitive authorization tokens or server passwords.
* D) Restrict Claude to generating plain text terminal commands while disabling structured outputs.

6. A technical product manager needs to explain the architectural trade-offs of using LLM agent workflows versus deterministic rules engines to executive stakeholders. What is the most accurate depiction of Claude’s operational capabilities and limitations?

* A) Claude provides 100% deterministic outputs suitable for replacing all relational database query engines.
* B) Claude excels at reasoning over unstructured data, adapting to varied natural language inputs, and executing complex workflows, but requires validation mechanisms for strict accuracy guarantees.
* C) Claude operates latency-free and requires zero compute resources when running enterprise workflows.
* D) Claude cannot execute structured data extraction or multi-step reasoning under any conditions.

7. A team is setting up a Claude Project to support a customer support engineering team. They have 10 separate PDF manuals and dynamic product release notes updated daily. What configuration strategy best balances knowledge stability and freshness?

* A) Hardcode all daily release notes directly into the static Project Instructions text field.
* B) Upload core, stable PDF manuals to Project Knowledge, and utilize dynamic API connectors or context-injected release notes for daily updates.
* C) Paste the contents of all PDFs into every individual customer support chat message.
* D) Delete the Project Knowledge base daily and manually re-upload all static PDFs alongside new release notes.

8. While authoring Project Instructions for a custom Claude Project, a developer notices that Claude frequently outputs conversational greetings despite an instruction stating "Be concise." What refinement to the system instructions best eliminates this behavior?

* A) Write "PLEASE BE CONCISE" in all capital letters 10 times in the prompt.
* B) Provide explicit negative constraints paired with positive operational directives, such as "Do not include introductory greetings or postscripts; begin responses immediately with requested data."
* C) Increase the temperature parameter to 1.0 to force stricter rule adherence.
* D) Move the conciseness instruction into a separate PDF file uploaded to Project Knowledge.

9. A healthcare technology platform wants to leverage Claude to draft patient communication letters based on clinical EHR summaries. According to health data governance and compliance requirements (e.g., HIPAA), how must the system be architected?

* A) Send unencrypted raw patient EHR records directly through public chat endpoints.
* B) De-identify or anonymize Protected Health Information (PHI) prior to API transmission, ensure enterprise data privacy agreements are active, and enforce human clinical review before sending letters to patients.
* C) Request Claude to automatically promise patients that their health data will never be stored by any cloud system.
* D) Rely on Claude’s internal guardrails to automatically scrub PHI without pre-processing pipeline checks.

10. A prompt intended to extract structured financial metrics from quarterly earnings reports produces inconsistent key names across execution runs (e.g., returning `total_revenue` in run 1 and `rev_total` in run 2). What optimization fix guarantees key name consistency?

* A) Enforce a strict JSON schema with explicitly defined key names and provide few-shot examples demonstrating the precise output structure.
* B) Raise the temperature parameter to promote structural variety in outputs.
* C) Re-phrase the prompt request using polite conversational phrasing.
* D) Run the extraction task only during off-peak computing hours.

--- ANSWER KEY ---

Question 1: B

Explanation: Task decomposition breaks complex analysis into manageable sub-tasks, while thinking directives give the model reasoning space to evaluate sub-clauses prior to generating structured XML outputs.

Question 2: B

Explanation: Generating non-existent API functions is a classic hallucination; providing official library documentation and version boundaries grounds the model's output in factual API signatures.

Question 3: B

Explanation: Claude Haiku offers the lowest latency and cost per token, making it the ideal choice for massive-scale, real-time structured data parsing and categorization.

Question 4: B

Explanation: Context window accumulation causes latency increases and prompt drift; summarizing key context and re-initializing clean chat sessions maintains high performance and compliance with system instructions.

Question 5: B

Explanation: Critical operational workflows benefit from human-in-the-loop review, using Claude to generate editable Artifacts while requiring domain experts (Incident Commanders) to authorize external releases.

Question 6: B

Explanation: LLMs excel at reasoning over complex unstructured context, but because they operate probabilistically, enterprise workflows must incorporate verification mechanisms for high-stakes accuracy.

Question 7: B

Explanation: Project Knowledge is best reserved for stable, core reference materials, whereas rapidly changing dynamic data should be supplied via API connectors or dynamic context injection to avoid stale knowledge base issues.

Question 8: B

Explanation: System instructions are most effective when combining explicit negative constraints ("Do not include greetings") with direct positive directives specifying the exact desired output behavior.

Question 9: B

Explanation: Regulatory compliance frameworks like HIPAA mandate PHI de-identification/anonymization at the data pipeline layer, zero-data-retention enterprise agreements, and mandatory human clinician verification before patient delivery.

Question 10: A

Explanation: Structuring prompts with explicit JSON schemas and concrete few-shot examples eliminates structural ambiguity, ensuring deterministic key naming across independent execution runs.
