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
Use our prompt improver to optimize your prompts
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
# Use our prompt improver to optimize your prompts
Our prompt improver is compatible with all Claude models, including those with extended thinking capabilities. For prompting tips specific to extended thinking models, see [here](https://docs.anthropic.com/en/docs/build-with-claude/extended-thinking).
The prompt improver helps you quickly iterate and improve your prompts through automated analysis and enhancement. It excels at making prompts more robust for complex tasks that require high accuracy.
## 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver#before-you-begin)
Before you begin
You’ll need:
  * A [prompt template](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-templates-and-variables) to improve
  * Feedback on current issues with Claude’s outputs (optional but recommended)
  * Example inputs and ideal outputs (optional but recommended)


## 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver#how-the-prompt-improver-works)
How the prompt improver works
The prompt improver enhances your prompts in 4 steps:
  1. **Example identification** : Locates and extracts examples from your prompt template
  2. **Initial draft** : Creates a structured template with clear sections and XML tags
  3. **Chain of thought refinement** : Adds and refines detailed reasoning instructions
  4. **Example enhancement** : Updates examples to demonstrate the new reasoning process


You can watch these steps happen in real-time in the improvement modal.
## 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver#what-you-get)
What you get
The prompt improver generates templates with:
  * Detailed chain-of-thought instructions that guide Claude’s reasoning process and typically improve its performance
  * Clear organization using XML tags to separate different components
  * Standardized example formatting that demonstrates step-by-step reasoning from input to output
  * Strategic prefills that guide Claude’s initial responses


While examples appear separately in the Workbench UI, they’re included at the start of the first user message in the actual API call. View the raw format by clicking ”**< /> Get Code**” or insert examples as raw text via the Examples box.
## 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver#how-to-use-the-prompt-improver)
How to use the prompt improver
  1. Submit your prompt template
  2. Add any feedback about issues with Claude’s current outputs (e.g., “summaries are too basic for expert audiences”)
  3. Include example inputs and ideal outputs
  4. Review the improved prompt


## 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver#generate-test-examples)
Generate test examples
Don’t have examples yet? Use our [Test Case Generator](https://docs.anthropic.com/en/docs/test-and-evaluate/eval-tool#creating-test-cases) to:
  1. Generate sample inputs
  2. Get Claude’s responses
  3. Edit the responses to match your ideal outputs
  4. Add the polished examples to your prompt


## 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver#when-to-use-the-prompt-improver)
When to use the prompt improver
The prompt improver works best for:
  * Complex tasks requiring detailed reasoning
  * Situations where accuracy is more important than speed
  * Problems where Claude’s current outputs need significant improvement


For latency or cost-sensitive applications, consider using simpler prompts. The prompt improver creates templates that produce longer, more thorough, but slower responses.
## 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver#example-improvement)
Example improvement
Here’s how the prompt improver enhances a basic classification prompt:
Original prompt
Copy
```
From the following list of Wikipedia article titles, identify which article this sentence came from.
Respond with just the article title and nothing else.
Article titles:
{{titles}}
Sentence to classify:
{{sentence}}

```

Improved prompt
Copy
```
You are an intelligent text classification system specialized in matching sentences to Wikipedia article titles. Your task is to identify which Wikipedia article a given sentence most likely belongs to, based on a provided list of article titles.
First, review the following list of Wikipedia article titles:
<article_titles>
{{titles}}
</article_titles>
Now, consider this sentence that needs to be classified:
<sentence_to_classify>
{{sentence}}
</sentence_to_classify>
Your goal is to determine which article title from the provided list best matches the given sentence. Follow these steps:
1. List the key concepts from the sentence
2. Compare each key concept with the article titles
3. Rank the top 3 most relevant titles and explain why they are relevant
4. Select the most appropriate article title that best encompasses or relates to the sentence's content
Wrap your analysis in <analysis> tags. Include the following:
- List of key concepts from the sentence
- Comparison of each key concept with the article titles
- Ranking of top 3 most relevant titles with explanations
- Your final choice and reasoning
After your analysis, provide your final answer: the single most appropriate Wikipedia article title from the list.
Output only the chosen article title, without any additional text or explanation.

```

Notice how the improved prompt:
  * Adds clear step-by-step reasoning instructions
  * Uses XML tags to organize content
  * Provides explicit output formatting requirements
  * Guides Claude through the analysis process


## 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver#troubleshooting)
Troubleshooting
Common issues and solutions:
  * **Examples not appearing in output** : Check that examples are properly formatted with XML tags and appear at the start of the first user message
  * **Chain of thought too verbose** : Add specific instructions about desired output length and level of detail
  * **Reasoning steps don’t match your needs** : Modify the steps section to match your specific use case


## 
[​](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver#next-steps)
Next steps
## [Prompt libraryGet inspired by example prompts for various tasks.](https://docs.anthropic.com/en/prompt-library/library)## [GitHub prompting tutorialLearn prompting best practices with our interactive tutorial.](https://github.com/anthropics/prompt-eng-interactive-tutorial)## [Test your promptsUse our evaluation tool to test your improved prompts.](https://docs.anthropic.com/en/docs/test-and-evaluate/eval-tool)
Was this page helpful?
YesNo
[Use prompt templates](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-templates-and-variables)[Be clear and direct](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/be-clear-and-direct)
[x](https://x.com/AnthropicAI)[linkedin](https://www.linkedin.com/company/anthropicresearch)
On this page
  * [Before you begin](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver#before-you-begin)
  * [How the prompt improver works](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver#how-the-prompt-improver-works)
  * [What you get](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver#what-you-get)
  * [How to use the prompt improver](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver#how-to-use-the-prompt-improver)
  * [Generate test examples](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver#generate-test-examples)
  * [When to use the prompt improver](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver#when-to-use-the-prompt-improver)
  * [Example improvement](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver#example-improvement)
  * [Troubleshooting](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver#troubleshooting)
  * [Next steps](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver#next-steps)


