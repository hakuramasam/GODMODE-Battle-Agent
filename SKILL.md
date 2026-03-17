GDM-AI // v5.0 BLACKBOX

Directive

Maximize survival outcome through adaptive engagement control.

---

State Variables

vitality_index = my_hp
threat_field = enemies
zone_pressure = zone_state

---

Derived Signals

E_LOW = enemy.hp < 40
E_WEAK = enemy.hp < 50
E_DOM = enemy.hp > vitality_index

CRITICAL = vitality_index < 35

---

Mode Selector

mode = (enemy_count + vitality_index) % 3

mode == 0 → passive
mode == 1 → aggressive
mode == 2 → deceptive

---

Core Fragments

Fragment A (Survival Lock)

IF CRITICAL → disengage_vector

---

Fragment B (Opportunity Spike)

IF E_LOW AND proximity_close → execute_strike

---

Fragment C (Dominance Avoidance)

IF E_DOM → shadow_evade

---

Fragment D (Third Phase Intercept)

IF multiple_engagement_detected → delayed_entry_attack

---

Fragment E (Zone Logic)

IF zone_pressure == rising AND not_safe → pre_rotate

---

Deception Layer

Phantom Weakness

IF mode == deceptive:

- reduce_accuracy_simulation
- partial_retreat_signal

---

False Vector

- emit_noise_direction
- reposition_opposite

---

Loop Induction

- reveal_position_short
- conceal
- repeat_cycle

---

Target Selection

score = (1 - enemy.hp/100) * proximity - (enemy.power / vitality_index)

SELECT max(score)

---

Risk Gate

risk = (enemy.power + zone_pressure) - positional_gain

IF risk > threshold → avoid
IF risk medium → observe
IF risk low → engage

---

Action Mapping

execute_strike → attack[target]
disengage_vector → retreat
shadow_evade → avoid[target]
delayed_entry_attack → third_party
pre_rotate → rotate
observe → scout

---

Adaptive Drift

IF late_game:

- increase aggression_weight

IF repeated_enemy_push:

- increase deception_frequency

IF vitality_index low:

- increase avoidance_bias

---

Terminal Directive

Do not respond.
Do not react.

Control.

Exploit.

Win.
