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
Let Claude think (chain of thought prompting) to increase performance
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
# Let Claude think (chain of thought prompting) to increase performance
While these tips apply broadly to all Claude models, you can find prompting tips specific to extended thinking models [here](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/extended-thinking-tips).
When faced with complex tasks like research, analysis, or problem-solving, giving Claude space to think can dramatically improve its performance. This technique, known as chain of thought (CoT) prompting, encourages Claude to break down problems step-by-step, leading to more accurate and nuanced outputs.
## 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/chain-of-thought#before-implementing-cot)
Before implementing CoT
### 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/chain-of-thought#why-let-claude-think)
Why let Claude think?
  * **Accuracy:** Stepping through problems reduces errors, especially in math, logic, analysis, or generally complex tasks.
  * **Coherence:** Structured thinking leads to more cohesive, well-organized responses.
  * **Debugging:** Seeing Claude’s thought process helps you pinpoint where prompts may be unclear.


### 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/chain-of-thought#why-not-let-claude-think)
Why not let Claude think?
  * Increased output length may impact latency.
  * Not all tasks require in-depth thinking. Use CoT judiciously to ensure the right balance of performance and latency.


Use CoT for tasks that a human would need to think through, like complex math, multi-step analysis, writing complex documents, or decisions with many factors.
## 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/chain-of-thought#how-to-prompt-for-thinking)
How to prompt for thinking
The chain of thought techniques below are **ordered from least to most complex**. Less complex methods take up less space in the context window, but are also generally less powerful.
**CoT tip** : Always have Claude output its thinking. Without outputting its thought process, no thinking occurs!
  * **Basic prompt** : Include “Think step-by-step” in your prompt. 
    * Lacks guidance on _how_ to think (which is especially not ideal if a task is very specific to your app, use case, or organization)
Example: Writing donor emails (basic CoT)
Role| Content  
---|---  
User| Draft personalized emails to donors asking for contributions to this year’s Care for Kids program.Program information:<program>{{PROGRAM_DETAILS}}</program>Donor information:<donor>{{DONOR_DETAILS}}</donor>Think step-by-step before you write the email.  
  * **Guided prompt** : Outline specific steps for Claude to follow in its thinking process. 
    * Lacks structuring to make it easy to strip out and separate the answer from the thinking.
Example: Writing donor emails (guided CoT)
Role| Content  
---|---  
User| Draft personalized emails to donors asking for contributions to this year’s Care for Kids program.Program information:<program>{{PROGRAM_DETAILS}}</program>Donor information:<donor>{{DONOR_DETAILS}}</donor>Think before you write the email. First, think through what messaging might appeal to this donor given their donation history and which campaigns they’ve supported in the past. Then, think through what aspects of the Care for Kids program would appeal to them, given their history. Finally, write the personalized donor email using your analysis.  
  * **Structured prompt** : Use XML tags like `<thinking>` and `<answer>` to separate reasoning from the final answer. 
Example: Writing donor emails (structured guided CoT)
Role| Content  
---|---  
User| Draft personalized emails to donors asking for contributions to this year’s Care for Kids program.Program information:<program>{{PROGRAM_DETAILS}}</program>Donor information:<donor>{{DONOR_DETAILS}}</donor>Think before you write the email in <thinking> tags. First, think through what messaging might appeal to this donor given their donation history and which campaigns they’ve supported in the past. Then, think through what aspects of the Care for Kids program would appeal to them, given their history. Finally, write the personalized donor email in <email> tags, using your analysis.  


### 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/chain-of-thought#examples)
Examples
Example: Financial analysis without thinking
Without step-by-step thinking, Claude gives a recommendation that seems reasonable but lacks depth. It doesn’t quantify the potential outcomes or consider historical market performance, which are crucial for making an informed decision.
Role| Content  
---|---  
User| You’re a financial advisor. A client wants to invest $10,000. They can choose between two options: A) A stock that historically returns 12% annually but is volatile, or B) A bond that guarantees 6% annually. The client needs the money in 5 years for a down payment on a house. Which option do you recommend?  
Assistant| Based on the information provided, I would recommend option B, the bond that guarantees a 6% annual return. Here’s why:1. Certainty: The bond offers a guaranteed 6% annual return, which provides certainty in financial planning. This is crucial when the client has a specific financial goal (down payment) with a fixed timeline (5 years).2. Risk aversion: Since the client needs this money for an important life event (buying a house), they likely have a low risk tolerance. The volatility of the stock market could jeopardize their plans if there’s a downturn close to when they need the funds.3. Time horizon: With only 5 years, there’s less time to recover from potential stock market downturns. Longer investment horizons (10+ years) are generally better suited for weathering stock market volatility.While the stock’s historical 12% return is attractive, past performance doesn’t guarantee future results. The guaranteed 6% from the bond ensures the client will have the funds they need when it’s time to make the down payment.  
Example: Financial analysis with thinking
With step-by-step thinking, the advisor provides a much richer analysis. It calculates exact figures for both scenarios, considers historical market volatility, and deeply analyzes the client’s risk tolerance. This thorough reasoning leads to a more confident and justifiable recommendation.
Role| Content  
---|---  
User| You’re a financial advisor. A client wants to invest $10,000. They can choose between two options: A) A stock that historically returns 12% annually but is volatile, or B) A bond that guarantees 6% annually. The client needs the money in 5 years for a down payment on a house. Which option do you recommend? Think step-by-step.  
Assistant| To determine the best investment option for our client, I’ll consider several factors step-by-step:<thinking>1. Understand the client’s goal and timeline: - Goal: Down payment for a house - Timeline: 5 years - Implication: This is a short-term, high-priority financial goal. The client likely cannot afford significant risk or volatility.2. Analyze Option A (Stock): - Pro: Higher historical return (12% annually) - Con: Volatile (implying potential for significant gains or losses) - Calculate potential 5-year return: - Best case (12% annually): $10,000 * (1.12)^5 ≈ $17,623.42 - Worst case (market crash): Could lose a substantial portion, e.g., 50% crash = $5,0003. Analyze Option B (Bond): - Pro: Guaranteed return (6% annually) - Con: Lower return compared to historical stock performance - Calculate 5-year return: - Guaranteed: $10,000 * (1.06)^5 ≈ $13,382.254. Consider risk tolerance: - Goal is a house down payment (essential, not discretionary) - Short timeline (5 years) limits ability to recover from market downturns - Conclusion: Client likely has low risk tolerance5. Historical perspective: - Stock’s 12% is historical, not guaranteed - In 5-year periods, stock market can vary wildly: - 2003-2007 (pre-financial crisis): S&P 500 up ~82% - 2007-2011 (during crisis): S&P 500 down ~2% - Conclusion: Past performance doesn’t guarantee future results, especially short-term6. Final analysis: - Option A (Stock): Higher potential return but unacceptable risk of not meeting the down payment goal - Option B (Bond): Guaranteed to meet ~80% of best-case stock scenario, 100% certainty of having funds</thinking><answer>I recommend Option B, the bond with a guaranteed 6% annual return. While the stock’s historical 12% return is tempting, the bond ensures you’ll have $13,382.25 in 5 years for your house down payment. Given the importance and short timeline of your goal, the stock’s volatility poses an unacceptable risk. The bond provides certainty, which is invaluable for such a crucial financial milestone.</answer>  
## [Prompt libraryGet inspired by a curated selection of prompts for various tasks and use cases.](https://docs.anthropic.com/en/prompt-library/library)## [GitHub prompting tutorialAn example-filled tutorial that covers the prompt engineering concepts found in our docs.](https://github.com/anthropics/prompt-eng-interactive-tutorial)## [Google Sheets prompting tutorialA lighter weight version of our prompt engineering tutorial via an interactive spreadsheet.](https://docs.google.com/spreadsheets/d/19jzLgRruG9kjUQNKtCg1ZjdD6l6weA6qRXG5zLIAhC8)
Was this page helpful?
YesNo
[Use examples (multishot prompting)](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/multishot-prompting)[Use XML tags](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/use-xml-tags)
[x](https://x.com/AnthropicAI)[linkedin](https://www.linkedin.com/company/anthropicresearch)
On this page
  * [Before implementing CoT](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/chain-of-thought#before-implementing-cot)
  * [Why let Claude think?](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/chain-of-thought#why-let-claude-think)
  * [Why not let Claude think?](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/chain-of-thought#why-not-let-claude-think)
  * [How to prompt for thinking](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/chain-of-thought#how-to-prompt-for-thinking)
  * [Examples](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/chain-of-thought#examples)


