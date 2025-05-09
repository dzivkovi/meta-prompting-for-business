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
Prefill Claude's response for greater output control
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
# Prefill Claude's response for greater output control
While these tips apply broadly to all Claude models, you can find prompting tips specific to extended thinking models [here](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/extended-thinking-tips).
Prefilling is only available for non-extended thinking modes. It’s not currently supported with extended thinking.
When using Claude, you have the unique ability to guide its responses by prefilling the `Assistant` message. This powerful technique allows you to direct Claude’s actions, skip preambles, enforce specific formats like JSON or XML, and even help Claude maintain character consistency in role-play scenarios.
In some cases where Claude is not performing as expected, a few prefilled sentences can vastly improve Claude’s performance. A little prefilling goes a long way!
## 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prefill-claudes-response#how-to-prefill-claudes-response)
How to prefill Claude’s response
To prefill, include the desired initial text in the `Assistant` message (Claude’s response will continue from where the `Assistant` message leaves off):
Copy
```
import anthropic
client = anthropic.Anthropic()
response = client.messages.create(
  model="claude-3-7-sonnet-20250219",
  max_tokens=1024,
  messages=[
    {"role": "user", "content": "What is your favorite color?"},
    {"role": "assistant", "content": "As an AI assistant, I don't have a favorite color, But if I had to pick, it would be green because"} # Prefill here
  ]
)

```

The prefill content cannot end with trailing whitespace. A prefill like `"As an AI assistant, I "` (with a space at the end) will result in an error.
### 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prefill-claudes-response#examples)
Examples
#### 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prefill-claudes-response#example-1-controlling-output-formatting-and-skipping-the-preamble)
Example 1: Controlling output formatting and skipping the preamble
**Power user tip** : Prefilling `{` forces Claude to skip the preamble and directly output the JSON object. This is cleaner, more concise, and easier for programs to parse without additional processing.
Example: Structured data extraction without prefilling
Role| Content  
---|---  
User| Extract the name, size, price, and color from this product description as a JSON object:<description>The SmartHome Mini is a compact smart home assistant available in black or white for only $49.99. At just 5 inches wide, it lets you control lights, thermostats, and other connected devices via voice or app—no matter where you place it in your home. This affordable little hub brings convenient hands-free control to your smart devices.</description>  
Assistant| Here’s the extracted information in JSON format:```json{ “name”: “SmartHome Mini”, “size”: “5 inches wide”, “price”: “$49.99”, “colors”: [“black”, “white”]}```I’ve extracted the following details from the product description:- **Name** : SmartHome Mini- **Size** : 5 inches wide- **Price** : $49.99- **Colors** : Available in black and whiteThe JSON object provides a structured format that’s easy for programs to parse and use. Let me know if you need any modifications or have any other questions!  
Example: Structured data extraction with prefilling
Role| Content  
---|---  
User| Extract the name, size, price, and color from this product description as a JSON object:<description>The SmartHome Mini is a compact smart home assistant available in black or white for only $49.99. At just 5 inches wide, it lets you control lights, thermostats, and other connected devices via voice or app—no matter where you place it in your home. This affordable little hub brings convenient hands-free control to your smart devices.</description>  
Assistant (prefill)| {  
Assistant (Claude’s response)| “name”: “SmartHome Mini”,“size”: “5 inches wide”,“price”: “$49.99”,“colors”: [ “black”, “white”]}  
#### 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prefill-claudes-response#example-2-maintaining-character-in-roleplay-scenarios)
Example 2: Maintaining character in roleplay scenarios
**Role-play tip** : Prefilling a bracketed `[ROLE_NAME]` can remind Claude stay in character, even for longer and more complex conversations. This is especially powerful when combined with role prompting in the `system` parameter.
Example: Maintaining character without role prompting
Role| Content  
---|---  
User (50 conversation turns in with “Sherlock Holmes” Claude)| What do you deduce about the owner of this shoe? <image>muddy_shoe.jpg</image>  
Assistant| As an AI assistant, I would be happy to analyze the image of a muddy shoe as if you had provided it. Here’s my deduction…  
Example: Maintaining character with role prompting
Role| Content  
---|---  
User (50 conversation turns in with “Sherlock Holmes” Claude)| What do you deduce about the owner of this shoe? <image>muddy_shoe.jpg</image>  
Assistant (prefill)| [Sherlock Holmes]  
Assistant (Claude’s response)| Ah, what have we here? A most curious specimen, Watson! Let us examine this shoe with a discerning eye. The mud, you see, is not your common London clay, but rather the distinctive reddish hue of the iron-rich soil found only in the environs of Hampstead Heath. And yet, the wear on the sole suggests a gait more suited to the cobblestones of Whitechapel than the gentle slopes of the Heath.Now, observe the laces! They are tied with a particular knot favored by those in the medical profession—doubtless a habit acquired during years of tying surgical gowns. But the scuff marks on the toe box tell a different tale: they are consistent with the kicking motion one might employ in the martial arts, specifically Baritsu.We may conclude, then, that our absent shoe owner is a doctor, possibly a surgeon, who resides in Whitechapel but frequents Hampstead Heath—perhaps for a secret Baritsu practice, away from prying eyes. A most intriguing case, Watson! We must make haste; the game is afoot!  
## [Prompt libraryGet inspired by a curated selection of prompts for various tasks and use cases.](https://docs.anthropic.com/en/prompt-library/library)## [GitHub prompting tutorialAn example-filled tutorial that covers the prompt engineering concepts found in our docs.](https://github.com/anthropics/prompt-eng-interactive-tutorial)## [Google Sheets prompting tutorialA lighter weight version of our prompt engineering tutorial via an interactive spreadsheet.](https://docs.google.com/spreadsheets/d/19jzLgRruG9kjUQNKtCg1ZjdD6l6weA6qRXG5zLIAhC8)
Was this page helpful?
YesNo
[Give Claude a role (system prompts)](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/system-prompts)[Chain complex prompts](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/chain-prompts)
[x](https://x.com/AnthropicAI)[linkedin](https://www.linkedin.com/company/anthropicresearch)
On this page
  * [How to prefill Claude’s response](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prefill-claudes-response#how-to-prefill-claudes-response)
  * [Examples](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prefill-claudes-response#examples)
  * [Example 1: Controlling output formatting and skipping the preamble](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prefill-claudes-response#example-1-controlling-output-formatting-and-skipping-the-preamble)
  * [Example 2: Maintaining character in roleplay scenarios](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prefill-claudes-response#example-2-maintaining-character-in-roleplay-scenarios)


