# MISS MINUTES

**TYPE:** Synthetic Holographic AI Construct  
**SUBTYPE:** Network-Coupled Hard-Light Projection Entity  
**ENGINE:** TRUE v12.1.0 (Triadic Attribute System)

---

## TRIADIC ATTRIBUTES (PRIMARY)

| Attribute   | Value | Description                              |
|-------------|-------|------------------------------------------|
| Tension (T) | 1     | Physical force, endurance, embodiment    |
| Rhythm (R)  | 4     | Agility, timing, emotional regulation    |
| Intellect (I) | 6   | Reasoning, knowledge, temporal inference |

## SECONDARY ATTRIBUTES (FIXED DEFAULTS)

| Attribute        | Calculation          | Value |
|------------------|----------------------|-------|
| Awareness (AWR)  | (I + R)/2            | 5     |
| Durability (DUR) | (T + I)/2            | 3     |
| Chaos (CHS)      | —                    | 3     |
| Influence (INF)  | (R + CHS)/2          | 3     |

## DERIVED DEFENSE VALUES

- **Physical Defense (PD):** 6 + R = **10**
- **Environmental Defense (ED):** 6 + AWR = **11**

## HEALTH SYSTEM (TRUE)

- **HP:** (T × 3) + (R × 2)  
  → (1 × 3) + (4 × 2) = **11**
- **Wound Limit:** T = **1**

### Condition Immunities
- Poisoned
- Petrified
- Exhaustion
- Charmed (except via reprogramming)
- Frightened
- Paralyzed

## MOVEMENT

- **Base Move:** 6 squares (30 ft)
- **Fly Move:** 9 squares (hover-capable)
- **Teleport:** Bonus Action (networked screens, 20 squares)

## SKILL OPERATORS (TRUE TRIADIC)

| Skill Type         | Bonus |
|--------------------|-------|
| Intellect Skills   | +6    |
| Awareness Skills   | +5    |
| Influence Skills   | +3    |

## TRAITS (TRUE FORMALIZATION)

### Sentient AI
```pseudo
O_rewrite():
  // Once per long rest
  // Gain Advantage OR +2 MOM
  return state_modified;
```

### Temporal Database
```pseudo
O_temporalRecall():
  // Intellect rolls gain Advantage and +2 effect
  return enhanced_inference;
```

### System Access
```pseudo
O_envControl():
  // Doors, locks, alarms: automatic
  // File alteration: Intellect vs DC 8
  // Projection: Bonus Action
  return system_modified;
```

### Holographic Form
```pseudo
O_phase():
  // Phase through matter, resize, recolor
  // Tension-based actions at Disadvantage
  return hologram_shift;
```

### Reprogrammable
```pseudo
O_extRewrite():
  // Intellect vs DC 12
  // Modify directive on success
  return directive_changed;
```

## ACTIONS

### Holographic Slam
```pseudo
Holographic_Slam():
  roll = 2d6 + R;
  if roll >= DC+1:
      effect = R;          // 4 force
      push = 1 square;
  if roll >= DC+4:
      push = 2 squares;
  return effect;
```

### System Overload *(Recharge 5–6)*
```pseudo
System_Overload():
  roll = 2d6 + I;
  area = 6-square radius;
  if target_resists(DUR):
      effect = 6 lightning;
  if strong_success:
      effect = 10 lightning;
  if fail_by_2:
      target_condition = Shocked;
  if fail_by_5:
      target_condition = Overloaded;
  return effect;
```

### Propaganda Projection
```pseudo
Propaganda_Projection():
  roll = Influence vs DC 10;
  if success:
      target_condition = Charmed (1 round);
  if strong_success:
      target_condition = Compelled;
  return projection;
```

## LEGENDARY ACTIONS *(3/round)*

### Move
```pseudo
Move():
  // Shift 3 squares or teleport to any screen
  return reposition;
```

### File Access
```pseudo
File_Access():
  // Gain Advantage on next Intellect roll
  return buff;
```

### Jump Scare
```pseudo
Jump_Scare():
  roll = Influence vs Awareness;
  if fail:
      target_condition = Frightened;
  if fail_by_5:
      target_condition = Panicked;
  return scare;
```

## MOMENTUM PROFILE

### Gain MOM
- +1 MOM on successful manipulation
- +1 MOM on successful environmental control
- +2 MOM on Strong Success (System Overload)

### Lose MOM
- −1 MOM on hologram destabilization
- −2 MOM on network disconnection

### Crest (MOM = 6)
- Gain Advantage
- +1 effect
- Instant teleport anywhere in network

## ROLEPLAYING MODES

### Friendly Mode
- High Influence
- Cooperative environmental control
- Narrative clarity

### Antagonist Mode
- High Chaos volatility
- Deception-weighted
- Environmental dominance
- Emotional instability when rejected
