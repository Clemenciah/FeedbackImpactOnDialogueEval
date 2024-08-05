# FeedbackImpactOnDialogueEval

Welcome to the GitHub repository for the paper "Rethinking the Evaluation of Dialogue Systems: Effects of User Feedback on Crowdworkers and LLMs." SIGIR 2024

This repository contains the data and analysis tools used in the study exploring the impact of user feedback on the evaluation processes of crowd workers and Large Language Models (LLMs) within the context of dialogue systems. The project aims to provide insights into how user feedback can influence the assessment accuracy of both crowdworkers and LLMs.

Additionally, we do further analysis to understand which metrics benefit from the inclusion of follow-up utterance and in which metrics human assessors perform better compared to LLM assessors

## Overview

Our study investigates two primary methodologies for assessing Task-Oriented Dialogue Systems (TDSs):
1. Evaluations that incorporate the user’s follow-up utterance.
2. Evaluations conducted without the user's follow-up.

## Repository Structure

- **Data/**
  - **CrowdworkerAnnotations/**: Contains annotated dialogue data by human crowdworkers.
  - **LLMAnnotations/**: Contains dialogue data annotated by LLMs.
- **Prompts/**: Prompts used for dialogue aspect assessment by gpt-3.5-turbo.


## Data Description

The datasets in this repository are divided into two main parts:

- **Crowdworkers**: Data capturing how crowdworkers' evaluations are influenced by direct user feedback.
- **LLMs**: Data reflecting how Large Language Model  evaluations are influenced by direct user feedback.

Each dataset includes:

- `user_id`: Identifier for the user session.
- `dialogue_id`: Identifier for each dialogue instance.
- `feedback`: Actual feedback provided by users.
- `evaluations`: Responses and evaluation scores from crowdworkers and LLM.


### Evaluation Aspects of Dialogue Systems

This section outlines the criteria used to evaluate dialogue responses in our study. Each aspect plays a significant role in the comprehensive assessment of Task-Oriented Dialogue Systems (TDSs).

- **Relevance**: How relevant are the responses to the initial query?
- **Usefulness**: The utility of the responses in context.
- **Interestingness**: How engaging the responses are.
- **Explanation Quality**: The clarity and helpfulness of explanations provided by the system.

