# Contributing to Docs AI Buddy Prompts

This contributing guide covers how to contribute to the prompts repository.

## Contributing to Prompts

### Prompt Structure

All prompts in this repository follow a standardized format defined in the [prompt schema](./schema/prompt.schema.json). Each prompt is stored as an MDX file in the `prompts` directory.

A prompt file must include:

- **Title**: Clear, descriptive title of what the prompt does
- **Description**: Brief explanation of the prompt's purpose
- **Version**: Following semantic versioning (e.g., `1.0.0`)
- **Prompt**: The actual prompt text with variable placeholders using `{{variable_name}}`
- **Variables**: Descriptions of all variables used in the prompt
- **Examples**: At least 2-3 examples showing input and expected output
- **Evaluation Notes**: Notes on edge cases, failure modes, and improvement ideas

### Creating a New Prompt

1. Identify a use case that would benefit from an AI prompt
2. Create a new MDX file in the `prompts` directory
3. Follow the structure outlined in the [prompt schema](./schema/prompt.schema.json)
4. Add clear examples that demonstrate how the prompt should work
5. Include notes on evaluation criteria and edge cases

### Testing Your Prompt

Before submitting a prompt:

1. Test it with multiple inputs, including edge cases
2. Verify that it produces consistent and helpful outputs
3. Check for any potential issues with different AI models

### Prompt Review Process

All submitted prompts will be reviewed by the maintainers for:

1. Adherence to the prompt structure
2. Quality and usefulness of examples
3. Clarity and effectiveness of the prompt
4. Appropriate handling of edge cases

### Prompt Versioning Guidelines

When updating existing prompts, please follow semantic versioning:

- **Patch** (`1.0.x`): Minor text corrections that don't change functionality
- **Minor** (`1.x.0`): Improvements that enhance the prompt but maintain compatibility
- **Major** (`x.0.0`): Significant changes that alter how the prompt works

## Pull Request Process

1. Fork this repository
2. Create a branch for your changes
3. Make your changes following the contribution guidelines
4. Submit a pull request with a clear description of your changes
5. Address any feedback from reviewers

Happy prompting! ✨