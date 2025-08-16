# Task_06_Descriptive_Stats


## Project Overview

This project, "Research Task 5: Descriptive Statistics and Large Language Models," is an exploration of how Large Language Models (LLMs) like ChatGPT, Co-Pilot, or Gemini handle and interpret data from a small public dataset. The core task is to provide a dataset to an LLM and challenge it to answer natural language questions about the data. The primary focus is not just on getting a correct answer, but on understanding the LLM's process, its limitations, and the prompt engineering required to achieve accurate results.

---

## Objectives

* To provide a large language model with a public dataset and ask it to answer natural language questions.
* To use prompt engineering to guide the LLM to correctly answer questions, particularly more probing ones that require defining a measure of quality.
* To validate the LLM's answers against the original dataset to ensure accuracy.
* To document the experience, including instances where the LLM failed, what prompts were used, and the nature of the failure.
* To explore the LLM's capability to produce visualizations directly from the data.

---

## Repository Contents

* `readme.md`: This file, providing an overview of the project.
* `prompts.txt`: A file containing the natural language questions asked of the LLM.
* `scripts/`: A directory that may contain scripts for generating basic statistics for validation purposes.
* `findings.md`: A summary of the interactions with the LLM, including its responses, an analysis of its successes and failures, and any visualizations it produced.

---

## How to Use

1.  **Obtain the Dataset:** Access the Syracuse University Women’s Lacrosse data (or a similar public dataset) from the source link.
2.  **Select an LLM:** Choose a large language model like ChatGPT, Co-Pilot, Gemini, or Claude.
3.  **Prompt the LLM:** Copy the contents of the prompts file and interact with the LLM, providing the dataset and asking the questions.
4.  **Document Findings:** Record the LLM's responses and your analysis in a `findings.md` file. Compare the LLM's answers to your own manual validation to assess accuracy.
5.  **Contribute:** Update this repository with your findings and any code used for validation.

---

## Summary of Findings

This section includes a detailed account of the LLM's performance, highlighting its ability to handle straightforward statistical queries versus its struggles with complex, interpretive questions.

* **Successes:** The LLM was consistently successful in answering direct, factual questions that required simple data retrieval or calculations (e.g., total goals, overall record, total attendance, etc.). It demonstrated a strong ability to find and present numerical information as long as the data was explicitly present in the provided document.

* **Challenges:** The LLM struggled with more complex, probing questions. These required a defined measure of quality, an interpretive leap, or the ability to correlate data points that were not directly linked in the dataset.
    * **Subjective Metrics:** Questions requiring a subjective metric, such as "most improved player" or "game-changer," could not be answered without a specific, user-defined formula for these terms. The LLM correctly identified this limitation.
    * **Data Correlation:** The model was unable to answer questions that required correlating data from different parts of the document that were not linked (e.g., player goals per period or home vs. away individual stats). It correctly identified that the necessary granularity was missing from the aggregated data.
    * **Causal Inference:** The LLM was unable to provide a definitive "reason" or "causal" analysis (e.g., "what might be a possible reason for this change?"). It correctly identified that this kind of speculative reasoning falls outside the scope of descriptive statistics.

* **Visualizations:** The LLM's ability to produce visualizations was not tested in this phase of the project, as the focus was on generating and interpreting descriptive statistical text.

---

## Source Dataset

* **Dataset:** Syracuse University Women’s Lacrosse, Combined Team Statistics (as of May 26, 2023)
* **Link:** https://s3.us-east-2.amazonaws.com/sidearm.nextgen.sites/suathletics.com/documents/2023/2/14/2023Stats.pdf?timestamp=20230527030432
