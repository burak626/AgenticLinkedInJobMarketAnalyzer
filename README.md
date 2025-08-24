---

# Agentic AI Job Market Analyzer

## Overview

Agentic AI Job Market Analyzer is an automated workflow built with **n8n** that scrapes LinkedIn job postings, extracts structured technical qualifications using **OpenAI LLMs**, and stores results in **Google Sheets**.
It provides real-time insights into the most in-demand programming languages, frameworks, platforms, and tools in the AI job market.

---

## Features

* **Automated Job Collection**

  * Uses LinkedIn Data API via RapidAPI
  * Weekly scheduled scraping of relevant jobs (Agentic AI and AI/ML roles)

* **Skill Extraction**

  * OpenAI LLM categorizes technical qualifications into:

    * Programming Languages
    * Frameworks & Libraries
    * Tools & Software
    * Platforms & Environments
    * Databases & MLOps

* **Data Cleaning**

  * Removes markdown formatting, whitespace, and noise for clean storage

* **Trend Analysis**

  * Aggregates job descriptions
  * Calculates frequency of each skill with percentages and fractions
  * Highlights top skills and emerging trends

* **Google Sheets Integration**

  * Logs per-job extracted qualifications with date and URL
  * Stores aggregated statistics and insights

---

## Workflow Summary

1. **Schedule Trigger** – Runs weekly
2. **Fetch Jobs** – LinkedIn Data API job search
3. **Split & Lookup** – Retrieve job details per listing
4. **Data Structuring** – Normalize title, description, URL, etc.
5. **LLM Extraction** – Extract structured technical skills
6. **Cleaning** – Format and sanitize outputs
7. **Save to Google Sheets** – Store results with metadata
8. **Aggregate Analysis** – Calculate trends across postings
9. **Save Insights** – Append summary statistics to Google Sheets

---

## Outputs

* **Per-job data**: Structured technical requirements from each posting
* **Aggregated trends**: Frequency and percentage of in-demand skills
* **Key insights**: Identification of emerging frameworks and technologies

---

## Use Cases

* **Students**: Align learning with real-world demand
* **Job Seekers**: Target high-demand skills for AI roles
* **Businesses**: Monitor market trends for hiring strategies

---
