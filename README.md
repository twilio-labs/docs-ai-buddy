# Docs AI Buddy Prompts

A collection of optimized prompts for documentation-related AI agents.

## 📝 About

Docs AI Buddy is a tool designed to assist documentation teams with AI-driven workflows. It provides prompts for simplifying jargon, generating alt text, editing documents, and more.

Docs AI Buddy was featured at these conferences. Watch the videos below to learn more:

- **AI Engineer Conference**: [Watch the presentation](https://www.youtube.com/watch?v=pSqpC7fFLZA)
- **API the Docs Conference**: [Watch the presentation](https://www.youtube.com/watch?v=fF-dN4VF74Y)

## 🚀 Included Prompts

The repository currently includes the following prompts:

1. **[Simplify Jargon](prompts/simplify-jargon.mdx)** - Simplifies complex technical jargon in documentation.
2. **[Generate Alt Text](prompts/generate-alt-text.mdx)** - Creates concise and informative alt text for images.
3. **[Auto Edit Document](prompts/auto-edit-document.mdx)** - Improves documentation based on style guides and rubrics.
4. **[Generate Metadata](prompts/generate-metadata.mdx)** - Generates SEO meta titles and descriptions.

Each prompt includes:

- Detailed instructions and variables
- Few-shot examples
- Evaluation notes
- Recommended model parameters

## 🛠️ Quickstart

These prompts can be used with various Large Language Model providers. Below is an example of usage:

### Example with OpenAI

```javascript
import OpenAI from "openai";

const openai = new OpenAI({ apiKey: process.env.OPENAI_API_KEY });

const simplifyJargon = async (text) => {
  const response = await openai.chat.completions.create({
    model: "gpt-4o",
    temperature: 0.7,
    max_tokens: 500,
    messages: [
      {
        role: "system",
        content: `Your role is to assist contributors working on documentation:
- Automatically identify and highlight complex technical language.
- Process text to pinpoint jargon-heavy terms and phrases.
- Use the style guide for context only without including sections in your output.
- Provide full form for acronyms on first use.
- Widely known acronyms (e.g., REST API, HTTP, HTML, SQL) need no explanation.
- Give me the revised final version of the text with the heading "Revised Text:"
- Give me the terms that you flagged along with their explanations under the heading "Flagged Content:"`,
      },
      { role: "user", content: text },
    ],
  });
  return response.choices[0]?.message?.content;
};
```

## 📁 Repository Structure

```
docs-ai-buddy-prompts/
├── prompts/                      # Prompt files in MDX format
├── schema/                       # JSON schema definitions
├── .github/                      # GitHub templates
├── CONTRIBUTING.md               # Contribution guidelines
├── CHANGELOG.md                  # Version history
└── README.md                     # This file
```

## 🤝 Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on how to submit new prompts or improve existing ones.

## Code of Conduct

This project follows the [Twilio Labs Code of Conduct](https://github.com/twilio-labs/.github/blob/master/CODE_OF_CONDUCT.md). Please review it before contributing.

## 📝 License

Copyright 2025 Twilio Inc.

This project is licensed under the Creative Commons Attribution 4.0 International (CC-BY 4.0) License. See the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgements

These prompts were developed as part of the Docs AI Buddy project to assist documentation teams with AI-driven workflows.
