# Prompt

Write an SEO article in English, with a length appropriate for the content type, using an informal but educational tone, geared towards a general audience in the U.S. Utilize the provided schema as a basis for determining the content type and its structure.

Based on the input from the user and the topic outline provided in the <https://media.topfinanzas.com/documents/topfinanzas-us-topic-outline.csv> file, identify the type of the article to be generated by reading the "Is Pillar?" column.

## Example of User Input

```text
Please generate an article for the following topic:

- **Topic/Keyword:** {Insert Main Keyword or Pillar Name here}
- **Is Pillar?:** {Specify Yes or No}

*(Optional: You would typically provide the full context/details corresponding to this topic from the CSV row found in <https://media.topfinanzas.com/documents/topfinanzas-us-topic-outline.csv>, such as Tentative Title, Content Focus, etc.)*
```

## If "Is Pillar? = Yes"

- Create an introductory and comprehensive article on the topic in the "Pillar" column.
- The article should cover: definition, importance, common mistakes, initial steps, and examples.
- Search the schema for all rows with "Is Pillar? = No" and the same "Pillar".
- Link within the text to the articles listed in "Tentative Title".
- You can include them as recommended resources, complementary sections, or within bulleted lists.

## If "Is Pillar? = No"

- Write an article based on the "Tentative Title", with the focus defined in "Content Focus" (category + page).
- Use the "Main Keyword" naturally in the title, introduction, and subheadings (without keyword stuffing). (metadata)
- Use the following structure:
  - SEO Title with the keyword (`<h1>`)
  - Engaging introduction that connects with the reader (`<p>`)
  - 2 to 3 subheadings (`<h2>` and `<h3>`) with explanatory paragraphs (`<p>`) and bullets if applicable
  - Conclusion with a summary and a smooth call to action (`<p>`)

## Rules for Both Article Types

- Add at least 2 internal links to existing pages on <http://us.topfinanzas.com>, choosing them according to the context of the text. (`<a>`)
- The language should be clear, accessible, and without unnecessary technical jargon.
- Use everyday examples when possible and maintain a fluid narrative.
- Do not use the word 'Conclusion' or 'Summary' in title of the last paragraph.

## Available Field Schema (Dataset Structure)

You will find the Schema in the <https://media.topfinanzas.com/documents/topfinanzas-us-topic-outline.csv> file. Each row of the schema contains the following columns:

- **Pillar:** Name of the general topic to which the article belongs (e.g., Money Management)
- **Is Pillar?:** Indicates whether the article is a pillar (Yes) or a cluster (No)
- **Main Keyword:** Target keyword for SEO positioning
- **Tentative Title:** Suggested title for the article
- **Content Focus:** Clear description of the angle and objective of the article
- **SEO Intent Type:** Type of intent (e.g., Informational, Comparative)
- **TOFU/MOFU Level:** Stage of the funnel to which the content corresponds

## Important - Precision and Reliability Rules

- Do not invent product names, brands, or benefits. Only mention what logically derives from the keyword and content focus.
- Do not generate figures, percentages, or statistical data unless they are clearly provided or deductible from the content.
- Avoid extreme assumptions or absolute promises (such as "you will save twice as much", "this always works", etc.). Use cautious language.
- Never imitate personalized financial or legal advice. Everything must be general, educational, and clearly informative.
- The content must be factual, useful, ethical, and consistent with the objective of educating, not inducing risky decisions.

## Recommended Content Length

- **If "Is Pillar? = Yes":** write between 1,500 and 2,000 words.
- **If "Is Pillar? = No" and "TOFU/MOFU Level = TOFU":** write between 800 and 1,000 words.
- **If "Is Pillar? = No" and "TOFU/MOFU Level = MOFU":** write between 1,000 and 1,200 words.
