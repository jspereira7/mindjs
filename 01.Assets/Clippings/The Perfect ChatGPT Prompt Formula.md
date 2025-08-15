---
title: The Perfect ChatGPT Prompt Formula
source: https://medium.com/artificial-corner/the-perfect-chatgpt-prompt-formula-0dd8d29e57a6
author:
  - "[[The PyCoach]]"
published: 2025-06-24
created: 2025-06-26
description: No matter how advanced the model is, inconsistency is still a challenge. Writing a good prompt isn’t some kind of mystery. It’s about understanding and balancing a few key elements. Every prompt…
tags:
  - clippings
  - Ai
---
Good prompts are still the key to getting great results from AI.

No matter how advanced the model is, inconsistency is still a challenge. Writing a good prompt isn’t some kind of mystery. It’s about understanding and balancing a few key elements.

Here are the elements of a good prompt:

![](https://miro.medium.com/v2/resize:fit:700/0*qheN0Pj08u2DRKNg.png)

How you combine these six components will depend on your specific needs and context.

Let’s break down each component and explore how to get the most out of them.

> If you’re not a paid subscriber, you can read this article [for free on my site](https://artificialcorner.com/p/the-perfect-chatgpt-prompt-formula). You can also get my AI and Python [cheat sheets](https://artificialcorner.com/p/redeem-my-udemy-courses-for-free) for free there.

## 1\. Task: The Core Directive

Every prompt needs a task. This is the specific instruction or question you’re trying to answer. A clear task is by far the most important part of any prompt. If everything else fails, clearly stating what you want often still leads to a meaningful result.

One recommendation when crafting the task is to be as explicit as possible.

For example, if you write a prompt like:

> Write a product launch email announcing our new smart home speaker, highlight its unique features (voice control, energy efficiency), and include a compelling call to action for pre-orders.

Here, ChatGPT knows exactly what to do (write an email) and what to include.

OpenAI’s own [guidelines](https://help.openai.com/en/articles/10032626-prompt-engineering-best-practices-for-chatgpt) emphasize clarity, specificity, and avoiding ambiguity in prompts. This is simply good practice, as the AI tends to follow instructions exactly as written, rather than trying to guess hidden meanings.

If the model’s response isn’t what you expected, chances are the task description was too broad or was misunderstood.

One tip that has worked well for me: if your task involves multiple steps, it’s really helpful to let the AI know upfront. You can include something like this in your prompt:

> Let’s approach \[insert your task\] step by step.Step 1: \[what to do\]Step 2: \[what to do next\]

To solve complex problems, it’s better to break the task down into smaller parts or explicitly ask for a structured approach.

## 2\. Context: Set the Stage

Context gives the AI the essential background it needs to work with, instead of forcing it to assume or hallucinate information. While the latest updates across various AI platforms have expanded general knowledge significantly — which is a major advantage — it can also be a drawback if we don’t learn to handle this properly. For any specific task, we still need to provide the right framework in which the response should be generated.

For example, just recently, a colleague at the office had to summarize a Q1 sales report. In that case, including specific figures and data points was absolutely necessary to get a high-quality result.

As OpenAI’s guidelines point out, giving the model enough context helps it understand exactly what you’re asking. It’s worth highlighting that this area has improved significantly with recent ChatGPT updates.

With features like extended memory, you can now provide larger amounts of text and maintain longer conversations. I find this especially helpful when I need to revisit or summarize what we’ve discussed so far.

You could try a prompt like:

> Summarize what we’ve talked about so far in bullet points.

But here, relevance is key — we don’t want the AI to get sidetracked or waste attention on trivial details.

A question I often ask myself to clarify what context is needed is: What would you say to someone who’s just joining in, so they can catch up on the task? That’s your context.

Another important update worth mentioning is multimodality. Like other advanced models, ChatGPT can now [understand images](https://artificialcorner.com/p/chatgpt-just-got-2-amazing-features), diagrams, and charts. Including them in your prompt can be very effective.

Here’s an example combining the components we’ve discussed so far:

> Attached is a chart with user feedback \[attach image\]

Context

> The bars represent how frequently certain features were requested.

Task

> Analyze the image and suggest the top two features we should prioritize

Because the model can now “see” images, I’ve found it useful to include [screenshots](https://artificialcorner.com/p/ive-been-using-chatgpt-vision-as) from websites, dashboards, or infographics as part of my prompts. Just make sure you clearly reference the image within the prompt so the AI knows how to use it to your advantage.

## 3\. Examples: Show, Don’t Just Tell

Adding one or more examples to your prompt can dramatically improve the quality of the AI’s output, especially for more complex or nuanced tasks. This method, known as few-shot prompting, takes advantage of the AI’s ability to pick up patterns and context from what you provide.

Instead of simply describing what you want, you’re showing the AI how to do it.

A practical tip I recently shared with a colleague is this: if you need the AI to respond in a specific style, or follow a particular format or framework, your best bet is to include a clear example in your prompt. Then, ask it to generate a similar result based on your current context.

Here are a few helpful reminders when adding examples to your prompts:

![](https://miro.medium.com/v2/resize:fit:700/0*V1Qaerwe5-r0Bqg5.png)

When I’m stuck or unsure of how to come up with a good example, one approach that works well is to ask the AI to create one for me. I’ll then include that sample in the actual prompt I’m building. It becomes a sort of feedback loop that helps refine the output.

Here’s how I’d apply this when preparing for a job interview:

> Based on my own resume, please help me structure an answer to the interview question: “What’s your biggest weakness?”
> 
> Use the STAR answer framework: Situation, Task, Action, and ResultsHere’s my resume for reference: \[**Put your resume here**\]

In the prompt above, the STAR framework was the example structure I used.

This kind of prompt not only sets a clear expectation but also provides the necessary structure for the AI to generate a high-quality, tailored response.

## 4\. Persona: Defining the Voice

One thing I’ve noticed is that AI models usually respond in a neutral assistant tone by default. However, you can shape the voice, level of expertise, and overall perspective by assigning the AI a specific role or persona. This helps guide how the response is written and how it should “think.”

Recent updates in ChatGPT now allow for more personalized GPT profiles. You can also use the Custom Instructions feature to set preferences for each new chat. Once you define this, you don’t need to repeat it every time. [Set it up](https://artificialcorner.com/p/the-chatgpt-setup-i-use-to-be-ahead) once, and the model will respond accordingly from that point on.

Here’s a persona prompt I’ve used regularly that helps generate responses aligned with my day-to-day communication style and work context:

> I’m a \[**Data Scientist**\] with over \[five years\] of experience in **\[predictive modeling and statistical analysis**\]. I focus on using data to solve real-world problems. Even though I have a technical background, I work closely with cross-functional teams, so I prefer responses that are accurate but also accessible to any audience.
> 
> I value clarity, simplicity, and efficiency. I like responses that are well-structured, concise, and easy to apply. Whether it’s solving a technical problem or explaining a concept, I prefer answers that are practical and strike a good balance between depth and clarity.

Here are a few tips to keep in mind when defining a persona effectively:

- **Align the persona with the task.** If the task is technical, setting the AI as a subject matter expert will help ensure the right terminology and depth. If the task is more creative, using a more imaginative or unique persona can lead to more original results.

## 5\. Format: Shaping the Output

In simple terms, format refers to how the AI should present its response.

One example I often use to make this clear is:

> Provide the output as a JSON object with the keys ‘Problem’ and ‘Recommendation’.

Another might be:

> Provide a table comparing these options (columns: Feature, Option A, Option B).

If you don’t specify a format, the AI will choose one on its own based on what it thinks fits best. That might work sometimes, but other times it can lead to responses that aren’t quite what you were looking for.

Here are a few formatting prompts I’ve used in different contexts. Feel free to adapt them to your needs:

- Respond in bullet points, one sentence per point
- Output only the Python code, with no extra explanation
- Present the answer in a Markdown table

I also have a template I like to use whenever I’m preparing content for a team presentation. It helps keep things consistent and clear:

![](https://miro.medium.com/v2/resize:fit:700/0*1cmU2t411I_bBvuU.png)

This small step makes a big difference. It ensures I never forget to define the format when it matters, especially for work that needs to be shared or presented.

## 6\. Tone: Fine-Tuning the Style

Tone is what you might consider the finishing touch to a prompt. It guides how the response should sound. If you have a specific tone in mind, it’s a good idea to include it. Otherwise, the AI will choose the tone itself.

Tone often works hand in hand with persona. In many cases, setting a clear persona already implies a certain tone. For example, telling the AI to act as a marketing director naturally sets an authoritative and strategic tone.

Still, adding a separate tone instruction can help sharpen the response. Take this example:

> “You’re a doctor explaining a diagnosis to a patient using a calm and reassuring tone.”

Here, the role is “doctor,” but the tone adds another layer of guidance. Together, they ensure the response is both accurate and emotionally appropriate for someone without a medical background.

That’s why I recommend including tone preferences in the Custom Instructions section, as mentioned earlier when we talked about Persona.

Don’t overlook tone. It can often be the difference between a response that simply checks the boxes and one that actually resonates with your audience. Tone gives your prompt personality, and it helps ensure the output feels relevant and human.