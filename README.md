# Supplementary Methodology for SEATUC 2027

**Paper:** 労働生産性に関連するコミュニケーション条件の比較：LLMベースAIエージェントによるMotivation関連評価

This repository provides supplementary methodological information for the paper submitted to SEATUC 2027. Its purpose is to document the conversation conditions and Motivation-related evaluation procedure in greater detail than is possible within the paper's page limit. This repository is a methodological supplement, not an independent measurement of human motivation or labor productivity.

## Study overview

Communication-related conditions were derived from a review of prior research. In each experimental session, locally hosted LLM-based agents exchanged messages via Mastodon. A target agent (Agent A) then generated a post-conversation Motivation score in response to an evaluation prompt. The study compares the scores observed across conditions rather than directly measuring labor productivity.

## Experimental environment

| Item | Setting |
| --- | --- |
| Conversation platform | Mastodon (local environment) |
| LLM designation used in the study | Gemma4 (exact model identifier/version not documented) |
| Temperature | 0.7, held constant across conditions |
| Maximum generation tokens | 2048 |
| Sessions | Independent conversation sessions; previous session histories not carried forward |
| Repetitions | 30 planned for each of 16 conditions |
| Evaluation target | Agent A |
| Baseline conversation | Agent A → Agent B → Agent A; 3 utterances |
| Three-agent conversation | 3 agents, configured maximum 5 turns |

Temperature 0.7 was selected provisionally to allow response variation; it was **not** optimized through fitting or a sensitivity study. Other model/runtime details that were not recorded are not inferred here.

## Experimental conditions

Six pairs of High/Low settings plus four additional conditions (16 conditions total):

1. a and b (baseline)
2. contentOfRemarks High
3. contentOfRemarks Low
4. politeness High
5. politeness Low
6. informationSharing High
7. informationSharing Low
8. support High
9. support Low
10. communicationStyle High
11. communicationStyle Low
12. leader'sApproach High
13. leader'sApproach Low
14. emoji moderate
15. a and b and c
16. casual conversation

`emoji none` was excluded from the final set and is not included in the baseline.

See [experimental conditions](methodology/experimental_conditions.md) and [source-configuration verification](methodology/source_configuration_checklist.md). The descriptions in the comparison table are explanatory summaries, **not substitutes** for the exact experiment-time Persona/Behavior Policy fields.

## Motivation evaluation

The common initial reference score is **50/100**, which is not a human pre-test measurement. After each conversation, the evaluation LLM is prompted to take the perspective of the participating target agent and generate a score between 0 and 100, along with a reason. No additive numerical rubric is applied. See [the complete evaluation prompt](methodology/motivation_evaluation_prompt.md).

The baseline condition produced a mean *post-conversation* Motivation score of **61.33** over 30 runs. This mean is different from the common initial reference score of **50**. Differences between conditions are reported relative to 61.33, while within-session change is relative to 50.

There were 480 planned runs and 479 usable Motivation evaluations; one evaluation was missing in the informationSharing Low condition.

## Manipulation check

A separate manipulation check examines actual generated utterances for the targeted communication characteristics, independently of the score-generating agent's rationale. The protocol is documented in [manipulation_check/method.md](manipulation_check/method.md). Results must be added after checking the logs; no results are fabricated in this repository.

## Scope and limitations

The study assesses an LLM-generated Motivation-related score, not observed human motivation or directly measured productivity. High/Low operationalization differs by factor, so the magnitude of condition differences must not be interpreted as comparable causal effect sizes. Release of raw conversations or per-run scores is not required for the purpose of documenting the methodology, but their absence limits independent re-analysis of the manipulation check.

**Publication status:** The detailed condition settings have been provided as screenshots. Before publication, the exact agent fields and Knowledge content should be copied from the original application/configuration records into this repository and checked against the actual run configuration. Until then, the condition table is a documented overview rather than a complete executable specification.
