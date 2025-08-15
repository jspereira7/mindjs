---
title: "This One Prompt Changed How I Use AI Forever"
source: "https://levelup.gitconnected.com/this-one-prompt-changed-how-i-use-ai-forever-401ceb3c457c"
author:
  - "[[Maria Ali]]"
published: 2025-06-20
created: 2025-06-26
description: "I used to think the magic of AI was in the tools APIs, libraries, fancy models. But I was wrong. The real magic? It’s in the prompt. And not just any prompt, but a prompt that reprograms how you…"
tags:
  - "clippings Ai"
---
## How one Friday afternoon experiment led me down a rabbit hole of automating tasks I didn’t even realize I could automate — with one surprisingly powerful prompt.



I used to think the magic of AI was in the tools APIs, libraries, fancy models. But I was wrong. The real magic? It’s in the prompt. And not just *any* prompt, but a prompt that reprograms *how you think* about automation.

Let me show you how one prompt transformed my workflow and eventually how I built a Python-powered automation system that now handles tasks I used to waste hours on. If you’re still manually rewriting resumes, summarizing content, or sifting through PDFs… you’re doing it wrong. Here’s what changed everything for me.

![](https://miro.medium.com/v2/resize:fit:640/0*X3a9GGcXHeJNdrIw.jpg)

Photo from Pixabay

# The Problem: I Was Wasting Hours on Tasks That Felt “Too Small” to Automate

There were all these little tasks I was doing every week:

- Rewriting resumes for different job postings
- Extracting key points from YouTube tutorials I didn’t finish watching
- Organizing research papers into folders on my desktop (which always ended in chaos)

Each one felt too minor to justify building a full automation system around. But altogether? They added up to hours of lost time and a lot of mental fatigue.

So, I started experimenting with how I could offload some of this to AI. And one day, I wrote this prompt:

# The Prompt That Changed Everything

"""  
I have a \[TYPE\_OF\_INPUT\] and I want to automate \[THIS\_SPECIFIC\_TASK\].  
Here are the constraints:  
\- It should be efficient, scalable, and easy to reuse  
\- The output should be clean and ready for the next step in a workflow  
\- If the task includes transformation or formatting, follow industry best practices  
  
Can you give me:  
\- A clean, modular Python script that performs this  
\- A list of libraries I need and why  
\- Suggestions for how I could improve or scale it later  
"""

I fed this into ChatGPT, changed the placeholders, and watched it create actual solutions that worked cleanly, consistently, and repeatably. And that’s when the light bulb went on.

# Use Case #1: Rewriting Resumes for Job Descriptions

**(a prompt-powered automation that saves me 90 minutes every time)**

I used to copy-paste my resume into ChatGPT manually and tweak it to fit each job. It worked kind of, but it felt clunky and repetitive. Using the master prompt, I built a proper Python pipeline that now tailors my resume automatically.

## Step 1: Markdown Resume + Job Description

I keep a markdown version of my resume and paste in the job description.

md\_resume = open("resume.md", "r").read()  
job\_description = open("job.txt", "r").read()

## Step 2: Prompt Engineering + GPT API

I wrap the prompt dynamically:

from openai import OpenAI  
openai.api\_key = "your\_sk"  
  
prompt = f"""  
I have a resume in Markdown and a job description.  
Tailor the resume to emphasize the skills and experiences that align with the job.  
  
\### Resume:  
{md\_resume}  
  
\### Job Description:  
{job\_description}  
"""  
  
response = openai.ChatCompletion.create(  
    model="gpt-4o-mini",  
    messages=\[{"role": "user", "content": prompt}\],  
    temperature=0.25  
)  
  
optimized\_resume = response.choices\[0\].message.content

## Step 3: Convert Markdown to PDF Automatically

import markdown  
import pdfkit  
  
\# Convert markdown to HTML  
html = markdown.markdown(optimized\_resume)  
  
\# Save as PDF  
with open("resume.html", "w") as f:  
    f.write(html)  
  
pdfkit.from\_file("resume.html", "resume.pdf")

This one pipeline now does in 10 seconds what I used to do in 90 minutes.

![](https://miro.medium.com/v2/resize:fit:700/0*ng7m9ZJdKLvmZXn9.jpg)

Photo from Pixabay

# Use Case #2: Summarizing YouTube Lectures I Never Finished Watching

**(and actually learning from them)**

## Step 1: Extract Transcript from YouTube

import re  
from youtube\_transcript\_api import YouTubeTranscriptApi  
  
youtube\_url = "https://www.youtube.com/watch?v=example"  
video\_id = re.search(r"(?:v=|\\/)(\[0-9A-Za-z\_-\]{11})", youtube\_url).group(1)  
transcript = YouTubeTranscriptApi.get\_transcript(video\_id)  
  
text = "\\n".join(\[entry\['text'\] for entry in transcript\])

## Step 2: Summarize with GPT

summary\_prompt = f"""  
Summarize this YouTube lecture in bullet points:  
{text}  
"""  
  
response = openai.ChatCompletion.create(  
    model="gpt-4o-mini",  
    messages=\[{"role": "user", "content": summary\_prompt}\],  
    temperature=0.3  
)  
  
summary = response.choices\[0\].message.content  
print(summary)

Now I can “watch” a lecture without even opening the video.

# Use Case #3: Automatically Organizing PDFs by Topic

**(finally cleaned my desktop)**

I had 118 research PDFs. No structure. I couldn’t find anything. So I made AI do it for me.

## Step 1: Extract Abstracts

import fitz  \# PyMuPDF  
import os  
  
def get\_abstract(pdf\_path):  
    doc = fitz.open(pdf\_path)  
    text = doc\[0\].get\_text()  \# first page usually has abstract  
    return text.strip()  
  
pdf\_dir = "research\_papers"  
abstracts = \[get\_abstract(os.path.join(pdf\_dir, f)) for f in os.listdir(pdf\_dir)\]

## Step 2: Generate Embeddings and Cluster

from sentence\_transformers import SentenceTransformer  
from sklearn.cluster import KMeans  
import pandas as pd  
  
model = SentenceTransformer("all-MiniLM-L6-v2")  
embeddings = model.encode(abstracts)  
  
kmeans = KMeans(n\_clusters=5)  
labels = kmeans.fit\_predict(embeddings)  
  
df = pd.DataFrame({"filename": os.listdir(pdf\_dir), "label": labels})

## Step 3: Auto-Sort into Folders

import shutil  
  
for \_, row in df.iterrows():  
    folder = f"cluster\_{row\['label'\]}"  
    os.makedirs(folder, exist\_ok=True)  
    shutil.move(os.path.join(pdf\_dir, row\['filename'\]), os.path.join(folder, row\['filename'\]))

Done. Organized by topic. Zero manual sorting.

# The Realization: Prompts Are the New Programming Interfaces

I used to start with libraries. Now, I start with the prompt. The right prompt isn’t just a way to get AI to do something, it’s a way to architect your thinking. It forces you to:

- Be clear about what you want
- Think modularly
- Automate at the **problem level**, not just the task level

And that changes *everything*.

![](https://miro.medium.com/v2/resize:fit:640/0*6VsNWM8ZETTT9bYC.jpg)

# Pro Tip:

When building with AI, don’t ask “How do I use this tool?” Ask, “What would I *never* want to do again manually?” That’s where the best prompts are born.

# What I’d Tell Any Beginner Now

You don’t need to be an AI expert. You need to be a **problem-solver** with a bias toward automation.

If you’re 18 like me and wondering if you can build stuff that saves time, impresses employers, and makes your daily life smoother, the answer is yes. And it starts with one prompt that changes how you think about building.

# **Final Thoughts**

We’re no longer coding just to code. We’re coding to scale *ourselves*. And the best way to do that is to turn everything into a prompt-driven, Python-powered pipeline.

If this resonated with you, start with one task. One workflow. One friction point. And ask the right prompt.

**That’s where automation begins.**

Want to see the full code for each project? I’ll be sharing all of them in an upcoming post. Drop your questions in the comments, I actually read them.

[[Tradução - Artigo]]

