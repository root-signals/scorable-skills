# Scorable Skills

Skills for integrating and using [Scorable](https://scorable.ai) LLM-as-a-Judge evaluators into applications with LLM interactions.

## What these skills do

- [scorable-integration](skills/scorable-integration/SKILL.md): Guides you through integrating Scorable LLM-as-a-Judge evaluators into your codebase via direct API calls.
- [scorable-otel-evaluation](skills/scorable-otel-evaluation/SKILL.md): Wires end-to-end OpenTelemetry tracing for an LLM application, ships traces to Scorable, and configures server-side evaluation filters that auto-score matching traces. Use when you want production observability + auto-evaluation rather than per-call SDK integration.

## Installation

```bash
npx skills add root-signals/scorable-skills
```

## Usage

The skill automatically activates when you mention evaluation, judges, or Scorable. It works with frameworks like LangChain, PydanticAI, Mastra, and similar agent frameworks.

### Examples

**Basic integration:**
```
Help me add Scorable evaluation to my chatbot
```

**Framework-specific:**
```
Integrate Scorable judges into my LangChain application
```

**Analysis and setup:**
```
Analyze my codebase for LLM interactions and help me set up Scorable evaluation
```

**Production deployment:**
```
Set up production sampling for Scorable evaluation with 10% coverage
```

**OTEL-based tracing + evaluation:**
```
Add OTEL tracing to my pydantic-ai agent and auto-evaluate every trace with Scorable
```

```
Instrument my OpenAI agent with OpenInference and create a filter that scores production traffic
```


## About Scorable

[Scorable](https://scorable.ai) is a tool for creating LLM-as-a-Judge based evaluators for safeguarding applications. It generates custom evaluators (judges) that assess LLM outputs for quality, safety, and policy adherence.
