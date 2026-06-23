# Lenovo-LEAP-GenAI-Internship
🚀 My journey through Lenovo LEAP: Generative AI &amp; Agentic Systems Engineering Internship | AICTE | Day-by-day projects, tools, and learnings in Gen AI &amp; Agentic Systems
# Day 1 – Agentic AI Email Automation 🚀

**Lenovo LEAP: GenAI & Agentic Systems Engineering Internship | AICTE**

## 📅 Overview
On Day 1 of the internship, I built an end-to-end **Agentic AI workflow** using [Relay.app](https://relay.app) + GPT-4.5 mini — my first hands-on example of AI acting autonomously to complete a real task without human intervention.

## 🤖 What I Built
An AI-powered customer support email automation that:

- 📥 **Detects** incoming customer complaint emails in Gmail
- 🧠 **Generates** a professional, context-aware reply using GPT-4.5 mini
- 📤 **Sends** the response back automatically — no manual drafting or approval step

## 🔧 Tools Used
| Tool | Role |
|---|---|
| **Relay.app** | Workflow orchestration / trigger → action automation |
| **GPT-4.5 mini** | Drafts the reply based on the incoming complaint |
| **Gmail** | Source of incoming emails + delivery of the automated reply |

## 🧠 Why This Counts as "Agentic AI"
Most chatbot use cases still need a human to read the output and decide what happens next. This workflow is different — it **perceives** (detects a complaint email), **reasons** (drafts an appropriate reply), and **acts** (sends it) end-to-end on its own. That perceive → reason → act loop is the core idea behind agentic systems, as opposed to a single-turn prompt-and-response interaction.

## 💡 Key Takeaway
Agentic AI isn't just "a chatbot that's faster" — it's AI given enough trust and structure to complete a task autonomously. Day 1 made that idea concrete instead of theoretical.

# Day 2 – Prompt Engineering Techniques 🧠✨

**Lenovo LEAP: GenAI & Agentic Systems Engineering Internship | AICTE**

## 📅 Overview
On Day 2 of the internship, I explored and practiced core prompt engineering techniques using Google Gemini, learning how the *way* a prompt is structured changes the depth, accuracy, and format of an LLM's response.

## 🔧 Techniques Practiced

### 1. Few-Shot Prompting
Gave the model two example review → sentiment pairs, then asked it to classify a new, unseen review on its own.
> **Result:** The model correctly inferred the labeling pattern and applied it without further instruction.

### 2. One-Shot Prompting
Provided a single example (`Naruto -> Never Give Up`) and asked the model to continue the same pattern for a related character (`Boruto`).
> **Result:** One demonstration was enough for the model to match the intended format and tone.

### 3. Chain-of-Thought (CoT) Prompting
Asked the model to explain, step by step, how to grow Instagram reach from under 1,000 to 50,000.
> **Result:** Produced a structured 5-step "Reach Blueprint" (profile optimization → Reels strategy → save/share triggers → engagement tricks → consistency & analytics) instead of a vague one-line answer.

### 4. Tabular Formatting
Requested a direct comparison between Python and C++ "in tabular format."
> **Result:** A clean, side-by-side table covering execution speed, memory management, typing, and use cases — much faster to scan than a paragraph.

### 5. Comparative Prompting
Asked the model to compare two entities (Captain America vs. Iron Man) using a structured framework (SWOT).
> **Result:** A balanced strengths/weaknesses/opportunities/threats breakdown for both, showing how pairing comparison with a framework sharpens the output.

### 6. Perspective Prompting
Asked the model to explain social media "from the perspective of parents."
> **Result:** The tone and focus shifted entirely — highlighting parental anxieties (the comparison trap, invisible threats, the battle for attention) instead of a generic definition.

### 7. Reverse Prompt Engineering
Took an output I liked (the parent-perspective SWOT analysis) and asked the model to reverse-engineer the exact prompt that would generate it.
> **Result:** Got a detailed, reusable prompt template — a great way to "save" a style for future use.

### 8. RGC Framework (Role – Goal – Constraints)
Structured a prompt explicitly as:
- **Role:** AI Trainer
- **Goal:** Explain deep learning
- **Constraints:** Use only World Cup soccer examples

> **Result:** The model explained neural networks, weights, loss functions, and backpropagation entirely through soccer analogies (players as neurons, the post-match review as backpropagation).

### 9. "I Want You to Act As..." (Role-Play Prompting)
Asked the model to act as a Data Scientist Interviewer for mock interview practice.
> **Result:** The model ran a simulated, one-question-at-a-time technical interview — useful for low-pressure practice before the real thing.

## 🎯 Bonus Mini-Activity: Applied Branding Exercise
Used the techniques above on a real-world task — generated 10 short, social-media-friendly brand name ideas for a gaming café (e.g., *Vault, Nexus, Ping, Forge*), then created a logo concept for the chosen name, **NEXUS**.

## 💡 Key Takeaway
The same question can produce drastically different value depending on *how* it's framed. Examples, role, perspective, constraints, and structure are all levers that shape an LLM's output quality — prompting is a skill, not a guess.

## Day 3 – Automated Project Planning Agentic Workflow with n8n 🤖📋

**Lenovo LEAP: GenAI & Agentic Systems Engineering Internship | AICTE**

### 🗂️ Overview

On Day 3 of the internship, I transitioned from simple automations to engineering a highly dynamic, multi-stage AI Agent Workflow using **n8n**, **OpenAI**, and **Google Sheets** — an autonomous agent that takes a raw user request and instantly transforms it into a fully mapped-out, dynamic project plan assigned to real team members.

---

### 🔨 What I Built

An AI-powered autonomous project planning agent that:

- 📥 **Receives** a raw user request via chat (e.g., *"I want to build a website for my business"*)
- 📊 **Retrieves** active team data dynamically from a Google Sheet (roles, names, departments)
- 🧠 **Aggregates** the list of items and feeds them into the AI layer
- 🗂️ **Plans** the project using an OpenAI-powered Planner Agent with a Structured Output Parser — breaking the request into clear, ordered milestones with owners, start/end dates, priorities, and descriptions
- 📝 **Writes** the structured task array back into a centralized master tracking sheet (task tracker) as individual task rows

---

### 🛠️ Tools Used

| Tool | Role |
|------|------|
| n8n | Workflow orchestration & multi-stage agent automation |
| OpenAI (Chat Model) | Core Agentic Layer — Planner Agent for project breakdown |
| Google Sheets | Source of team data + destination master task tracker |
| Structured Output Parser | Enforces strict JSON schema for reliable data transformation |

---

### 🤖 Why This Counts as "Agentic AI"

This workflow goes beyond a single prompt-response — it **perceives** (reads team data), **reasons** (plans the full project with assignments), and **acts** (writes structured output back to a live sheet) end-to-end without human intervention. The multi-stage orchestration with a dedicated Planner Agent mirrors real-world agentic system design patterns.

---

### 💡 Key Takeaway

The real magic isn't just getting a smart response from the LLM — it's the **data transformation**. Forcing the AI to adhere strictly to a JSON schema via the Structured Output Parser is what makes it reliable enough to programmatically update a database or sheet without breaking. Agentic systems are fundamentally shifting how we think about automation and project management.

📁 *Screenshots for each technique are available in the `/screenshots` folder of this repo.*
