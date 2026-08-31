--- QUIZ ---

1. An enterprise developer needs Claude to parse unformatted legacy logs into JSON payloads matching a schema. Which prompting strategy ensures the highest structural reliability?

* A) Include detailed XML tags (`<example>`, `<schema>`, `<rules>`) isolating input, desired output structure, and few-shot input-output pairs.
* B) Set a high temperature parameter and write the output instructions using all-capital letters.
* C) Repeat the JSON schema multiple times throughout the user prompt to artificially increase internal model attention weights.
* D) Use open-ended chain-of-thought instructions without providing concrete sample JSON objects.

2. A complex legacy migration request requires analyzing monolithic code, designing microservices, generating OpenAPI specs, and writing unit tests. Which task decomposition strategy produces the most reliable output?

* A) Instruct Claude in a single prompt to execute all migration tasks simultaneously in one output stream.
* B) Break the workflow into sequential sub-tasks: analyze dependencies, outline service boundaries, generate OpenAPI specs per service, and produce unit tests in distinct prompt steps.
* C) Ask Claude to loop internally without returning intermediate outputs until the entire migration is complete.
* D) Provide all source code files at once and request microservice skeletons without specifying execution order.

3. An enterprise team notices Claude produces overly generic strategic recommendations when analyzing market reports. To iterate and improve prompt quality for deep technical analysis, which prompt modification is most effective?

* A) Append "Be extremely detailed and act as an expert" to the end of the existing prompt.
* B) Provide explicit evaluation criteria, define required analytical frameworks, and mandate negative constraints such as excluding high-level buzzwords.
* C) Replace specific domain jargon with simplified everyday vocabulary.
* D) Remove background context to allow the model maximum creative freedom.

4. A financial analyst uses Claude to evaluate contrasting macroeconomic forecasts. Which prompting technique best adapts Claude’s approach specifically for high-rigor comparative research?

* A) Direct Claude to immediately draft an executive memo favoring the first forecast provided.
* B) Require Claude to construct a structured pros-and-cons matrix, explicitly analyze underlying assumptions for each forecast, and cite supporting evidence before drawing conclusions.
* C) Set system instructions to enforce short, single-sentence responses to limit analytical depth.
* D) Ask Claude to brainstorm fictional economic scenarios to supplement the actual research data.

5. A software security team needs Claude to conduct strict compliance audits on Python infrastructure-as-code scripts. How should the prompt be framed to maximize audit rigor?

* A) Define a precise role persona ("Senior Cloud Security Engineer"), set explicit regulatory standards like CIS Benchmarks, and mandate reporting violations with line numbers.
* B) Ask Claude to review the scripts as a general assistant and highlight anything that looks unusual.
* C) Instruct Claude to rewrite the code to make it look shorter and more modern.
* D) Request that Claude generate a positive summary explaining why the infrastructure is already secure.

6. When prompting Claude to generate a complex multi-file Rust application, what is the best structural technique to ensure clean separation of files without missing implementation details?

* A) Request all code to be written in a single inline block without file paths or comments.
* B) Direct Claude to use explicit file wrapper XML tags (such as `<file path="src/main.rs">`) and enforce complete implementation for each component without placeholders.
* C) Instruct Claude to omit boilerplate code and use placeholder comments like `// implement later` for complex logic.
* D) Ask Claude to describe the architecture verbally rather than outputting code files.

7. A data scientist asks Claude to solve a multi-step probability puzzle, but the model makes arithmetic errors when generating final answers immediately. How should the prompt be restructured?

* A) Force Claude to output the final numerical answer as the very first word in its response.
* B) Instruct Claude to think through the problem step-by-step inside `<scratchpad>` or `<thinking>` tags before presenting the final answer.
* C) Request the answer in binary format to simplify calculation steps.
* D) Tell Claude that the math problem is simple and requires no calculation steps.

8. A product design team uses Claude for iterative brainstorming. After 15 turns, response quality degrades due to context drift. What strategy best restores optimal output quality?

* A) Continue the existing conversation while typing "Focus!" at the start of every turn.
* B) Summarize key decisions and constraints established so far, then launch a fresh session with that summary as the starting context.
* C) Paste the entire 15-turn transcript into every new user message going forward.
* D) Switch to a shorter prompt format while omitting previously agreed constraints.

9. A developer reviews a Claude-generated SQL query designed for PostgreSQL that includes a function named `STRING_AGG_DISTINCT()`. How should the developer evaluate this output?

* A) Accept the query as valid because Claude natively validates SQL syntax before responding.
* B) Identify `STRING_AGG_DISTINCT()` as a probable hallucination, as standard PostgreSQL uses `STRING_AGG(DISTINCT ...)` syntax, requiring manual syntax verification.
* C) Execute the query directly in production since LLM code is automatically optimized for database engines.
* D) Assume the function is a proprietary PostgreSQL extension created by Claude.

10. A technical writer asks Claude to generate a comprehensive 3,000-word API reference document along with interactive visual diagrams. Which output format selection strategy is most appropriate?

* A) Request the entire guide as inline plain text within the primary chat window to avoid UI sidebars.
* B) Direct Claude to generate the standalone documentation and architecture diagrams as dedicated visual/code Artifacts for modular editing and rendering.
* C) Force output into a single-line JSON string to simplify raw text extraction.
* D) Require output to be split across 50 individual chat messages without saving artifacts.

11. An enterprise risk team uses Claude to summarize regulatory compliance updates. To validate that the summary contains no fabricated rules or omitted mandates, which procedure should be required?

* A) Trust the summary if Claude expresses high confidence in its introductory paragraph.
* B) Cross-reference every extracted policy statement against source regulatory texts using automated citation mapping and mandatory human-in-the-loop audit.
* C) Re-run the exact prompt three times and accept the output if two of the responses match word-for-word.
* D) Ask Claude in the same session whether the summary contains any mistakes.

12. In a generated software architecture proposal, Claude recommends using a serverless function architecture for real-time video rendering, but later notes that individual request execution time is hard-limited to 60 seconds. What evaluation verdict should the system architect reach?

* A) The proposal contains an internal logical contradiction because long-running video processing will hit serverless timeout limits.
* B) The proposal is fully valid because serverless functions scale infinitely regardless of execution timeouts.
* C) Claude intentionally included this contradiction as a standard benchmarking test for architects.
* D) The execution timeout is irrelevant to architectural selection.

13. A legal department leverages Claude to analyze third-party vendor contracts. Which output scenario strictly requires mandatory human legal counsel intervention before action is taken?

* A) Claude extracts all party names and contract start dates accurately into a JSON object.
* B) Claude identifies standard boilerplate confidentiality clauses that match company templates.
* C) Claude flags ambiguous indemnity language and proposes modified liability terms for high-risk indemnification.
* D) Claude formats the contract text with standardized Markdown headers.

14. A senior developer receives a dense, jargon-heavy technical explanation from Claude regarding a database lock escalation issue. The developer needs to present this issue to non-technical executive stakeholders. How should the output be refined?

* A) Forward the original technical output directly without modification to maintain complete detail.
* B) Prompt Claude to re-frame the issue using business-impact metrics such as downtime risk and revenue effect while abstracting low-level thread locks.
* C) Translate the technical explanation into machine code hex dumps for executive presentation.
* D) Delete the explanation and provide only raw database server CPU utilization logs.

15. Claude is tasked with generating a Python user registration function. Upon code review, the engineer notes the function handles valid input and database insertion, but lacks input sanitization, error handling, and duplicate email checks. What is the correct quality evaluation of this output?

* A) Complete, because the primary happy-path functional requirement was met.
* B) Incomplete and insecure, as critical edge cases, validation, and security exception handling were omitted.
* C) Optimal, because adding security logic increases token overhead unnecessarily.
* D) Complete, because error handling is automatically handled by the Python runtime.

16. A front-end developer requires Claude to output data suitable for direct consumption by a REST API response parser. Which format and prompt constraint best ensures seamless machine readability?

* A) Request markdown text with conversational commentary surrounding key-value pairs.
* B) Enforce a strict JSON schema enclosed in `<json>` XML tags, explicitly forbidding conversational preamble or postscript text.
* C) Ask Claude to render data as an informal bulleted list using mixed indents.
* D) Direct Claude to return a styled HTML table with embedded CSS classes.

--- ANSWER KEY ---

Question 1: A

Explanation: Using structured XML tags (`<example>`, `<schema>`, `<rules>`) and few-shot examples clearly demarcates prompt components, significantly improving structural adherence for data parsing tasks.

Question 2: B

Explanation: Complex engineering tasks perform best when decomposed into sequential, modular steps rather than attempting single-pass generation of an entire system architecture.

Question 3: B

Explanation: Explicit evaluation criteria, structured analytical frameworks, and negative constraints provide clear boundaries that eliminate generic boilerplate responses.

Question 4: B

Explanation: Analytical and comparative research tasks require explicit directives to evaluate underlying assumptions, construct structural comparisons, and ground conclusions in evidence.

Question 5: A

Explanation: High-rigor domain tasks benefit from role personas, explicit standards/benchmarks, and concrete output requirements like specifying precise line numbers.

Question 6: B

Explanation: XML file tags provide clean delimiters for multi-file generation, ensuring code blocks are explicitly bounded and complete without relying on placeholders.

Question 7: B

Explanation: Chain-of-thought prompting using designated tags (like `<scratchpad>` or `<thinking>`) allows the model to compute intermediate reasoning steps before generating the final answer, preventing logic and calculation errors.

Question 8: B

Explanation: Summarizing past context and starting a fresh session clears cumulative context noise and prevents degradation from context drift in long multi-turn chats.

Question 9: B

Explanation: LLMs can hallucinate non-existent API or SQL methods; validating output against official technical specifications (like PostgreSQL syntax) is essential during output evaluation.

Question 10: B

Explanation: Large modular content such as extensive documentation and code visual renders are best managed via Artifacts for side-by-side editing, rendering, and export.

Question 11: B

Explanation: High-risk domains require rigorous fact-checking through citation mapping against primary sources and mandatory human review to verify accuracy.

Question 12: A

Explanation: Evaluating LLM outputs requires identifying internal logical inconsistencies, such as pairing long-running compute workloads with strict serverless execution timeouts.

Question 13: C

Explanation: Substantive legal decisions, indemnity modifications, and risk allocations require expert human review, whereas routine data extraction or formatting carries lower risk.

Question 14: B

Explanation: Refining output for target audiences involves translating domain-specific technical details into audience-appropriate metrics, business impacts, and high-level summaries.

Question 15: B

Explanation: Thorough evaluation assesses non-functional requirements and edge cases; omitting error handling and input sanitization renders code incomplete and production-unsafe.

Question 16: B

Explanation: Programmatic consumption requires clean, structured data (e.g., JSON in explicit tags) free of conversational preambles or markdown wrappers that break parsers.
