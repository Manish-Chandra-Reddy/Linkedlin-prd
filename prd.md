# Unlimited InMail to Recruiters and Professionals Without LinkedIn Premium

## Objective
Enable non-Premium LinkedIn members to send unlimited InMail messages to verified recruiters and selected professional contacts, increasing engagement, platform utility, and recruiter reach while preserving LinkedIn’s Premium value.

---

## 1. Background
- LinkedIn Premium is currently required for unlimited InMail access.
- Many users need to contact recruiters or professionals for career opportunities, hiring, and networking.
- Removing InMail limits for these target groups can boost platform usage, candidate flow, and recruiter success without broadly eroding Premium differentiation.

## 2. Problem Statement
- Non-Premium users are blocked by InMail caps when trying to reach recruiters or professionals who are likely to respond.
- This creates friction in talent sourcing, job search, and network growth.
- Recruiter-facing use cases suffer because candidates cannot initiate contact freely.

## 3. Goals
- Provide unlimited InMail access for defined recruiter/professional segments to non-Premium users.
- Maintain Premium value by limiting the feature scope to targeted recruitment-related communications.
- Improve candidate-recruiter connections and platform engagement.
- Reduce cold outreach friction while preserving spam controls and user trust.

## 4. Scope

### In Scope
- Unlimited InMail to:
  - verified recruiters
  - LinkedIn Recruiter / Recruiter Lite users
  - professionals marked with hiring/recruiting roles
- Maintain existing limits for:
  - non-recruiter professionals
  - general networking outreach
- Implement guardrails for abuse and spam
- Track usage and impact through analytics
- Update UX to surface the new capability for eligible senders

### Out of Scope
- Unlimited InMail to all LinkedIn members
- Replacing Premium InMail for sales or broad business development messaging
- Premium feature changes unrelated to InMail volume

## 5. User Personas

### Persona 1: Job Seeker
- Needs to reach recruiters quickly
- Lacks Premium subscription
- Wants to apply or inquire about roles without waiting for recruiter contact

### Persona 2: Recruiter
- Wants more candidate inbound messages
- Uses LinkedIn Recruiter / Recruiter Lite
- Benefits from higher candidate engagement

### Persona 3: Passive Professional
- Open to recruiter approaches
- May receive InMail without needing Premium to start the conversation

## 6. User Stories

### Core Stories
1. As a job seeker, I want to send unlimited InMail messages to verified recruiters so I can reach hiring teams without buying Premium.
2. As a non-Premium member, I want to message professionals with recruiting roles without hitting an InMail cap.
3. As a recruiter, I want more candidates to be able to contact me directly so I can fill roles faster.

### Edge Stories
4. As a user, I want to know when InMail is unlimited to a recruiter versus when it is limited to avoid confusion.
5. As a user, I want spam protections so recruiter messages remain meaningful and not abused.

## 7. Requirements

### Functional Requirements
- FR1: Identify eligible recipients:
  - “Recruiter” badge/attribute
  - LinkedIn Recruiter / Recruiter Lite account status
  - verified recruiting or hiring role
- FR2: Allow unlimited InMail sends from non-Premium users to eligible recipients
- FR3: Preserve existing InMail limit behavior for ineligible recipients
- FR4: Display clear messaging in the compose flow when unlimited InMail applies
- FR5: Add tracking to measure:
  - volume of unlimited InMail sends
  - conversion/reply rates
  - abuse or spam reports
- FR6: Apply spam controls:
  - rate limiting per sender across all recipients
  - quality filtering for repeated low-response patterns
  - reporting and automated enforcement

### Non-Functional Requirements
- NFR1: Ensure zero degradation to existing InMail infrastructure performance
- NFR2: Keep message delivery and read tracking consistent
- NFR3: Support rollout with feature flagging and A/B testing
- NFR4: Protect user privacy and comply with policies

## 8. UX / UI

### Compose Experience
- When sending an InMail to an eligible recruiter:
  - show badge/icon: “Unlimited InMail to recruiters”
  - show explanatory microcopy: “No InMail credits required for this recipient.”
- When sending to ineligible recipient:
  - preserve existing credit balance and prompts

### Profile / Search Experience
- On recruiter profiles or search results:
  - surface recruiter status clearly
  - indicate that candidates can message them without Premium

### Onboarding / Education
- Add short help text in Messaging and Premium pages:
  - “You can send unlimited InMail messages to verified recruiters even without Premium.”

## 9. Metrics / Success Criteria

### Adoption Metrics
- Increase in inbound messages to recruiters from non-Premium users
- Volume of unlimited InMail sent
- Number of non-Premium users using the feature

### Quality Metrics
- Response rate to unlimited InMails
- Spam/report rate for recruiter-targeted messages
- Recruiter satisfaction / engagement

### Business Metrics
- Retention lift for non-Premium users engaging recruiters
- Recruiter productivity improvement
- Premium conversion delta remains neutral or positive

## 10. Risks & Mitigations

### Risk: Premium devaluation
- Mitigation:
  - restrict unlimited InMail to recruiters and verified hiring professionals only
  - keep all other Premium benefits unchanged

### Risk: Spam / abuse
- Mitigation:
  - monitoring and enforcement
  - abuse thresholds
  - recipient controls and reporting

### Risk: Confusion about feature boundaries
- Mitigation:
  - clear UI messaging and eligibility indicators
  - help articles and FAQs

## 11. Dependencies
- Recruiter / professional classification data
- InMail eligibility service
- Messaging compose UI
- Analytics instrumentation
- Spam detection / enforcement systems

## 12. Release Plan
1. Define eligible recruiter/professional criteria
2. Build backend eligibility and compose flow support
3. Add UI indicators and explanatory copy
4. Launch experiment to a subset of non-Premium users
5. Monitor metrics and iterate
6. Expand to full rollout if metrics show improved recruiter/candidate engagement with controlled abuse

## 13. Open Questions
- Which exact recruiter accounts qualify? (Recruiter Lite vs all recruiting roles)
- Should the feature apply globally or start in target markets?
- How should recruiter recipients be labeled to avoid false expectations?

## 14. Appendix

### Definitions
- InMail: LinkedIn direct messaging channel for contacting members outside your network.
- Verified recruiter: a member with recognized recruiting tools or role attributes.
- Non-Premium user: any member without an active LinkedIn Premium subscription.

### Non-Goals
- Unlimited InMail for sales or cold outreach unrelated to recruiting.
- Altering Premium pricing or membership tiers.
