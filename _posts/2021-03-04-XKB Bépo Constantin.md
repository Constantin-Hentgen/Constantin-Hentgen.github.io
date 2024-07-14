---
title: XKB Bépo Constantin
date: 2021-03-04 12:00:00 +0100
categories: [Personal project, Setup]
tags: [linux, keyboard layout]
render_with_liquid: false
---

# Typing Frequency Analysis Program

## Objective

Building on my initial experiences with typing, I developed a program to analyze the frequencies of letters and characters in various texts. The goal is to generate an optimal keyboard configuration based on these frequencies. The program can compare up to three text sources and produce a detailed PDF report.

The frequency analysis examines characters common across different sources, averages the results, and classifies them by language based on these averages. This analysis aids in designing keyboard layouts by optimizing the distribution of typing load between hands and prioritizing faster, more powerful fingers.

Here are excerpts from a report comparing text sources in different languages:

![Frequency Analysis Report](https://user-images.githubusercontent.com/48366000/224126966-b4580f54-669c-4bcf-a34a-cec491cdec4c.png)

The program calculates the frequency of letter appearances and helps determine the optimal positioning of letters on a keyboard. This allows for better distribution of typing effort and reduces strain by assigning letters to fingers based on their speed and strength.

For example, the graph above shows that the letter "e" is heavily used in German compared to French, which uses it less. Additionally, French uses the letter "h" less frequently than English and German, reflecting linguistic variations.

![Frequency Analysis Comparison](https://user-images.githubusercontent.com/48366000/224127015-9b66307e-e4bd-46f8-88b0-da6defe3024b.png)

## Feedback

Developing this program has been both enjoyable and enlightening. It provided insights into the principles behind optimized keyboard layouts and offered a playful exploration of linguistic patterns. I enjoyed seeing how theoretical concepts could be applied practically to improve typing efficiency.

## Technologies Used

The development of this program involved several technologies and libraries:

- **Python3**: The primary language used for implementing the program's logic and analysis.

  - _Source:_ [Python Official Website](https://www.python.org/)

- **Pandas**: A library for data manipulation and analysis, used to handle and process text data.

  - _Source:_ [Pandas Documentation](https://pandas.pydata.org/pandas-docs/stable/)

- **Matplotlib**: A plotting library for creating visual representations of the frequency data.

  - _Source:_ [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)

- **ReportLab**: A library for generating PDF reports from Python.
  - _Source:_ [ReportLab Documentation](https://www.reportlab.com/docs/reportlab-userguide.pdf)

## Project Repository

For more information on the implementation, access the source code, and explore the project, visit the GitHub repository:

- [Typing Frequency Analysis GitHub Repository](https://github.com/Constantin-Hentgen/Typing-Frequency-Analysis)

## License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/Constantin-Hentgen/Typing-Frequency-Analysis/blob/main/LICENSE) file for more details.

---

_Note: This post is written in Markdown, a lightweight markup language with plain text formatting syntax. Markdown allows you to create formatted text using a plain text editor._

## References

- [Python Official Website](https://www.python.org/)
- [Pandas Documentation](https://pandas.pydata.org/pandas-docs/stable/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
- [ReportLab Documentation](https://www.reportlab.com/docs/reportlab-userguide.pdf)
- [Typing Frequency Analysis GitHub Repository](https://github.com/Constantin-Hentgen/Typing-Frequency-Analysis)
