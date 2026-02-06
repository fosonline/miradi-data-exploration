---
marp: true
paginate: true
---

# Talk to Your Data
## AI-Powered Conservation Analysis

ICTC 2026

<!--
Welcome slide. Introduce yourself.
~1 minute
-->

---

## What is Vibe Coding?

> "Just see stuff, say stuff, run stuff, and copy paste stuff, and it mostly works"
> -- Andrej Karpathy Feb-2025

- Describe what you want **in plain English**
- AI generates the code
- You run it, refine it, iterate
- **No programming experience required (but it still helps)**

<!--
Explain the concept. This isn't about becoming a programmer -
it's about using AI as a tool to answer YOUR questions about YOUR data.
~2 minutes

Andrej Karpathy - Previously Director of AI @ Tesla, founding team @ OpenAI, CS231n/PhD @ Stanford. 
-->

---

## What You'll Do Today

Working in teams, you'll:

1. Load conservation project data into a notebook
2. Ask AI to explore and visualize the data
3. Map relationships, analyze gaps, visualize trends
4. Build custom analyses through conversation

**Tools we'll use:**
- Google Colab (free, runs in your browser)
- Gemini AI (built into Colab)
- Miradi Share sample project data

The same approach works with ChatGPT, Claude, and other AI tools.

<!--
Set expectations. Everything runs in the browser, nothing to install.
Mention that teams help - you can compare approaches and share discoveries.
~1 minute
-->

---

## The Data: Miradi & the Conservation Standards

<!-- TODO: Replace with your own conceptual diagram -->

1. **Assess** -- Identify biodiversity targets, threats, contributing factors in a situation analysis
2. **Plan** -- Define goals, strategies, objectives, activities
3. **Implement** -- Track work plans, resources, expenses
4. **Analyze & Adapt** -- Monitor indicators, measure progress, learn & adjust

The sample data captures **all of these** as structured tables.

<!--
Brief grounding in the Open Standards for non-Miradi users.
If you have a custom diagram, insert it here.
~2 minutes
-->

---

## Sample Project at a Glance

| What | Count |
|------|-------|
| Biodiversity Targets | 7 (Coral reefs, Sharks, Seagrass, Mangroves, Seabirds) |
| Direct Threats | 9 |
| Strategies | 19 |
| Indicators | 77 |
| Measurements | 301 (spanning 2012-2025) |

Plus: goals, activities, results chains, funding sources, and more.

**38 tables total** from a real Miradi Share project export.

<!--
Give them a sense of what they'll be working with.
~1 minute
-->

---

# Getting Started

<!--
Transition to hands-on.
-->

---

## Step 1: Open the Notebook

1. Scan the QR code or type the short link:
   **https://tinyurl.com/miradi-workshop**
2. Click **"Copy to Drive"** (you need a Google account)
3. The Gemini sidebar should be visible on the right

![bg right:30% contain](assets/colab-qr-code.png)

<!--
Walk them through opening Colab. Have the link ready on screen.
Make sure everyone can see the Gemini sidebar.
~3 minutes (account for stragglers)
-->

---

## Step 2: Load the Data

Run the first two code cells:

```python
# Cell 1: Download the sample data
!wget -q https://...sample_project.sqlite
```

```python
# Cell 2: Connect and list tables
conn = sqlite3.connect('project.sqlite')
```

You should see **38 tables** listed.

<!--
Everyone runs together. Check that everyone sees the table list.
~2 minutes
-->

---

## Step 3: Explore the Data

Run the next cells to load key tables:

- `biodiversity_targets` -- What we're protecting
- `direct_threats` -- Human activities causing harm
- `strategies` -- Interventions
- `indicators` -- What we measure
- `measurements` -- Monitoring data over time

Look at the targets table output. **What do you notice?**

<!--
Pause and let them look at the data. Point out viability statuses.
~2 minutes
-->

---

# Your Turn: Talk to Your Data

<!--
Transition to the main hands-on block.
~30 minutes total for exercises
-->

---

## Exercise 1: Visualize Target Status

In the Gemini sidebar, try typing:

> "Create a bar chart showing the viability status of all biodiversity targets"

**Tips:**
- If the code doesn't work, tell Gemini the error
- Ask it to change colors, labels, or chart type
- Try: *"Make it a pie chart instead"*

<!--
First exercise - easy win to build confidence.
~5 minutes
-->

---

## Exercise 2: Network Diagrams

Ask Gemini to visualize relationships:

> "Create a network diagram showing how threats relate to targets"

> "Show me which strategies address which threats"

**Tip:** Tell Gemini to look at the reference section at the bottom of the notebook for help with data relationships.

<!--
This one is harder - some participants may need help.
~5 minutes
-->

---

## Exercise 3: Time Series

The measurements table has monitoring data from 2012-2025.

> "Plot the measurement values over time for coral reef indicators"

> "Are any indicators showing decline?"

> "Compare trends across all targets"

<!--
Time series is very natural for conservation data.
~5 minutes
-->

---

## Exercise 4: Maps

The project has location data (latitude, longitude).

> "Show the project location on a map"

> "Create a map with the project boundary"

Uses the `folium` library for interactive maps.

<!--
Maps are always a crowd-pleaser.
~5 minutes
-->

---

## Exercise 5: Your Questions

Now try your own analysis questions:

- *"Which targets don't have any indicators?"* (gap analysis)
- *"What's the budget distribution across strategies?"*
- *"Create a summary dashboard of project health"*
- *"Write a SQL query to count indicators per target"*

**Discuss with your team: what questions would you ask of YOUR project data?**

<!--
Open-ended exploration. Walk around the room, help people.
Flag interesting results to share with the group.
~10 minutes
-->

---

# Wrap-up

<!--
Transition to closing.
-->

---

## What Just Happened?

You explored a conservation dataset without writing code yourself.

**The AI handled:** SQL queries, chart generation, map rendering, statistics

**You provided:** The questions, domain expertise, and judgment

**Raise your hand if you got a chart working!**

<!--
Reinforce the key message: their expertise + AI tools = powerful combo.
Quick show of hands to gauge how far people got.
~2 minutes
-->

---

## Key Takeaways

1. **Describe what you want** -- AI generates the code
2. **Iterate** -- refine by describing what to change
3. **Domain expertise matters** -- AI doesn't know your project, you do
4. **This works with any structured data** -- not just Miradi

<!--
~1 minute
-->

---

## Next Steps

- **Try with your own project data**
  Export from Miradi Share, load into Colab the same way

- **Explore other AI tools**
  Claude, ChatGPT, GitHub Copilot -- same approach

- **Apply beyond Miradi**
  SMART, EarthRanger, survey data, any CSV/database

- **Share the notebook**
  It's yours -- modify, extend, share with colleagues

<!--
~2 minutes
-->

---

# Questions?

Workshop notebook: **https://tinyurl.com/miradi-workshop**

<!--
Q&A time. Have the link and QR code visible on screen.
-->
