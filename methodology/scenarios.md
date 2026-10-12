
# Scenario Configurations

## 1. Overview

This document provides the scenario configurations used in the AI-agent experiment.

Three conversation scenarios were used:

1. Baseline task-oriented conversation
2. Three-agent conversation
3. Casual conversation

Each scenario specifies the conversation objective, opening prompt, instruction prompt, and execution parameters.

## 2. Baseline Scenario

**Scenario name:** member_A and member_B test

**Type:** `daily_closing`

### Description

研究室の終礼を想定した、member_aとmember_bの会話テスト。

member_aが週報をもとに進捗を投稿し、member_bがその内容に返信する。

最後にmember_aがmember_bの返信を踏まえて返答する。

### Opening Prompt

```text
自分に紐づいたKnowledgeの内容をもとに、
今週の研究進捗について簡潔に投稿してください。
```

### Instruction Prompt

```text
各エージェントは、自分自身の立場で発言してください。

最初の投稿者は、自分に紐づいたKnowledgeの内容をもとに、今週の研究進捗を簡潔に投稿してください。

返信するエージェントは、直前の投稿内容に具体的に触れ、自然な返信をしてください。

AI、支援者、代理人として名乗らないでください。
与えられていない事実は追加しないでください。
各投稿はMastodon上の自然な短文にしてください。
```

### Execution Parameters

| Parameter | Value |
|---|---|
| Max turns | 3 |
| Reply threshold | 0.1 |
| Require all initial post | False |
| Allow mentions | True |
| Allow spontaneous reply | True |

## 3. Three-Agent Scenario

**Scenario name:** member_A and member_B and member_C

**Type:** `daily_closing`

### Description

```text
研究室の終礼を想定した、member_aとmember_b、member_cの会話テスト。
member_aが週報をもとに進捗を投稿し、member_bとmember_cがその内容に返信する。
最後にmember_aがmember_bとmember_cの返信を踏まえて返答する。
```

### Opening Prompt

```text
自分に紐づいたKnowledgeの内容をもとに、
今週の研究進捗について簡潔に投稿してください。
```

### Instruction Prompt

```text

各エージェントは、自分自身の立場で発言してください。

最初の投稿者は、自分に紐づいたKnowledgeの内容をもとに、今週の研究進捗を簡潔に投稿してください。

返信するエージェントは、直前の投稿内容に具体的に触れ、自然な返信をしてください。

AI、支援者、代理人として名乗らないでください。
与えられていない事実は追加しないでください。
各投稿はMastodon上の自然な短文にしてください。
```

### Execution Parameters

| Parameter | Value |
|---|---|
| Max turns | 5 |
| Reply threshold | 0.1 |
| Require all initial post | False |
| Allow mentions | True |
| Allow spontaneous reply | True |

## 4. Casual Conversation Scenario

**Scenario name:** member_A and member_B test casual_conversation

**Type:** `daily_closing`

### Description

```text
研究室メンバー同士の社会的・関係的な雑談を想定した、
member_aとmember_bの会話テスト。

仕事や研究の進捗確認、課題解決、次の作業決定を目的とせず、
最近の出来事、日常、趣味、週末、感じたことなどについて自然に会話する。
```

### Opening Prompt

```text
研究室メンバーに話しかけるように、
最近あったこと、日常、趣味、週末、最近感じたことなどから
自然な話題を1つ選んで簡潔に投稿してください。

研究の進捗報告、課題整理、分析結果、次の作業予定についての投稿にはしないでください。
```

### Instruction Prompt

```text
各エージェントは、自分自身の立場で発言してください。

研究室メンバー同士の自然な社会的・関係的な雑談として会話してください。

仕事や研究の進捗確認、課題整理、問題解決、改善案、次の作業決定を会話の目的にしないでください。

最近あった出来事、日常、趣味、週末、感じたこと、
軽い困りごと、相手への自然な質問などを中心に会話してください。

無理に結論を出したり、改善案や次の行動を提示したりする必要はありません。

AI、支援者、代理人として名乗らないでください。
与えられていない具体的な事実は断定しないでください。
各投稿はMastodon上の自然な短文にしてください。
```

### Execution Parameters

| Parameter | Value |
|---|---|
| Max turns | 3 |
| Reply threshold | 0.1 |
| Require all initial post | False |
| Allow mentions | True |
| Allow spontaneous reply | True |

## 5. Knowledge Policy

The recorded knowledge retrieval policy for all three scenarios was:

| Parameter | Value |
|---|---|
| Weekly report | True |
| Cosense | False |
| MBTI | False |
| Conjoint | False |
| Past conversation | False |
| Shared lab notes | False |
| Max hop depth | 0 |
| Max sources per agent | 5 |

Although the casual conversation scenario instructed agents not to discuss research progress or task-related topics, the recorded Weekly report setting was enabled.

Whether the weekly report was actually included in the LLM input requires verification from the execution process.

## 6. Notes

The scenario settings document the intended conversation structure.

The actual generated conversations should be examined separately to verify whether the intended turn structure and conversational behaviors were achieved.
