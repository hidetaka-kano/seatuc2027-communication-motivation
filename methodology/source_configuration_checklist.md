# Original configuration: transcription and verification checklist

**Do not replace original settings with paraphrased summaries.** Copy the original application fields, redacting authentication credentials, and verify that they match the settings at the time of the experimental runs. Screenshots may reflect subsequently edited configurations.

## Agent configuration records to transcribe

| Condition | Agent configuration source |
|---|---|
| Baseline Agent A | `Kano` / `member_a` |
| Baseline Agent B | `Member B` / `member_b` |
| contentOfRemarks High / Low | `member_b_A-High` / `member_b_A-Low` |
| politeness High / Low | `member_b_B-High` / `member_b_B-Low` |
| informationSharing High / Low | `member_b_C-High` / `member_b_C-Low` |
| support High / Low | `member_b_D-High` / `member_b_D-Low` |
| communicationStyle High / Low | `member_b_E-High` / `member_b_E-Low` |
| leader'sApproach High / Low | `member_b_F-High` / `member_b_F-Low` |
| emoji moderate | `member_b_emoji_moderate` |
| Three-agent condition Agent C | `Member C` / `member_c` |

For each record capture these *verbatim* fields:

- `Communication style` (including all nested keys and `language_rules`, `avoid`, etc.)
- `Behavior policy` (including `response_rules`, `identity_rules`, and all nested keys)
- Any additional system-level agent instructions actually included in the model request

The research theme and research keywords should be preserved if supplied to the model. **Never publish** `Access token`, authentication secrets, or private server credentials. Public Mastodon handles are not needed to understand the method and may be replaced by generic Agent A/B/C labels.

## Knowledge

The screenshot shows a weekly report titled `2026年7月第4週 週報`, attached to Agent A (`Kano`), with research questions WQ1 (Mastodon agent conversation environment) and WQ2 (checking a communication/productivity process diagram). **Copy its entire original Content field from the application** if it was used during the experiment. Do not substitute this summary for the original Knowledge. Verify whether the same report was used for every analyzed session.

## Scenario records

Verify and capture the complete `Description`, `Opening prompt`, `Instruction prompt`, `Max turns`, reply controls and `Knowledge Policy` for:

1. `member_A and member_B test` (baseline)
2. `member_A and member_B and member_C`
3. `member_A and member_B test casual_conversation`

## Publication gate

Mark the supplement **verified** only after all original text has been transferred and compared with the saved experiment-time configuration or logs. If experiment-time settings are unavailable, say clearly that they are the currently observed application settings and that identity with the experiment-time settings could not be independently confirmed.
