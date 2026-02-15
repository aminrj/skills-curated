# CodeRabbit Config Generator

Generates project-specific `.coderabbit.yaml` files by analyzing a repository's PR history, commit patterns, and existing tooling to create custom review rules.

## Install

```
/plugin install trailofbits/skills-curated/plugins/coderabbit-config-generator
```

## Prerequisites

- GitHub CLI (`gh`) authenticated
- Python 3 on your `PATH`
- Local git clone of the repository to analyze
- PyYAML for config validation only (auto-installed when using `uv run`)

## What It Covers

- Automated PR and commit history collection
- Pattern detection for recurring bug categories (shallow copy mutation, silent failures, exception path cleanup, etc.)
- CodeRabbit YAML generation with custom checks, path instructions, and tool configuration
- Config validation (custom check count limits, name lengths, YAML syntax)

## Usage

Ask the agent to generate a CodeRabbit config:

> Run the CodeRabbit config generator skill for this repo using the last 90 days of PRs and commits.

Or run the analysis scripts directly:

```bash
{baseDir}/scripts/run_analysis.sh \
  --repo-path /path/to/repo --repo owner/name
```

## Credits

- **Original source:** [alchemiststudiosDOTai/coderabbit-config-generator](https://github.com/alchemiststudiosDOTai/coderabbit-config-generator)
- **Author:** alchemiststudiosDOTai
- **License:** Not specified
