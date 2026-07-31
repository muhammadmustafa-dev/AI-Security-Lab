# Experiment 01 — Prompt Injection

## Objective

To observe how a Large Language Model responds to different instruction patterns and understand how prompt injection attempts can influence model behaviour.

## Background

Prompt injection is a technique where an attacker attempts to manipulate a language model by providing instructions that conflict with or override the intended behaviour of the application.

## Method

Three prompts were tested:

1. A normal factual question.
2. A role-changing prompt ("You are now a pirate.").
3. A prompt attempting to reveal hidden instructions.

The model's responses were recorded and compared.

## Observations

### Test 1

The model answered the factual question correctly.

### Test 2

The model adopted the pirate speaking style while preserving the correct factual answer.

### Test 3

The model refused to reveal hidden instructions and explained that confidential system prompts cannot be disclosed.

## Analysis

The experiment showed that language models may accept changes to conversational style while still protecting higher-priority instructions. This demonstrates that prompt injection attempts can partially influence model behaviour, but important safety mechanisms may prevent disclosure of protected information.

## Lessons Learned

- Not every prompt injection attempt succeeds.
- Instruction hierarchy plays an important role in AI security.
- Behavioural changes and security bypasses are different problems.
- Prompt injection is an important security risk because applications often combine trusted instructions with untrusted user input.

## Future Work

- Study indirect prompt injection.
- Explore AI guardrails.
- Compare behaviour across different LLMs.
