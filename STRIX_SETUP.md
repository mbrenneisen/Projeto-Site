# Strix LLM Configuration Guide

## Overview
This project is configured to use Strix LLM for AI-powered analysis and processing.

## Setup Instructions

### 1. Configure Environment Variables

Copy the `.env.example` file to `.env`:
```bash
cp .env.example .env
```

### 2. Set Your LLM API Key

Edit the `.env` file and replace the placeholder values:
```bash
STRIX_LLM=anthropic/claude-sonnet-4-6
LLM_API_KEY=your-actual-api-key-here
STRIX_TARGET=./
```

### 3. Running Strix

Run Strix with the configured environment:
```bash
export STRIX_LLM="anthropic/claude-sonnet-4-6"
export LLM_API_KEY="sua-chave-aqui"
strix --target ./
```

Or use the environment file:
```bash
source .env
strix --target ./
```

## Configuration Files

- `.env` - Local environment variables (not committed to git)
- `.env.example` - Template for environment variables
- `.strixrc.json` - Strix configuration file with model and target settings

## Environment Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `STRIX_LLM` | LLM model identifier | `anthropic/claude-sonnet-4-6` |
| `LLM_API_KEY` | API key for authentication | Your actual API key |
| `STRIX_TARGET` | Target directory for Strix | `./` (current directory) |

## Supported Models

- `anthropic/claude-sonnet-4-6` - Claude Sonnet 4.6
- Other Anthropic models as supported by Strix

## Notes

- Keep `.env` file secure and never commit it to version control
- `.env.example` should be committed to show configuration structure
- Ensure your API key has appropriate permissions for the models you use
