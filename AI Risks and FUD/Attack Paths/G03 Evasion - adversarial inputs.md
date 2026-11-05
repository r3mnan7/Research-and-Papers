---
tags: [attack-path, ai-fud-whitepaper]
---
# G03 Evasion / adversarial inputs

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Baseline: crafted or modified inputs get past deployed ML detectors such as spam, fraud or face-recognition systems. Maximal: physical-world adversarial changes make safety-critical perception (for example autonomous driving) misread its surroundings, with a risk of physical harm.

**Path (baseline):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Attacker probes or learns how the deployed classifier behaves | 🟢 | Bursztein/Google, May 2018: "Adversaries constantly probe classifiers with new inputs/payloads in an attempt to evade detection." |
| 2 | Attacker crafts an evasive input (digital change, or a physical disguise or object) | 🟢 | Same source: spammer "weaponized this knowledge by adding an invisible first multipart." NIST AI 100-2e2025 p.16: "the suspect used various wigs to evade the face recognition system" (2022 unemployment-fraud case) |
| 3 | Model misclassifies and the detection or control is bypassed (AI does what the concern says) | 🟢 | Same two sources |
| 4 | Attacker gets the fraud, abuse or delivery they wanted | 🟢 | NIST p.16 (fraud case) |

**Path (maximal, physical-world safety):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Attacker places a physical perturbation on a real object | 🟡 | Eykholt et al., arXiv 1707.08945, 2017/18: "targeted misclassification in 100% of the images obtained in lab settings" (84.8% of frames in drive-by tests) |
| 2 | The vehicle's perception model misclassifies it | 🟡 | Same source |
| 3 | The system acts on the misclassification and causes physical harm | 🔴 | NIST p.17: "These are demonstrations of evasion vulnerabilities by researchers, but did not result in attacks in the wild." |

**Weakest-link light:** Baseline 🟢. Maximal 🔴.

**In scope:** Yes. Necessary security failure at step 3: integrity and system control (a security or detection control is bypassed).

**Gaps:**
- MITRE ATLAS AML.CS0004, "Camera Hijack Attack on Facial Recognition System," https://atlas.mitre.org/studies/AML.CS0004 (Type: Incident; reporter: Ant Group AISEC Team): two individuals used it against the Shanghai tax office's facial recognition, starting in 2018, and "were able to fraudulently collect $77 million." ATLAS cites a news report ("Faces are the next target for fraudsters"), not a court record.
- The wig case is evasion of face recognition without a crafted adversarial perturbation.