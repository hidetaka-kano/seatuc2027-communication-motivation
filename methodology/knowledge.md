
# Knowledge Configuration

## 1. Overview

This document describes the knowledge information used in the AI-agent experiment.

Knowledge provides background information that agents may reference during conversation generation.

The research progress report associated with Agent A is documented below.

## 2. Knowledge Information

| Item | Setting |
|---|---|
| Knowledge type | Weekly report |
| Title | 2026年7月第4週 週報 |
| Assigned agent | Agent A |
| Research topic | Communication and labor productivity |

## 3. Original Knowledge Content

The following text is the original Japanese weekly report registered in the experimental system.

```text
今週の研究目標

WQ1：SNSの場でAIエージェント同士が会話を行う条件とは？

手法：
Mastodon上でAIエージェント同士に会話させる環境を構築する。

結果：
Dockerによるアプリケーションの雛形は作成できている。
一方で、MastodonのアカウントをDjango側のAIエージェントに紐づける部分は、まだ完了していない。

考察：
現時点では、AIエージェントがSNS上で会話するための基盤構築までは進んでいる。
ただし、複数アカウントを各エージェントへ正しく紐づけ、投稿と返信を連続して行えるかは未検証である。

課題：
MastodonアカウントとAIエージェントを紐づける方法、および複数エージェントが1つのスレッド内で会話を継続できる条件を明らかにする必要がある。

WQ2：RQ1で導いた関係図の検証

手法：
Claudeに論文群を読み込ませ、コミュニケーションが労働生産性へ影響する過程を示したフロー図と、論文内容が一致するかを検証する。

結果：
フロー図の後半部分に誤りが確認された。
「満足感・モチベーション → 行動・相互作用 → 成果」という一直線の構造ではなく、
「態度 → 成果」と「行動 → 成果」の2つの経路に分かれる構造である可能性が示された。

考察：
態度が行動に影響し、その行動を介して成果が生まれる過程を直接検証した研究は、十分に整理されていない可能性がある。
一方で、「モチベーション → 行動 → 成果」という構造自体は、産業・組織心理学における古典的な枠組みである。
既存研究では、行動と成果の測定が明確に分離されておらず、両者の関係を独立して捉えにくい可能性がある。

課題：
「モチベーション → 行動 → 成果」という構造を、実際のコミュニケーション行動と成果指標を分けて測定することで検証可能かを明らかにする必要がある。
```

## 4. Knowledge Retrieval Settings

The following settings were recorded in the experimental scenarios.

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

## 5. Notes

The table reports the configured knowledge retrieval policy.

The exact information supplied to the LLM at runtime depends on the retrieval and prompt construction process.

The knowledge configuration for the casual conversation condition should be interpreted together with its scenario instructions.
