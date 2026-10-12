
# Agent Configurations

## 1. Overview

This document provides the agent configurations used in the experiment.

Each agent was configured using a communication style and a behavior policy. Experimental conditions were implemented by modifying the relevant attributes of Agent B.

The original Japanese instructions are preserved to document the actual experimental settings.

## 2. Baseline Configuration

### 2.1 Agent A

**Agent name:** `member_a`

**Communication style**

```json
【Agent AのCommunication style全文】
```

**Behavior policy**

```json
【Agent AのBehavior policy全文】
```

### 2.2 Agent B

**Agent name:** `member_b`

**Communication style**

```json
【Baseline Agent BのCommunication style全文】
```

**Behavior policy**

```json
【Baseline Agent BのBehavior policy全文】
```

### 2.3 Agent C

**Agent name:** `member_c`

Agent C was used in the three-agent condition.

**Communication style**

```json
【Agent CのCommunication style全文】
```

**Behavior policy**

```json
【Agent CのBehavior policy全文】
```

## 3. Experimental Configurations

The following configurations describe the experimental conditions applied to Agent B.

### 3.1 Content of Remarks — High

**Agent name:** `member_b_A-High`

**Communication style**

```json
【contentOfRemarks HighのCommunication style全文】
```

**Behavior policy**

```json
【contentOfRemarks HighのBehavior policy全文】
```

### 3.2 Content of Remarks — Low

**Agent name:** `member_b_A-Low`

**Communication style**

```json
【contentOfRemarks LowのCommunication style全文】
```

**Behavior policy**

```json
【contentOfRemarks LowのBehavior policy全文】
```

### 3.3 Politeness — High

**Agent name:** `member_b_B-High`

**Communication style**

```json
【politeness HighのCommunication style全文】
```

**Behavior policy**

```json
【politeness HighのBehavior policy全文】
```

### 3.4 Politeness — Low

**Agent name:** `member_b_B-Low`

**Communication style**

```json
【politeness LowのCommunication style全文】
```

**Behavior policy**

```json
【politeness LowのBehavior policy全文】
```

### 3.5 Information Sharing — High

**Agent name:** `member_b_C-High`

**Communication style**

```json
【informationSharing HighのCommunication style全文】
```

**Behavior policy**

```json
【informationSharing HighのBehavior policy全文】
```

### 3.6 Information Sharing — Low

**Agent name:** `member_b_C-Low`

**Communication style**

```json
【informationSharing LowのCommunication style全文】
```

**Behavior policy**

```json
【informationSharing LowのBehavior policy全文】
```

### 3.7 Support — High

**Agent name:** `member_b_D-High`

**Communication style**

```json
【support HighのCommunication style全文】
```

**Behavior policy**

```json
【support HighのBehavior policy全文】
```

### 3.8 Support — Low

**Agent name:** `member_b_D-Low`

**Communication style**

```json
【support LowのCommunication style全文】
```

**Behavior policy**

```json
【support LowのBehavior policy全文】
```

### 3.9 Communication Style — High

**Agent name:** `member_b_E-High`

**Communication style**

```json
【communicationStyle HighのCommunication style全文】
```

**Behavior policy**

```json
【communicationStyle HighのBehavior policy全文】
```

### 3.10 Communication Style — Low

**Agent name:** `member_b_E-Low`

**Communication style**

```json
【communicationStyle LowのCommunication style全文】
```

**Behavior policy**

```json
【communicationStyle LowのBehavior policy全文】
```

### 3.11 Leader's Approach — High

**Agent name:** `member_b_F-High`

**Communication style**

```json
【leader'sApproach HighのCommunication style全文】
```

**Behavior policy**

```json
【leader'sApproach HighのBehavior policy全文】
```

### 3.12 Leader's Approach — Low

**Agent name:** `member_b_F-Low`

**Communication style**

```json
【leader'sApproach LowのCommunication style全文】
```

**Behavior policy**

```json
【leader'sApproach LowのBehavior policy全文】
```

### 3.13 Emoji — Moderate

**Agent name:** `member_b_emoji_moderate`

**Communication style**

```json
【emoji moderateのCommunication style全文】
```

**Behavior policy**

```json
【emoji moderateのBehavior policy全文】
```

## 4. Configuration Comparison

| Factor | High condition | Low condition |
|---|---|---|
| Content of remarks | Constructive feedback | Critical feedback |
| Politeness | Polite and softened expressions | Direct expressions |
| Information sharing | Detailed information sharing | Limited information sharing |
| Support | Supportive responses | Non-supportive responses |
| Communication style | Empathetic and positive | Neutral and task-focused |
| Leader's approach | Participative leadership | Directive leadership |

The operational definitions and manipulation ranges differed across factors. Therefore, comparisons should be interpreted within the implemented experimental conditions.

## 5. Notes

Access tokens and authentication credentials are excluded from this document.

The configurations above describe the instructions assigned to the agents, not necessarily the communication behaviors observed in the generated conversations.
