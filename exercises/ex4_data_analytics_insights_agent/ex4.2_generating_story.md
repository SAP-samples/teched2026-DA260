# TechEd Hands-On: Data and Analytics Insights Agent in SAP Analytics Cloud

> **TechEd 2026 — Hands-On Session**

Learn how to use the Data and Analytics insights agent to auto-generate SAC stories with goal suggestion, automatic widget generation, and Joule natural-language chart editing to build a complete analytics story in minutes.

| | |
|---|---|
| **Product** | SAP Analytics Cloud |
| **Topic** | Data and Analytics Insights Agent and Joule in SAC |
| **Steps** | 14 Steps |
| **Duration** | ~20 Minutes |

---

## About this Exercise

In this exercise you will use the Data and Analytics Insights Agent to generate a fully structured analytics story from an Insights Instruction. You will let the agent suggest a story goal, configure the output, watch the Story Generation Agent build the story in real time, and finally use **Joule in SAC** to modify a chart with a natural-language prompt — all without writing a single piece of code or placing and configuring a single widget by hand.

**Prerequisites**

- SAP Analytics Cloud tenant access
- Permission: Story Generation and Insights Instruction permission
- Insights Instruction: `sales-performance-analysis-da260-sample`
- Modern browser (Chrome recommended)

---

## Part 1 — Define Your Story Goal

### Step 1 — Open the Create Story Wizard

In SAP Analytics Cloud, navigate to the **Stories** section using the left navigation sidebar (the speech-bubble icon). Click the **+ Create Story** button to open the wizard. The agent provide 2 entry mode: wizard mode and Joule mode. In this exercise we are going to use the wizard mode.

The wizard opens on **Step 1: Define Goal**, showing a three-step progress bar: *Define Goal → Review Outline → Story Settings*. The **Based on** field is pre-set to *Insights Instructions*. The **Your Goal** text area is empty, awaiting your input or an AI suggestion.

> **Tip:** The Create Story wizard is one of the entry point for Data and Analytics Insights Agent. It uses Insights Instructions or SAC models — domain-specific metadata files — to guide the AI in proposing the content for your analytics story.

![Create Story wizard — Step 1: Define Goal](teched_handson_assets/step01.jpg)
*Create Story wizard opens on the Define Goal step with an empty goal field.*

---

### Step 2 — Open the Insights Instruction Picker

In the **Based on** row, click the **search/link icon** next to the *Insights Instructions* label (or click inside the text input field that reads *Select insights instructions...*).

The **Select Insights Instruction** dialog opens and begins loading the available instructions for your tenant. A three-dot loading indicator confirms the system is fetching the list.

![Select Insights Instruction dialog loading](teched_handson_assets/step02.jpg)
*The Insights Instruction picker dialog opens and loads available instructions.*

---

### Step 3 — Select the Insights Instruction

Once the list loads, locate and select the instruction what you created in the exercise ex4.1. Alternatively, you can also choose the sample instructions `sales-performance-analysis-da260-sample`. Click **OK** to confirm.

The dialog closes and the instruction name appears in the **Based on** field. The **Your Goal** text area is still empty, showing the placeholder text *"Describe an objective for your story or allow AI to suggest a prompt for you."*

> **Tip:** Insights Instructions bundle domain expertise (which measures to use, which chart types suit which analyses, relevant filters) into a reusable file. Selecting the right instruction ensures the AI generates contextually accurate content.

![Insights Instruction selected — sales-performance-analysis-dsag](teched_handson_assets/step03.jpg)
*The instruction `sales-performance-analysis-dsag` is now selected in the Based on field.*

---

### Step 4 — Request an AI-Suggested Goal

You can type your goal manually, or click the **Suggest** button (the blue AI button with a sparkle icon in the top-right of the goal area) to let the AI propose a story goal based on the selected Insights Instruction.

The system shows *"This is taking a moment, please wait..."* with a loading indicator. The AI is analyzing the Insights Instruction metadata and composing a structured story outline.

![AI suggestion in progress — Please wait](teched_handson_assets/step04.jpg)
*The AI is analyzing the Insights Instruction and generating a story goal suggestion.*

---

### Step 5 — Review the AI-Generated Story Goal

The AI populates the **Your Goal** text area with a comprehensive story outline structured by analytical sections:

**Page 1: Sales Performance Overview**
- *Key Metrics* — Numeric point charts comparing Sales, Online Revenue, and Units (2026 vs 2025)
- *Region Analysis* — Bar charts for Sales and Expense by Region (USA, Canada, Mexico)
- *Product & Store Analysis* — Bar charts for Sales by Product Category and by Store
- *Period Analysis* — Time series line chart for monthly sales trend (Q1 2025–Q3 2026)
- *Brand Analysis* — Data table with Sales and Expense by Brand

> **Tip:** You can freely edit this AI-generated outline before proceeding. Modify chart types, add or remove sections, or refine the goal text. The AI will use your final text as the instruction for story generation.

![AI-generated story goal — structured outline](teched_handson_assets/step05.jpg)
*The AI suggests a complete multi-section story outline with specific chart types for each analysis area.*

---

## Part 2 — Configure & Generate

### Step 6 — Configure Story Settings

Click **Next Step** to advance past the *Review Outline* step to **Step 3: Story Settings**. Configure the following options:

- **Output Type** — Open the dropdown and select *Story Page* (default). Alternatively, choose *New HTML Page* if you prefer an HTML-based output format.
- **Theme** — Keep the default *SAP Morning Horizon (Light)* theme.
- **Story Options** — Optionally enable *Include Appendix Page* to add a data appendix, or *Auto-save story pages to File Repository* for automatic backup.

> **Tip:** For this exercise, keep Output Type as *Story Page* and leave the other options at their defaults.

![Story Settings — Output Type dropdown open](teched_handson_assets/step06.jpg)
*Step 3: Story Settings with the Output Type dropdown showing Story Page and New HTML Page options.*

---

### Step 7 — Click Generate Story

Click the **Generate Story** button in the bottom-right corner of the wizard. The wizard closes and the story editor opens in a new tab named *New Story*.

The editor displays a live generation progress log. You can see the system loading the **Story Generation Agent** and initializing the AI models in real time. The first task — "Add Widgets to Story Page Sales Performance Overview" — begins immediately.

![Story generation progress — Load AI Agent and Load Models](teched_handson_assets/step07.jpg)
*The Story Generation Agent is loaded and begins adding widgets to the story page.*

---

### Step 8 — Watch Widgets Being Added in Real Time

The generation log updates live as each widget is created and added to the story page. You will see individual confirmation lines for each chart:

- Compare Sales for 2026 vs 2025 as numeric point — *Added*
- Compare Online Revenue for 2026 vs 2025 as numeric point — *Added*
- Compare Unit for 2026 vs 2025 as numeric point — *Added*
- Sales where Region is USA, Canada, and Mexico as bar chart — *Added*
- Expense where Region is USA, Canada, and Mexico as bar chart — *Added*

You may see toast notifications at the bottom of the screen about calculations being renamed (e.g., *"Calculation 2026 has been renamed to 2026 (2) due to a duplicate name."*). This is expected behavior — dismiss these notifications by clicking the X. With that you can see the calculated measure like *compare sales for 2025 vs 2025* is generated on-the-fly while generating the story.

![Story generation — multiple widgets added with rename notifications](teched_handson_assets/step08.jpg)
*The agent adds widgets one by one. Rename notifications at the bottom are expected and can be dismissed.*

---

### Step 9 — All Widgets Added — Auto Layout in Progress

The log continues until all 9 widgets from the story outline have been added:

- Sales by Product Category as bar chart — *Added*
- Sales by Store as bar chart — *Added*
- Monthly Sales trend (Q1 2025–Q3 2026) as line chart — *Added*
- Sales and Expense by Brand as table — *Added*

Once all widgets are placed, the AI applies an **Auto Layout** to the story page — intelligently arranging all charts for optimal readability without manual sizing or positioning.

![All widgets added — Auto Layout in progress](teched_handson_assets/step09.jpg)
*All 9 widgets are added. The AI now auto-arranges them into the best layout for the story page.*

---

### Step 10 — Story Generation Complete

The final entries in the generation log confirm:

- **Auto Layout** — "AI has created the best layout to fit the content."
- **Process Story Filters** — "filter Version by Actual — Applied"
- **Done** — "The story has been generated."

The story is now fully generated and ready to view. The editor tab shows the completed story. Proceed to the next step to explore it.

![Story generation complete — Done message](teched_handson_assets/step10.jpg)
*The generation log confirms all steps are complete: widgets added, layout applied, filters processed.*

---

## Part 3 — Review & Refine with Joule

### Step 11 — Review the Generated Story

Click anywhere on the story canvas (or scroll up from the generation log) to view the fully generated **Sales Performance Overview** story page. You will see:

- **Page title and subtitle** — AI-generated descriptive text
- **Time Series chart** — Monthly Sales per Date trend line (Sep 2025–Sep 2026)
- **Brand Analysis table** — Sales and Expense values for Even Better, Hermanos, Jumbo, and Sunset brands

Scroll the story page upward to also see the **Key Metrics** section (KPI tiles for Sales, Online Revenue, Units) and the **Region Analysis** bar charts. All charts are fully bound to live data.

> **Tip:** The story uses the SAP Morning Horizon (Light) theme. All charts have default styling, filters, and interactions applied automatically by the AI.

![Generated story — Sales Performance Overview with charts](teched_handson_assets/step11.jpg)
*The completed story shows a time series chart and brand analysis table. Scroll up to see all sections.*

---

### Step 12 — Open Joule and Select a Chart to Modify

Scroll up to the **Region Analysis** section. Click the **Sales per Region** bar chart to select it (a blue border appears around the selected chart).

Then click the **Joule** icon (purple diamond / AI assistant) in the top-right toolbar. The Joule panel slides open on the right side of the screen.

In the **Message Joule...** input at the bottom of the panel, type the following natural-language modification request:

```
remove Region, add calendar month, and filter by 2026 from january to september for the selected chart
```

> **Tip:** Joule operates on the currently *selected* widget. Always click your target chart before opening Joule, or select it while the Joule panel is open — otherwise the modification applies to nothing. Alaternatively, you can write the chart name in your natual language description instead of selecting the widget in story canvas

![Joule panel open with modification prompt](teched_handson_assets/step12.jpg)
*The Joule AI panel is open. A natural-language prompt instructs Joule to change the dimension and filter the chart.*

---

### Step 13 — Joule Processes Your Request

Press **Enter** or click the send button to submit the prompt. Joule displays your message in the conversation panel and begins thinking.

The panel shows *"Thinking..."* with a progress bar while Joule interprets your instruction, identifies the chart properties to change (dimension, measure filter, date range), and plans the sequence of modifications.

![Joule thinking — processing the natural language request](teched_handson_assets/step13.jpg)
*Joule processes your natural-language prompt, determining the exact chart property changes required.*

---

### Step 14 — Joule Applies the Chart Modifications

Joule applies the changes to the selected chart in real time. The panel updates to show *"Updating chart properties..."* as each modification is executed:

- **Remove Region** — The Region dimension is removed from the chart axis
- **Add Calendar Month** — Calendar Month replaces Region as the chart dimension
- **Filter 2026 Jan–Sep** — A date range filter (January 2026 to September 2026) is applied to the chart

Once complete, the chart on the canvas updates live to reflect the new configuration. The bar chart now shows monthly sales data for the first 9 months of 2026 instead of regional comparisons.

> **Tip:** Joule's AI interprets intent — note that the prompt used informal language ("janurary to september") and Joule resolved these to the correct dimension and filter values. You can continue refining with additional prompts in the same conversation.

![Joule updating chart properties](teched_handson_assets/step14.jpg)
*Joule applies all three chart modifications simultaneously — dimension change, new dimension added, and date range filter applied.*

---

### Step 15 — Save the generated story in My File folder and run this story.

---

## Exercise Complete!

You have successfully used the **Create Story wizard** with AI goal suggestion to generate a full analytics story, and refined a chart using **Joule's natural-language AI** — without writing a single piece of code or manually placingand configuring a single widget.

---

*SAP TechEd Hands-On Session — SAP Analytics Cloud — Story Generation & Joule AI — All screenshots captured from a live SAP Analytics Cloud environment.*
