# Sample Prompts (Vertex AI + BigQuery GenAI Workflow)

This file demonstrates prompt design along with sample inputs and outputs from:

* Customer sentiment analysis (BigQuery pipeline)
* Insurance risk analysis (Vertex AI - Gemini)

---

## 1. Sentiment Classification (BigQuery Pipeline)

**Prompt**
Analyze the following customer review and classify sentiment. Also extract key issues.

**Input**
"The delivery was late and the package was damaged. Very disappointed with the service."

**Output**
Sentiment: Negative
Key Issues: Late delivery, damaged package

---

## 2. Customer Feedback → Business Summary

**Prompt**
Summarize the issue, identify key problems, and suggest improvements.

**Input**
"The app keeps crashing when I try to make a payment. It’s very frustrating."

**Output**
Summary: Customer unable to complete payment due to app crashes
Key Issues: App instability, failed transactions
Recommended Actions: Fix payment module bugs, improve app reliability

---

## 3. Structured Insurance Data Extraction

**Prompt**
Extract structured data from the insurance claim text.

**Input**
"Policy number 12345. The accident occurred on March 3rd at 5 PM. The vehicle was damaged in a collision. Estimated loss is $8000."

**Output**
Policy Number: 12345
Claimant Name: Not found
Date of Loss: March 3rd
Time of Loss: 5 PM
Type of Loss: Vehicle collision
Estimated Loss Amount: $8000
Injuries Reported: Not found

---

## 4. Risk Factor Identification (Baseline)

**Prompt**
Identify key risk factors.

**Input**
"Driver has multiple past claims and operates in a high-traffic urban area."

**Output**

* History of multiple claims
* High-risk driving environment

---

## 5. Risk Factor + Recommendation (Improved Prompt)

**Prompt**
Identify risk factors and suggest mitigation strategies.

**Input**
"Driver operates a high-value cargo truck in a congested city and has prior accident history."

**Output**
Risk Factor: Prior accident history
Explanation: Indicates higher likelihood of repeated incidents
Recommendation: Provide driver training and enforce stricter monitoring

Risk Factor: High-value cargo
Explanation: Increases financial exposure in case of loss
Recommendation: Use additional insurance coverage and tracking systems

---

## 6. Prompt Comparison (Experiment)

**Version 1 Output (Basic)**

* High traffic
* Previous claims

**Version 2 Output (Improved)**
Risk Factor: Previous claims
Explanation: Indicates recurring risk pattern
Recommendation: Introduce driver monitoring

👉 Observation: Structured prompt produced clearer and more usable output

---

## 7. Multimodal Prompt (Image + Text)

**Prompt**
Analyze the image and provide insights.

**Input**
Image: Delivery package with visible damage
Text: "Customer reported receiving a damaged product."

**Output**
Description: Package appears damaged on arrival
Issue Identified: Product damage during delivery
Summary: Delivery handling issue leading to customer dissatisfaction

---

## 8. Hallucination Control Prompt

**Prompt**
Use only provided information. Do not assume missing details.

**Input**
"Policy number 78910. Incident occurred last night."

**Output**
Policy Number: 78910
Date of Loss: Not found
Time of Loss: Not found
Type of Loss: Not found

---

## 9. Controlled Output (Parameter-Tuned)

**Prompt**
Generate precise and structured output.

**Input**
"Minor accident reported with low damage."

**Output**
Risk Level: Low
Reason: Minor incident with limited damage

---

## 10. HTML Output (BigQuery Notebook)

**Prompt**
Generate sentiment summary in HTML table format.

**Input**
Negative reviews: 10
Positive reviews: 25

**Output (HTML)**

<table>
<tr>
<th>Negative</th>
<th>Positive</th>
</tr>
<tr>
<td style="color:red;">10</td>
<td style="color:green;">25</td>
</tr>
</table>

---
