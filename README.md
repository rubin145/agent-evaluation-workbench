# Agent Evaluation Workbench

Organize evaluation cases, generate and perturb prompts, collect agent responses and review the results in one workflow.

The workbench combines deterministic checks, LLM-based evaluation and configurable metric resolvers. A Python backend and React/TypeScript interface support workflow exploration, review and comparison.

## Workflow

1. Define evaluation criteria and prepare scenarios and prompts.
2. Generate variations and collect responses from the target agent.
3. Evaluate responses using rules and LLM judgments.
4. Review individual results, compare runs and examine the dimensions behind aggregate scores.

Runs and model calls retain context for tracing a result back through the workflow. Technical failures, refusals and content-related violations can be examined separately.

## Evaluation engine

The evaluation engine applies deterministic rules before calling a judge, then computes scores while preserving individual flags and explanations.

[Agent Evaluation Core](https://github.com/rubin145/agent-evaluation-core) is the standalone Python library for response evaluation and aggregation. It includes runnable examples with a simulated judge.

## Choosing evaluation criteria

Exact-match rules depend on the target system's vocabulary. LLM judges require calibration against human judgments. Aggregation weights and caps should reflect the task, and dimensions such as brand alignment apply only where relevant.
