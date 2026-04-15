# GenAI Risk Analysis & Customer Insight Pipeline (Vertex AI + BigQuery)

## Overview

This project demonstrates a practical workflow built on Google Cloud using Vertex AI (Gemini) and BigQuery. It combines structured data querying, prompt engineering, and multimodal inputs to generate business insights such as sentiment analysis, customer summaries, and insurance risk recommendations.

## What I Built

* Queried customer review data in BigQuery and processed it inside a notebook environment
* Generated sentiment classification (positive vs negative) and displayed results using HTML tables
* Built prompt-driven workflows in Vertex AI Studio using Gemini (gemini-2.5-flash)
* Designed structured prompts to extract key fields from unstructured insurance claim text
* Created an insurance risk analysis prototype generating risk factors and recommendations
* Tested multiple prompt versions and compared outputs to improve structure and clarity
* Used multimodal prompts (image + text) to generate contextual summaries and insights

## Key Implementations

### 1. Customer Sentiment Analysis (BigQuery + Notebook)

* Processed customer review dataset with fields like review_text and source
* Generated sentiment counts and displayed results dynamically using HTML output
* Created structured summaries and recommended responses for customer feedback

### 2. Prompt Engineering with Gemini

* Built structured prompts to extract:

  * Policy number
  * Claim details
  * Estimated loss
  * Incident type
* Enforced output format (key-value pairs) to reduce ambiguity
* Compared prompt versions to improve output quality and consistency

### 3. Insurance Risk Analysis Prototype

* Generated risk factors such as:

  * Geographic exposure
  * Cargo type and value
  * Driver behavior insights
* Produced recommendation sections for mitigation strategies
* Designed outputs in structured bullet format for decision-making

### 4. Multimodal + Generative AI

* Used image + text inputs to generate contextual insights
* Combined visual understanding with text-based reasoning

## Tools & Technologies

* Google Cloud Platform (GCP)
* Vertex AI Studio
* Gemini (gemini-2.5-flash)
* BigQuery
* Python (Notebook environment)
* Prompt Engineering

## Key Learnings

* Few-shot prompting significantly improved structured outputs compared to zero-shot
* Controlling temperature reduced variability in analytical responses
* Structuring prompts (explicit format instructions) reduced hallucinations
* Combining BigQuery data with LLM prompts produced more grounded outputs

## Screenshots

Refer to the `screenshots/` folder for:

* BigQuery dataset and queries
* Sentiment analysis output
* Prompt engineering comparisons
* Insurance risk summary outputs
* Multimodal examples

## Note

This project was implemented as part of Google Cloud hands-on labs and demonstrates practical application of Generative AI workflows using real tools and interfaces.
