---
title: Ctrl Alt Discuss
date: 2023-11-28 12:00:00 +0100
categories: [App, Software]
tags: [cybersecurity, python, artificial intelligence]
pin: true
image:
  path: /micro.webp
  lqip: data:image/webp;base64,UklGRoQBAABXRUJQVlA4IHgBAADQCQCdASocADIAPjESiEKiISEYDf4AIAMEtIBlAxQIlw3E9BV1AH+A82KYA/3XqACgr+kswQF9S5xzGlnQ9pQDhazKqrqUxl+BNy8A6c7FaiFM1qUZTYAA/v+S6nqzP72yK/xtUoMgKzsF84LooW/9tF+Fawx3gpGxI1pB7KfKfxPc7fsA7ADytIOhWraYOqz+bfKGvft1XBOtQXhYVaKCeBsAbhMeL5gcj7Rorv7MOkxLKOAFNTq3EngNNY3NsWs5UH8T81JfosvymYUWbUdkVp3/vq7nwPMUOxI2d/b/ufCGBdr1qc6+fpjf4SAOgny6cE1n8NN4Ul+7H+PNf1mFUioYb0/T6UI5Kxf8f9S+Rq146eOZOPhk2b1zHf9TrAgSWDX+ogzGtFHv6aJsAc6rrnW4J8c5Klcsghm9ISTw2eDSzDOMDMoYMQpLtgXr2WO96FB970YtsfjEQZzkwAQ/P+I66TDHYlzNzuR6ttiBR3Z7yeyAAAAA
  alt: Responsive rendering of Chirpy theme on multiple devices.
---

Welcome to the Ctrl+Alt+Discuss project! This project combines the powerful capabilities of OpenAI, Eleven Labs AI, and RSS feed aggregation to automatically create podcasts. The core of this solution relies on the GPT-3.5-turbo language model from OpenAI to generate podcast scripts, complemented by Eleven Labs' Text-to-Speech (TTS) to bring these scripts to life.

# Table of Contents

1. [Objective](#objective)
2. [Features](#features)
   - [RSS Feed Aggregation](#rss-feed-aggregation)
   - [Script Generation with GPT](#script-generation-with-gpt)
   - [Text-to-Speech with Eleven Labs](#text-to-speech-with-eleven-labs)
3. [Configuration](#configuration)
   - [Installing Dependencies](#installing-dependencies)
   - [Setting Environment Variables](#setting-environment-variables)
   - [Running the Project](#running-the-project)
4. [References](#references)

# Objective

The goal of this project is to simplify podcast creation by automating the content generation process. By leveraging state-of-the-art natural language processing and speech technologies, aim to provide relevant and accurate content on demand.

# Features

## RSS Feed Aggregation

The project starts by aggregating RSS feeds from predefined sources. These RSS feeds provide the foundational content for podcast episodes.

## Script Generation with GPT

The OpenAI GPT-3.5-turbo model is used to generate podcast scripts from content extracted from the RSS feeds. This model can understand context and produce high-quality natural language.

## Text-to-Speech with Eleven Labs

Generated scripts are then converted into audio files using Eleven Labs' Text-to-Speech (TTS) technology. This step gives a realistic and pleasant voice to the scripts, creating the final podcast audio.

# Configuration

Make sure that you’re inside the virtual environement :

```bash
cd Ctrl_Alt_Discuss
poetry env list
```

Which should return a result such as  :
`ctrl_alt_discuss-Z2Ju98Sf-py3.11 (Activated)`

Otherwise try the following command :

```bash
poetry env use env_name||python||python3||python3.X
```

## Installing Dependencies

Make sure to install the necessary dependencies by running the following command:

```bash
cd Ctrl_Alt_Discuss
poetry install --no-root
```

## Setting Environment Variables

```bash
export POETRY_OPENAI_API_KEY="your_openai_api_key_here"
export POETRY_XI_API_KEY="your_xi_api_key_here"
export POETRY_CAD_ROOT_PATH="/path/to/Ctrl_Alt_Discuss"
```

## Running the project

```bash
cd Ctrl_Alt_Discuss
poetry run python -i src/main.py
```
___

# References

- [OpenAI GPT-3.5-turbo](https://platform.openai.com/)
- [OpenAI TTS](https://platform.openai.com/docs/guides/text-to-speech)
- [Eleven Labs AI TTS](https://www.eleven-labs.ai/text-to-speech)
- [Poetry](https://python-poetry.org/docs/)
