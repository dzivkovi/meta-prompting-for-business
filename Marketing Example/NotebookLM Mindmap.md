Here is a mind map of the provided sources on Prompt Engineering, formatted in Markdown:

*   **Prompt Engineering**
    *   **Introduction**
        *   Definition: Designing high-quality prompts to guide LLMs to produce accurate outputs
        *   Input: Text prompt, sometimes with other modalities (e.g., image)
        *   Role: Input model uses to predict output
        *   Process: Iterative tinkering
        *   Factors Affecting Efficacy: Model, training data, configurations, word-choice, style, tone, structure, context
        *   Accessibility: Everyone can write a prompt
        *   Use Cases: Text summarization, information extraction, Q&A, classification, language/code translation, code generation/documentation/reasoning
        *   Model Choice: Optimization may be needed for specific models (Gemini, GPT, Claude, Gemma, LLaMA)
    *   **LLM Output Configuration**
        *   Purpose: Control the LLM's output
        *   Importance: Essential for effective prompt engineering
        *   Output Length
            *   Setting: Number of tokens to generate
            *   Impact: Computation cost (energy, time, money); affects prompting techniques like ReAct
            *   Note: Doesn't make output more succinct, just stops generation
        *   Sampling Controls
            *   Mechanism: Sample from predicted token probabilities
            *   Control: Randomness and diversity
            *   Settings: Temperature, Top-K, Top-P
            *   Interaction: Settings affect each other; order of application varies by model/platform
            *   Extreme Settings: Can make other settings irrelevant (e.g., Temp 0, Top-K 1, Top-P 0)
            *   Recommendations: Starting points for different creativity levels
        *   Temperature
            *   Controls: Degree of randomness
            *   Low Temperature: Deterministic, good for expected responses (Temp 0 = greedy decoding)
            *   High Temperature: Diverse, unexpected results
            *   Can exacerbate the repetition loop bug
        *   Top-K and Top-P (Nucleus Sampling)
            *   Control: Restrict next token to top probabilities
            *   Top-K: Selects top K most likely tokens (Higher K = more varied, Lower K = more factual)
            *   Top-P: Selects tokens with cumulative probability <= P (P=0 often means only most probable)
            *   Choice: Experimentation recommended
    *   **Prompting Techniques**
        *   General Prompting / Zero Shot
            *   Description: Simplest; task description + starting text; "no examples"
            *   Example: Classify movie reviews
        *   One-shot & Few-shot
            *   Use: Provide examples when zero-shot fails; helps model understand/imitate pattern
            *   One-shot: Single example
            *   Few-shot: Multiple examples (shows a pattern)
                *   Number: Depends on task complexity, example quality, model; generally 3-5+
                *   Example: Parse pizza orders to JSON
                *   Example Selection: Relevant, diverse, high quality, well written; include edge cases
                *   For Classification: Mix up classes in examples
        *   System, Contextual, and Role Prompting
            *   Purpose: Guide generation focusing on different aspects
            *   Overlap: Can occur
        *   System Prompting
            *   Primary Purpose: Defines fundamental capabilities and overarching purpose
            *   Function: Sets overall context; specifies how to return output
            *   Use Cases: Meet specific requirements (e.g., language compatibility, structure), safety/toxicity control
            *   Examples: Classifying reviews (uppercase label, JSON format)
            *   Benefits of JSON Output: Consistent style, focus on data, reduces hallucinations, relationship aware, data types, sortable
        *   Role Prompting
            *   Primary Purpose: Frames model's output style and voice
            *   Function: Assigns a specific character/identity
            *   Example: Act as a travel guide
            *   Styles: Humorous, Inspirational, Descriptive, etc.
        *   Contextual Prompting
            *   Primary Purpose: Provides immediate, task-specific information
            *   Function: Helps model understand nuances, tailor response; highly specific/dynamic
            *   Example: Suggesting blog article topics with context
        *   Step-back Prompting
            *   Technique: Ask a general question first, use its answer in the specific task prompt
            *   Benefit: Activates background knowledge/reasoning, encourages critical thinking, mitigates bias, increases accuracy
            *   Example: Writing a video game storyline (comparing traditional vs. step-back)
        *   Chain of Thought (CoT)
            *   Technique: Improves reasoning by generating intermediate steps
            *   Benefit: More accurate answers, interpretability, robustness
            *   Disadvantage: More tokens (cost, time)
            *   Use: Help LLMs with tasks they struggle with, like math
            *   Method: Instruct "Let's think step by step"
            *   Can combine with few-shot for better results
            *   Use Cases: Code generation, synthetic data, tasks solvable by breaking into steps
            *   Best Practices: Put answer after reasoning, separate answer for extraction, set temperature to 0
        *   Self-consistency
            *   Improves CoT: Combines sampling (high temperature) and majority voting
            *   Benefit: Generates diverse reasoning paths, selects most consistent answer, improves accuracy/coherence
            *   Cost: High costs
            *   Steps: Generate diverse paths, extract answers, choose most common
            *   Example: Email classification
        *   Tree of Thoughts (ToT)
            *   Generalizes CoT: Explores multiple reasoning paths simultaneously
            *   Suitable for: Complex tasks requiring exploration
            *   Mechanism: Maintains a tree of thoughts, branches from nodes
        *   ReAct (reason & act)
            *   Paradigm: Combines reasoning + external tools (search, code interpreter)
            *   Function: Allows interaction with external APIs (agent modeling)
            *   Mechanism: Thought-action loop (reason, plan, act, observe, update)
            *   Implementation: Requires code (e.g., LangChain)
            *   Example: Finding number of children of Metallica members
        *   Automatic Prompt Engineering (APE)
            *   Purpose: Automate the process of writing prompts
            *   Method: Use a model to generate prompts, evaluate, refine, repeat
            *   Example: Generating variations of a customer order phrase
            *   Evaluation: Score candidates using metrics (BLEU, ROUGE)
        *   Code Prompting
            *   Use Cases: Writing, explaining, translating, debugging/reviewing code
            *   Writing Code: Speeds up development (Caution: Read and test)
            *   Explaining Code: Helps understand existing code
            *   Translating Code: Between programming languages
            *   Debugging/Reviewing Code: Identifies errors and suggests improvements
    *   **Best Practices**
        *   Iterative Process: Craft, test, analyze, document, refine, experiment
        *   Provide Examples: Most important; one-shot/few-shot are powerful teaching tools
        *   Design with Simplicity: Concise, clear, easy to understand; use action verbs
        *   Be Specific about the Output: Provide details to guide model focus
        *   Use Instructions over Constraints: Focus on positive instructions (what *to* do); more effective (Constraints for safety, clarity, strict format)
        *   Control Max Token Length: Configuration or explicit request in prompt
        *   Use Variables: For reusability and dynamics, especially in applications
        *   Experiment: With input formats, writing styles, models, configurations
        *   Few-shot Classification: Mix up classes in examples
        *   Adapt to Model Updates: Stay informed, adjust prompts for new features
        *   Experiment with Output Formats: Use structured formats (JSON, XML) for non-creative tasks
            *   Benefits of JSON Output: Consistency, data focus, less hallucinations, relationships, data types, sorting
            *   JSON Repair: Use libraries (e.g., json-repair) to fix truncated/malformed JSON
            *   Working with Schemas: Use JSON Schema for structuring *input* data
        *   Experiment Together: Collaborate with others on prompt attempts
        *   CoT Best Practices: (Covered under CoT)
        *   Document Prompt Attempts: Crucially important; track details in a structured way (e.g., Table 21 template)
            *   Benefits: Record, revisit work, test on new models, debug
            *   Track version, result status (OK/NOT OK), feedback, hyperlink (if using Vertex AI Studio)
            *   For RAG: Capture query, chunk settings/output
            *   Codebase: Save prompts separately, use automated tests
    *   **Challenges**
        *   Inadequate prompts lead to ambiguous/inaccurate responses
        *   LLMs struggle with math
        *   Repetition loop bug
        *   JSON verbosity and truncation leading to invalid output
        *   Self-consistency can have high costs
    *   **Summary**
        *   Recaps discussed prompting techniques, challenges, and best practices
