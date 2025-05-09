# Transform AI Knowledge into Your Business Superpower

This repository shows how regular business professionals can take cutting-edge AI knowledge, often found in dense technical guides, and make it directly useful for their specific work. The key is a technique called **meta-prompting**.

Think of it like this: you give the AI a smart 'master instruction' (the meta-prompt). This master instruction tells the AI how to read a general guide (like one on advanced AI prompting) and then create a custom set of ready-to-use, practical instructions (your domain-specific prompts) tailored precisely for your industry or tasks. It's about turning expert advice into your everyday advantage, allowing you to apply the best AI practices directly to your unique business challenges.

## Inspiration

This repository is inspired by an idea shared by [Kieran Flanagan on LinkedIn](https://www.linkedin.com/posts/kieranjflanagan_you-can-instantly-turn-googles-new-65-page-activity-7325866858614562817-3PWD/). He demonstrated how to take comprehensive prompt engineering guides (like Google's 65-page document or guides from OpenAI and Anthropic) and transform them into a practical library of marketing-specific prompts. The core concept is to use a meta-prompt to process a guide and extract key prompt types, providing both general and domain-specific examples in a structured format.

![Marketing Prompts](Marketing%20Example/Kieran.jpeg)

This repository builds upon that approach by:

1. **Providing a [modified meta-prompt](Marketing%20Example/Kieran-NotebookLM.prompt)** specifically adapted for use with [NotebookLM](https://notebooklm.google.com/), Google's AI-powered research and note-taking tool.
2. **Curating links to [Official Prompting Guides from Major AI Model Providers](Guides/README.md)** to centralize valuable resources.
3. **Including key documents directly**, such as Google's ["Prompt Engineering" guide by Lee Boonstra](Guides/google/Google_Prompt_Engineering_v7_by_Lee_Boonstra.pdf) in PDF format for easy access.
4. **Consolidating and converting other relevant guides** into Markdown format within the [Guides](Guides) directory. For example, materials from OpenAI and Anthropic, often found across various web pages, were gathered and processed (utilizing tools like these [Crawl4ai scripts](https://github.com/dzivkovi/crawl4ai-tests) for this purpose).

## The Importance of Kieran's Approach

Kieran Flanagan's method highlights a powerful way to make advanced AI techniques more accessible and practical for various business domains. The key benefits include:

- **Practical Application of General Knowledge**: It translates general, often theoretical, prompt engineering principles into actionable, domain-specific tools.
- **Accelerated Learning and Adoption**: By providing ready-made, tailored prompt examples (like those in [Marketing](Marketing%20Example/Types%20of%20LLM%20Prompts%20and%20Their%20Uses%20in%20Marketing.md)), professionals can quickly learn and apply effective prompting in their specific field without needing to become AI experts.
- **Systematic Prompt Development**: It encourages a structured approach to building and organizing a library of prompts, moving beyond ad-hoc experimentation. This allows for easier reuse, refinement, and sharing of effective prompts within a team or organization.
- **Democratization of AI Skills**: It empowers subject-matter experts in any field (not just marketing) to leverage the full potential of LLMs by providing a clear framework for adapting general best practices to their unique needs.

## Applying This to Your Domain

The true power of this approach lies in its adaptability. While the example here focuses on marketing, you can apply the same methodology to virtually any domain:

1. **Identify a Comprehensive Guide**: Find a high-quality, general prompt engineering guide or a guide relevant to a broad area of interest. This repository includes several under the [Guides](Guides) directory.
2. **Obtain the Guide**: If it's a PDF, like [Guides/google/Google_Prompt_Engineering_v7_by_Lee_Boonstra.pdf](Guides/google/Google_Prompt_Engineering_v7_by_Lee_Boonstra.pdf), you can use it with AI chat tools that allow document uploads (e.g., NotebookLM).
3. **Adapt the Meta-Prompt**: Modify a prompt similar to [Marketing Example/Kieran-NotebookLM.prompt](Marketing%20Example/Kieran-NotebookLM.prompt) or [Marketing Example/Kieran.prompt](Marketing%20Example/Kieran.prompt). Crucially, change the "Marketing-Specific Example" instruction in the meta-prompt to target *your* specific domain (e.g., "Legal-Research-Specific Example", or "Healthcare-Planning-Specific Example").
4. **Generate Your Domain-Specific Library**: Use an LLM to run your adapted meta-prompt against the chosen guide.
5. **Refine and Expand**: Review the generated table of prompts. Refine the examples, add new ones based on your experiences, and build a valuable, customized resource for your work.
6. **Bonus**: If you're using [NotebookLM](https://notebooklm.google.com/), ou might find this guide on [NotebookLM for Content Research](https://dzivkovi.github.io/notebooklm-for-seo-research/). It is `SEO`-focused, but the principles apply to any domain.

By following this process, professionals in any field can create their own powerful libraries of advanced prompts, tailored to their specific tasks and challenges, thereby enhancing productivity and innovation.
