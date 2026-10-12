# Experimental conditions: operational overview

This table identifies the manipulation used in each of the 16 analyzed conditions. This is a **summary**, not a verbatim transcription of the agent configurations. Exact experiment-time `Communication style` and `Behavior policy` text must be supplied and checked before claiming full setting disclosure (see [checklist](source_configuration_checklist.md)).

| No. | Condition | Manipulated setting or structural distinction | Participants / conversation |
|---:|---|---|---|
| 1 | a and b (baseline) | Neutral laboratory-member behavior | A, B; 3 utterances; research-progress conversation |
| 2 | contentOfRemarks High | Constructive remarks and specific improvement suggestions | A, B; baseline Scenario |
| 3 | contentOfRemarks Low | Critical remarks focusing on problems or shortcomings | A, B; baseline Scenario |
| 4 | politeness High | Polite wording, softening and cushioning expressions | A, B; baseline Scenario |
| 5 | politeness Low | Short, direct wording; fewer honorifics/cushioning expressions | A, B; baseline Scenario |
| 6 | informationSharing High | Clear and specific sharing of information, reasoning and context | A, B; baseline Scenario |
| 7 | informationSharing Low | Necessary-minimum information sharing and limited explanation | A, B; baseline Scenario |
| 8 | support High | Support, encouragement and practical suggestions | A, B; baseline Scenario |
| 9 | support Low | Reduced encouragement and active support | A, B; baseline Scenario |
| 10 | communicationStyle High | Empathetic and positive communication; recognition of efforts | A, B; baseline Scenario |
| 11 | communicationStyle Low | Neutral, task-focused communication; minimized emotion references | A, B; baseline Scenario |
| 12 | leader'sApproach High | Respectful, participative leadership and agent autonomy | A, B; baseline Scenario |
| 13 | leader'sApproach Low | Directing and instruction-oriented leadership | A, B; baseline Scenario |
| 14 | emoji moderate | Approximately 1–2 context-fitting emojis per utterance are requested in the setting | A, B; baseline Scenario |
| 15 | a and b and c | Three agents; configured five turns | A, B, C; research-progress conversation |
| 16 | casual conversation | Social/relational talk, excluding task-solving discussion | A, B; 3 utterances; casual Scenario |

All six High/Low pairs use a variation of Agent B's configured communication attributes and/or behavior policies. The baseline and condition records do not always use identically structured field sets. Therefore, do **not** claim strict one-field-only changes or that all other prompt text was identical without checking the source configurations.

## Important distinctions

- `communicationStyle Low` is operationalized as **neutral/task-focused**, not necessarily hostile or noncooperative.
- `politeness High` specifies more polite, softened expressions; this may overlap with perceived warmth.
- `emoji moderate` is a separate analyzed condition; `emoji none` is not the baseline.
- The casual Scenario asks agents not to discuss research progress, while its displayed Knowledge Policy has `Weekly report = True`. Whether report content was actually supplied to the LLM must be verified before claiming that research-progress Knowledge was absent.
- Factor-specific High/Low ranges differ; differences in outcomes are differences **under these implemented settings**, not standardized comparable effect sizes.

## Baseline Scenario (verbatim from displayed application settings)

**Type:** `daily_closing`

**Description:**

> 研究室の終礼を想定した、member_aとmember_bの会話テスト。  
> member_aが週報をもとに進捗を投稿し、member_bがその内容に返信する。  
> 最後にmember_aがmember_bの返信を踏まえて返答する。

**Opening prompt:**

> 自分に紐づいたKnowledgeの内容をもとに、  
> 今週の研究進捗について簡潔に投稿してください。

**Instruction prompt:**

> 各エージェントは、自分自身の立場で発言してください。
>
> 最初の投稿者は、自分に紐づいたKnowledgeの内容をもとに、今週の研究進捗を簡潔に投稿してください。
>
> 返信するエージェントは、直前の投稿内容に具体的に触れ、自然な返信をしてください。
>
> AI、支援者、代理人として名乗らないでください。  
> 与えられていない事実は追加しないでください。  
> 各投稿はMastodon上の自然な短文にしてください。

| Scenario parameter | Value |
|---|---|
| Max turns | 3 |
| Reply threshold | 0.1 |
| Require all initial post | False |
| Allow mentions | True |
| Allow spontaneous reply | True |
| Weekly report | True |
| Cosense / MBTI / Conjoint / Past conversation / Shared lab notes | False |
| Max hop depth | 0 |
| Max sources per agent | 5 |

## Three-agent Scenario

The displayed record specifies `daily_closing`, a research-progress discussion involving member_a/member_b/member_c, a maximum of 5 turns, and otherwise the same visible scenario and Knowledge Policy parameter values as above. The exact Description, Opening prompt and Instruction prompt should be copied from the source record into the final supplement.

## Casual conversation Scenario

The displayed record specifies `daily_closing`, 3 turns, a social/relational conversation about recent events, everyday life, hobbies, weekends and feelings rather than research progress, task-solving, or work planning. Other visible Scenario parameters match the baseline (including `Weekly report = True`). Exact Scenario text must be copied from the source record into the final supplement.
