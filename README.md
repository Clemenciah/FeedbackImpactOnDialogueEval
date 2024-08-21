# FeedbackImpactOnDialogueEval

## Introduction

Welcome to the GitHub repository for the paper "Rethinking the Evaluation of Dialogue Systems: Effects of User Feedback on Crowdworkers and LLMs," published at SIGIR 2024.

This repository contains the data and prompts used in our study exploring the impact of user feedback on the evaluation processes of crowd workers and Large Language Models (LLMs) within the context of dialogue systems. Our project provides insights into how user feedback can influence the assessment accuracy of both crowdworkers and LLMs.

## Research Objectives

Our study investigates two primary methodologies for assessing Task-Oriented Dialogue Systems (TDSs):
1. Evaluations that incorporate the user's follow-up utterance (Setup 1: with user feedback).
2. Evaluations conducted without the user's follow-up (Setup 2: without user feedback).

We explore how these setups affect the evaluation of system responses across four aspects: relevance, usefulness, interestingness, and explanation quality.

## Repository Structure

```bash
.
├── Data/
│   ├── Crowdworkers/
│   │   ├── withuser.json
│   │   └── withoutuser.json
│   └── LLMs/
│       ├── withuser.json
│       └── withoutuser.json
├── Prompts/
│   ├── relevance_prompt.txt
│   ├── usefulness_prompt.txt
│   ├── interestingness_prompt.txt
│   └── explanation_quality_prompt.txt
└── README.md
```

## Data Description

The datasets in this repository are divided into two main categories:

1. **Crowdworkers**: Data capturing how crowdworkers' evaluations are influenced by direct user feedback.
2. **LLMs**: Data reflecting how Large Language Model evaluations are influenced by direct user feedback.

Each JSON file (`withuser.json` and `withoutuser.json`) contains an array of dialogue evaluations. Here's an example of the data structure:

```json
{
  "dialogue": 100,
  "interaction": {
    "user": "Know any good movies?",
    "system": "Off the top of my head the movie \"Shrek (2001)\" comes to mind. Only because alot of lines from it are stuck in my head If you dont like animated stuff I rewatched \"John Wick (2014)\" recently have you seen it?",
    "aspects": [
      {
        "Explanation-quality": {
          "score": 45,
          "justification": "The assistant gives two suggestions, \"Shrek (2001)\" and \"John Wick (2014)\". It mentions why \"Shrek\" is top of mind, but does not explain what makes it a good movie in general. The reference to \"John Wick\" lacks any explanation and seems to be mentioned as an alternative taste preference without elaboration. More detailed reasoning would improve the explanatory quality."
        },
        "interestingness": {
          "score": 45,
          "justification": "The response provides two movie suggestions with a personal touch, mentioning lines stuck in the head and a recent rewatch, which adds a slight personal and relatable element. However, the description lacks vivid language or details that evoke strong imagery or excitement about the movies."
        },
        "relevance": {
          "score": 62,
          "justification": "The assistant offers two movie suggestions which aligns with the user's simple request for movie recommendations. It presents options from two different genres—one animated and one action film—giving some variety. However, not much detail is given on why these movies were recommended or if they're generally considered 'good', which could be subjective and might not fully align with the user's expectations."
        },
        "usefulness": {
          "score": 58,
          "justification": "The assistant provides two movie suggestions, catering to different tastes: one animated and one action film. The mention of memorable lines from \"Shrek\" might resonate with many users, though the connection is personal and anecdotal. The suggestion of \"John Wick\" provides an option for those interested in non-animated films. However, the response lacks detail and does not inquire about the user's preferences for a more tailored recommendation."
        }
      }
    ]
  }
}
```

## Evaluation Aspects

Our study focuses on four key aspects of dialogue system evaluation:

1. **Relevance**: Assesses how well the system's response aligns with the user's initial query.
2. **Usefulness**: Measures the practical value of the response in addressing the user's needs.
3. **Interestingness**: Evaluates how engaging and captivating the system's response is.
4. **Explanation Quality**: Judges the clarity, depth, and helpfulness of the system's explanations.

## Prompts

The `Prompts/` directory contains the prompts used for dialogue aspect assessment by gpt-3.5-turbo. These prompts were carefully crafted to guide the LLM in evaluating dialogues across four aspects: relevance, usefulness, interestingness, and explanation quality. Each aspect has its own specific prompt:

- `relevance.txt`: For evaluating how well the system's response aligns with the user's query.
- `usefulness.txt`: For assessing the practical value of the response in addressing the user's needs.
- `interestingness.txt`: For evaluating how engaging and captivating the system's response is.
- `explanation_quality.txt`: For judging the clarity, depth, and helpfulness of the system's explanations.

These prompts are designed to be adaptable for both setups in our study:
- Setup 1: With user feedback (withuser)
- Setup 2: Without user feedback (withoutuser)

The same prompt for each aspect can be used in both setups, with slight modifications in application to account for the presence or absence of user feedback.

## Citation

If you use this dataset or findings in your research, please cite our paper:

Siro, C., Aliannejadi, M., & de Rijke, M. (2024). Rethinking the Evaluation of Dialogue Systems: Effects of User Feedback on Crowdworkers and LLMs. In Proceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval (pp. 1952-1962). Association for Computing Machinery. https://doi.org/10.1145/3626772.3657712

## Contact

For any questions or further information about this dataset, please contact:

c.n.siro@uva.nl

## License

This project is licensed under the MIT License.


