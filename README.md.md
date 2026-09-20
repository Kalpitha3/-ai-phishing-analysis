# AI-Generated Emails in Phishing Attacks: Effectiveness and Defense Strategies

**Institution:** University of New Haven — M.S. Cybersecurity and Networks
**Domain:** Threat Analysis / Social Engineering / Applied ML Detection

## Overview
A literature review examining how large language models (GPT-4, Claude, Gemini) have changed
phishing — comparing AI-generated phishing emails against human-crafted ones, evaluating
current detection methods, and identifying where the research still falls short. The review is
built around two research questions: how effective AI-generated phishing is compared to
human-crafted phishing, and which defense strategies actually hold up against it.

## Key Findings
- **AI-generated phishing matches human experts.** In the most comprehensive human-subject
  study reviewed (Heiding et al., 2024; 101 participants), fully AI-automated phishing emails
  (Claude 3.5 Sonnet) achieved a **54% click-through rate** — identical to human-expert-crafted
  emails, and **350% higher** than non-personalized control emails (12%).
- **Frontier models no longer need a human in the loop.** This is a meaningful shift from 2023
  research, where AI-generated phishing still required human assistance to be effective.
- **Detection accuracy varies sharply by method:** traditional spam filters caught AI-generated
  phishing at only **43%** (near chance), a Random Forest classifier reached **71%**, and LSTM
  neural networks reached **87%** by picking up on subtle AI "tells" — unnaturally consistent
  grammar, overly formal phrasing, and repetitive sentence construction.
- **AI can also be the detector:** Claude 3.5 Sonnet, when specifically primed to look for
  phishing, reached **97.25% detection with 0% false positives** in the same study.
- **It's cheap.** Fully automated AI phishing was estimated at ~$0.04 per email while matching
  expert-level effectiveness — profitable at target lists as small as ~2,859 people.

## Research Gaps Identified
- **Limited model coverage** — most research still tests GPT-3/early Claude; detection models
  trained on GPT-3-generated phishing dropped to 62% accuracy against GPT-4-generated content,
  showing how fast this goes stale.
- **No real-world deployment studies** — everything reviewed was lab-based; real inboxes, real
  consequences, and real time pressure are still untested.
- **Small, quickly outdated detection datasets** (the largest reviewed used 381 emails).
- **Thin psychological research** — click-rate data exists, but *why* AI phishing overrides
  scrutiny (which trust heuristics it exploits) is still poorly understood.
- **Technical detection and human training are studied in isolation**, not as a combined
  defense-in-depth system.

## Proposed Defense Strategies
- **Technical:** continuously-updated ML detection, multi-modal analysis (text + SPF/DKIM/DMARC
  + link reputation + behavioral metadata), and explainable-AI detection that shows *why* an
  email was flagged.
- **Human-centered:** move training away from spotting grammar mistakes (now obsolete) toward
  verification habits, metacognitive "slow down and check" skills, and training on realistic
  AI-generated phishing examples rather than dated, error-riddled ones.
- **Organizational:** mandatory SPF/DKIM/DMARC with reject policies, adaptive/risk-based
  authentication, and fast incident-response and reporting pipelines.
- **Collaborative:** industry-wide sharing of AI-phishing campaign indicators, and stronger
  content-safety controls on the AI providers' side.

## Skills Demonstrated
Literature review and synthesis, threat modeling for AI-enabled social engineering, comparative
evaluation of ML detection approaches, and translating academic findings into practical,
layered defense recommendations.

---
*Literature review completed as part of the M.S. Cybersecurity and Networks program at the
University of New Haven.*
