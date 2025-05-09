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
Use prompt templates and variables
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
# Use prompt templates and variables
When deploying an LLM-based application with Claude, your API calls will typically consist of two types of content:
  * **Fixed content:** Static instructions or context that remain constant across multiple interactions
  * **Variable content:** Dynamic elements that change with each request or conversation, such as: 
    * User inputs
    * Retrieved content for Retrieval-Augmented Generation (RAG)
    * Conversation context such as user account history
    * System-generated data such as tool use results fed in from other independent calls to Claude


A **prompt template** combines these fixed and variable parts, using placeholders for the dynamic content. In the [Anthropic Console](https://console.anthropic.com/), these placeholders are denoted with **{{double brackets}}** , making them easily identifiable and allowing for quick testing of different values.
# 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-templates-and-variables#when-to-use-prompt-templates-and-variables)
When to use prompt templates and variables
You should always use prompt templates and variables when you expect any part of your prompt to be repeated in another call to Claude (only via the API or the [Anthropic Console](https://console.anthropic.com/). [claude.ai](https://claude.ai/) currently does not support prompt templates or variables).
Prompt templates offer several benefits:
  * **Consistency:** Ensure a consistent structure for your prompts across multiple interactions
  * **Efficiency:** Easily swap out variable content without rewriting the entire prompt
  * **Testability:** Quickly test different inputs and edge cases by changing only the variable portion
  * **Scalability:** Simplify prompt management as your application grows in complexity
  * **Version control:** Easily track changes to your prompt structure over time by keeping tabs only on the core part of your prompt, separate from dynamic inputs


The [Anthropic Console](https://console.anthropic.com/) heavily uses prompt templates and variables in order to support features and tooling for all the above, such as with the:
  * **[Prompt generator](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-generator):** Decides what variables your prompt needs and includes them in the template it outputs
  * **[Prompt improver](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver):** Takes your existing template, including all variables, and maintains them in the improved template it outputs
  * **[Evaluation tool](https://docs.anthropic.com/en/docs/test-and-evaluate/eval-tool):** Allows you to easily test, scale, and track versions of your prompts by separating the variable and fixed portions of your prompt template


# 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-templates-and-variables#example-prompt-template)
Example prompt template
Let’s consider a simple application that translates English text to Spanish. The translated text would be variable since you would expect this text to change between users or calls to Claude. This translated text could be dynamically retrieved from databases or the user’s input.
Thus, for your translation app, you might use this simple prompt template:
Copy
```
Translate this text from English to Spanish: {{text}}

```

## 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-templates-and-variables#next-steps)
Next steps
## [Generate a promptLearn about the prompt generator in the Anthropic Console and try your hand at getting Claude to generate a prompt for you.](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-generator)## [Apply XML tagsIf you want to level up your prompt variable game, wrap them in XML tags.](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/use-xml-tags)## [Anthropic ConsoleCheck out the myriad prompt development tools available in the Anthropic Console.](https://console.anthropic.com/)
Was this page helpful?
YesNo
[Prompt generator](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-generator)[Prompt improver](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver)
[x](https://x.com/AnthropicAI)[linkedin](https://www.linkedin.com/company/anthropicresearch)
On this page
  * [When to use prompt templates and variables](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-templates-and-variables#when-to-use-prompt-templates-and-variables)
  * [Example prompt template](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-templates-and-variables#example-prompt-template)
  * [Next steps](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-templates-and-variables#next-steps)


