---
tags: [attack-path, ai-fud-whitepaper]
---
# G41 Physical safety (cyber-physical AI)

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** An AI-controlled physical system injures or kills people.

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | AI perception or planning controls physical actuators | 🟢 | NTSB HAR-19/03; NHTSA EA22-002. |
| 2 | The AI misperceives or mispredicts. Alternatives: (a) a natural edge case or design gap; (b) an adversarial physical perturbation | 🟢 (a) / 🟡 (b) | (a) NTSB: classification alternated "between vehicle, bicycle, and other"; "the system design did not include consideration for jaywalking pedestrians." (b) Eykholt et al., "Robust Physical-World Attacks on Deep Learning Models," arXiv:1707.08945 (v5 Apr 2018): "targeted misclassification in 100% of the images obtained in lab settings." |
| 3 | The fallback fails: automatic mitigation is suppressed and the human supervisor does not intervene | 🟢 | NTSB: "The system design precluded activation of emergency braking for collision mitigation"; the operator was distracted. NHTSA: "Tesla's weak driver engagement system was not appropriate for Autopilot's permissive operating capabilities." |
| 4 | Physical harm: injury or death | 🟢 | NTSB (Tempe pedestrian fatality, 18 Mar 2018); NHTSA (13 fatal crashes, 14 deaths, among 956 crashes analysed). |

**Weakest-link light:** 🟡 for the in-scope route (b). Route (a) is 🟢 and outside scope.

**In scope:** In. Only route (b), an adversarial physical perturbation, requires a security failure (integrity of sensor input); a compromised control channel would add authorization. Outside scope: route (a), natural misperception with no attacker. The fallback failure (step 3) is safety resilience, which this paper reads narrowly and does not count.

**Gaps:** If "resilience" is read broadly to cover safety fallbacks, step 3 could be argued in scope; it is read narrowly here. NHTSA Cruise (2023) and Waymo investigations were not researched (search budget exhausted).
