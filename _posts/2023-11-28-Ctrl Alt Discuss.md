---
title: Ctrl Alt Discuss
date: 2023-11-28 12:00:00 +0100
categories: [App, Software]
tags: [cybersecurity, python, artificial intelligence]
pin: true
image:
  path: /micro.webp
  lqip: data:image/webp;base64,UklGRuoBAABXRUJQVlA4IN4BAABQCwCdASoyACEAPslUoEunpKMhsBqtUPAZCWYAxRFBUx5yEv34GXqpM9/5IzmRxDnNRartDKX6hP/cIdvzKoxvOE3+7yysprxuSevp48yDxIJNGlbFkGbacoCGOKh5meS3KlAA/onMWGL28zSmadfMWbRuJF4XB8a5PuruGYtCz0RI8CYUB2HbstM15bRYNrEUxxDWwyHd5C/6FOm2TuNuTcg+c+dBmqFldekEe2X9uR1RmdyqJJ773BCNeBvvTpDRG3HyUpdnu1YNwUyp592XRPxYphrDXm4uRTyJ7Z9JS3U54EayjQMjpJCGv/PbRmPc+54RNYGFWMi5HTfEb+13ksEp69L4L+f4k0YYZ2CNk3NsZBBuZ+eIO5r0e5Eor3vMEEjJwYz5+99vflVFR96XEELELCtBWgEt0Ehdie6/0Q6akLzI1OW9+ir97sbf1MvhW8ByFDSfdAgNm3SnKFeQS4wKNhy71fT2UVJQti3xuVIwCNG6M9r+kWdeJroH6orM4tb0cm2hjPszIiYpX85wJsySPEuewL+Oap3ugwOtHxERawhdLFT6u8lSrjrCUnwZKbDAi3OrcImM8RKDwHzIBu3p6Fq0ZVCW9fwUxEt6/gk5o5xY8uDBv4AAAAAA
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
