[Anthropic home page![light logo](https://mintlify.s3.us-west-1.amazonaws.com/anthropic/logo/light.svg)![dark logo](https://mintlify.s3.us-west-1.amazonaws.com/anthropic/logo/dark.svg)](https://docs.anthropic.com/)
English
Search...
Ctrl K
  * [Research](https://www.anthropic.com/research)
  * [News](https://www.anthropic.com/news)
  * [Go to claude.ai](https://claude.ai/)
  * [Go to claude.ai](https://claude.ai/)


Search...
Navigation
Prompt engineering
Be clear, direct, and detailed
[Welcome](https://docs.anthropic.com/en/home)[User Guides](https://docs.anthropic.com/en/docs/welcome)[API Reference](https://docs.anthropic.com/en/api/getting-started)[Claude Code](https://docs.anthropic.com/en/docs/claude-code/overview)[Prompt Library](https://docs.anthropic.com/en/prompt-library/library)[Release Notes](https://docs.anthropic.com/en/release-notes/overview)
* [Developer Console](https://console.anthropic.com/)
* [Developer Discord](https://www.anthropic.com/discord)
* [Support](https://support.anthropic.com/)
##### Get started
  * [Overview](https://docs.anthropic.com/en/docs/welcome)
  * [Initial setup](https://docs.anthropic.com/en/docs/initial-setup)
  * [Intro to Claude](https://docs.anthropic.com/en/docs/intro-to-claude)


##### Learn about Claude
  * Use cases
  * Models
  * [Pricing](https://docs.anthropic.com/en/docs/about-claude/pricing)
  * [Security and compliance](https://trust.anthropic.com/)


##### Build with Claude
  * [Define success criteria](https://docs.anthropic.com/en/docs/build-with-claude/define-success)
  * [Develop test cases](https://docs.anthropic.com/en/docs/build-with-claude/develop-tests)
  * [Context windows](https://docs.anthropic.com/en/docs/build-with-claude/context-windows)
  * [Vision](https://docs.anthropic.com/en/docs/build-with-claude/vision)
  * Prompt engineering
    * [Overview](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview)
    * [Prompt generator](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-generator)
    * [Use prompt templates](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-templates-and-variables)
    * [Prompt improver](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver)
    * [Be clear and direct](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/be-clear-and-direct)
    * [Use examples (multishot prompting)](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/multishot-prompting)
    * [Let Claude think (CoT)](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/chain-of-thought)
    * [Use XML tags](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/use-xml-tags)
    * [Give Claude a role (system prompts)](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/system-prompts)
    * [Prefill Claude's response](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prefill-claudes-response)
    * [Chain complex prompts](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/chain-prompts)
    * [Long context tips](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/long-context-tips)
    * [Extended thinking tips](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/extended-thinking-tips)
  * [Extended thinking](https://docs.anthropic.com/en/docs/build-with-claude/extended-thinking)
  * [Multilingual support](https://docs.anthropic.com/en/docs/build-with-claude/multilingual-support)
  * Tool use (function calling)
  * [Prompt caching](https://docs.anthropic.com/en/docs/build-with-claude/prompt-caching)
  * [PDF support](https://docs.anthropic.com/en/docs/build-with-claude/pdf-support)
  * [Citations](https://docs.anthropic.com/en/docs/build-with-claude/citations)
  * [Token counting](https://docs.anthropic.com/en/docs/build-with-claude/token-counting)
  * [Batch processing](https://docs.anthropic.com/en/docs/build-with-claude/batch-processing)
  * [Embeddings](https://docs.anthropic.com/en/docs/build-with-claude/embeddings)


##### Agents and tools
  * [Computer use (beta)](https://docs.anthropic.com/en/docs/agents-and-tools/computer-use)
  * [Model Context Protocol (MCP)](https://docs.anthropic.com/en/docs/agents-and-tools/mcp)
  * [Google Sheets add-on](https://docs.anthropic.com/en/docs/agents-and-tools/claude-for-sheets)


##### Test and evaluate
  * Strengthen guardrails
  * [Using the Evaluation Tool](https://docs.anthropic.com/en/docs/test-and-evaluate/eval-tool)


##### Administration
  * [Admin API](https://docs.anthropic.com/en/docs/administration/administration-api)


##### Resources
  * [Glossary](https://docs.anthropic.com/en/docs/resources/glossary)
  * [Model deprecations](https://docs.anthropic.com/en/docs/resources/model-deprecations)
  * [System status](https://status.anthropic.com/)
  * [Claude 3 model card](https://assets.anthropic.com/m/61e7d27f8c8f5919/original/Claude-3-Model-Card.pdf)
  * [Claude 3.7 system card](https://anthropic.com/claude-3-7-sonnet-system-card)
  * [Anthropic Cookbook](https://github.com/anthropics/anthropic-cookbook)
  * [Anthropic Courses](https://github.com/anthropics/courses)
  * [API features](https://docs.anthropic.com/en/docs/resources/api-features)


##### Legal center
  * [Anthropic Privacy Policy](https://www.anthropic.com/legal/privacy)


Prompt engineering
# Be clear, direct, and detailed
While these tips apply broadly to all Claude models, you can find prompting tips specific to extended thinking models [here](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/extended-thinking-tips).
When interacting with Claude, think of it as a brilliant but very new employee (with amnesia) who needs explicit instructions. Like any new employee, Claude does not have context on your norms, styles, guidelines, or preferred ways of working. The more precisely you explain what you want, the better Claude’s response will be.
**The golden rule of clear prompting** Show your prompt to a colleague, ideally someone who has minimal context on the task, and ask them to follow the instructions. If they’re confused, Claude will likely be too.
## 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/be-clear-and-direct#how-to-be-clear-contextual-and-specific)
How to be clear, contextual, and specific
  * **Give Claude contextual information:** Just like you might be able to better perform on a task if you knew more context, Claude will perform better if it has more contextual information. Some examples of contextual information: 
    * What the task results will be used for
    * What audience the output is meant for
    * What workflow the task is a part of, and where this task belongs in that workflow
    * The end goal of the task, or what a successful task completion looks like
  * **Be specific about what you want Claude to do:** For example, if you want Claude to output only code and nothing else, say so.
  * **Provide instructions as sequential steps:** Use numbered lists or bullet points to better ensure that Claude carries out the task the exact way you want it to.


### 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/be-clear-and-direct#examples)
Examples
Example: Anonymizing customer feedback
Notice that Claude still makes mistakes in the unclear prompting example, such as leaving in a customer’s name.
Role| Unclear Prompt| Clear Prompt  
---|---|---  
User| Please remove all personally identifiable information from these customer feedback messages: {{FEEDBACK_DATA}}| Your task is to anonymize customer feedback for our quarterly review.Instructions:1. Replace all customer names with “CUSTOMER_[ID]” (e.g., “Jane Doe” → “CUSTOMER_001”).2. Replace email addresses with “EMAIL_[ID]@example.com”.3. Redact phone numbers as “PHONE_[ID]“.4. If a message mentions a specific product (e.g., “AcmeCloud”), leave it intact.5. If no PII is found, copy the message verbatim.6. Output only the processed messages, separated by ”---”.Data to process: {{FEEDBACK_DATA}}  
Assistant (Claude’s response)| Here are the anonymized customer feedback messages:1. I’ve been using your software for years, and it’s been great. But lately, AcmeCloud has been crashing a lot. Fix it!2. XXX, your customer support rep, was incredibly helpful. He guided me through the whole process. My email is XXX if you want to send a survey.3. I’m John Smith, and I’m not happy. I’ve been on hold for 2 hours trying to reach someone at XXX. This is unacceptable!| CUSTOMER_001: I’ve been using your software for years, and it’s been great. But lately, AcmeCloud has been crashing a lot. Fix it!---CUSTOMER_002: CUSTOMER_SERVICE_001, your customer support rep, was incredibly helpful. He guided me through the whole process. My email is EMAIL_002@example.com if you want to send a survey.---CUSTOMER_003: I’m CUSTOMER_003, and I’m not happy. I’ve been on hold for 2 hours trying to reach someone at PHONE_001. This is unacceptable!  
Example: Crafting a marketing email campaign
Notice that Claude makes up details to fill in the gaps where it lacks context with the vague prompt.
Role| Vague Prompt| Specific Prompt  
---|---|---  
User| Write a marketing email for our new AcmeCloud features.| Your task is to craft a targeted marketing email for our Q3 AcmeCloud feature release.Instructions:1. Write for this target audience: Mid-size tech companies (100-500 employees) upgrading from on-prem to cloud.2. Highlight 3 key new features: advanced data encryption, cross-platform sync, and real-time collaboration.3. Tone: Professional yet approachable. Emphasize security, efficiency, and teamwork.4. Include a clear CTA: Free 30-day trial with priority onboarding.5. Subject line: Under 50 chars, mention “security” and “collaboration”.6. Personalization: Use {{COMPANY_NAME}} and {{CONTACT_NAME}} variables.Structure:1. Subject line2. Email body (150-200 words)3. CTA button text  
Assistant (Claude’s response)| Here’s a draft marketing email for our new features:Subject: Boost Your Business with AcmeCloud’s Latest FeaturesDear Valued Customer,We’re excited to introduce three powerful features to AcmeCloud that will revolutionize your workflow:1. Real-Time Collaboration: Work on documents simultaneously with your team. No more version control issues!2. AI-Powered Insights: Make data-driven decisions with AI that analyzes trends and automates tasks.3. Advanced Security Suite: End-to-end encryption, multi-factor auth, and threat detection keep your data safe.Limited Offer: Upgrade now for a 20% first-year discount. Plus, refer a friend for an extra 10% off!Best,The AcmeCloud Team| Subject line: AcmeCloud: Enterprise security meets real-time teamworkEmail body:Dear {{CONTACT_NAME}},At {{COMPANY_NAME}}, you’re scaling fast and eyeing the cloud. But with growth comes the challenge of keeping data secure while fostering collaboration. That’s where AcmeCloud’s Q3 release comes in, tailor-made for tech innovators like you.1. Fort Knox for Your Files: Military-grade encryption now safeguards your data, both in motion and at rest. Your intellectual property stays yours, period.2. Sync Without Borders: Windows, Mac, or Linux—AcmeCloud speaks all languages. Unified version control means no more “final_v2_REALLY_FINAL.doc”.3. Collaborate at Light Speed: Ditch the attachment ping-pong. Now your devs, designers, and data scientists co-create in real-time, slashing time-to-market.Don’t just take our word for it. Experience the AcmeCloud difference with our 30-day trial. And because we know time is your most precious asset, we’re throwing in priority onboarding.Elevate Your Team Now - Free 30-Day Trial  
Example: Incident response
Notice that Claude outputs superfluous text and different formating with the vague prompt.
Role| Vague Prompt| Detailed Prompt  
---|---|---  
User| Analyze this AcmeCloud outage report and summarize the key points.{{REPORT}}| Analyze this AcmeCloud outage report. Skip the preamble. Keep your response terse and write only the bare bones necessary information. List only:1) Cause2) Duration3) Impacted services4) Number of affected users5) Estimated revenue loss. Here’s the report: {{REPORT}}  
Assistant (Claude’s response)| Here’s a summary of the key points from the AcmeCloud outage report:On May 15th, a misconfigured load balancer update caused significant traffic routing issues, resulting in a service outage from 09:15 to 13:52 UTC. The 4-hour 37-minute disruption impacted our core file syncing service and admin dashboard, rendering them inaccessible. Additionally, the mobile app experienced partial functionality loss. Approximately 68% of our user base, totaling 1.3 million users, were affected. Based on our Service Level Agreements (SLAs) and average revenue per user, we estimate a financial impact of $420,000 in service credits and potential customer churn.| 1) Cause: Misconfigured load balancer update2) Duration: 4h 37m (09:15-13:52 UTC, May 15)3) Impacted: Core sync, admin dashboard (down); mobile app (partial)4) Affected users: 1.3M (68% of base)5) Est. revenue loss: $420,000  
## [Prompt libraryGet inspired by a curated selection of prompts for various tasks and use cases.](https://docs.anthropic.com/en/prompt-library/library)## [GitHub prompting tutorialAn example-filled tutorial that covers the prompt engineering concepts found in our docs.](https://github.com/anthropics/prompt-eng-interactive-tutorial)## [Google Sheets prompting tutorialA lighter weight version of our prompt engineering tutorial via an interactive spreadsheet.](https://docs.google.com/spreadsheets/d/19jzLgRruG9kjUQNKtCg1ZjdD6l6weA6qRXG5zLIAhC8)
Was this page helpful?
YesNo
[Prompt improver](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver)[Use examples (multishot prompting)](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/multishot-prompting)
[x](https://x.com/AnthropicAI)[linkedin](https://www.linkedin.com/company/anthropicresearch)
On this page
  * [How to be clear, contextual, and specific](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/be-clear-and-direct#how-to-be-clear-contextual-and-specific)
  * [Examples](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/be-clear-and-direct#examples)


