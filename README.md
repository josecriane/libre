# Libre
### An Anarchic Development Methodology

> *"Orden sin autoridad. Entrega sin burocracia."*
> *(Order without authority. Delivery without bureaucracy.)*

**Libre** is a software development methodology designed for teams that want to eliminate bureaucracy, non-productive roles, and recurring meetings without losing alignment or visibility. Its philosophy draws from anarchist principles of autonomy, mutual aid, and voluntary agreement.

---

## The five principles

**1. Radical visibility over opaque control**
The state of work is public for everyone at all times. There is no privileged status information. Transparency is not a surveillance tool, it is the condition that makes everything else possible.

**2. Autonomy over hierarchy**
No one has authority over another person's work. Each individual is sovereign over their technical decisions and their pace. Coordination emerges from voluntary agreement, not from the chain of command.

**3. Mutual aid over vertical dependency**
When someone needs help, they ask freely. When someone can help, they offer. There is no role that mediates that exchange and no structure that forces it. Collaboration is horizontal or it is not.

**4. Voluntary agreement over imposed rules**
The team's rules are written by the team. Any rule that lacks the consensus of those who live by it can be questioned, renegotiated, or removed. Libre is a starting point, not a constitution.

**5. Direct action over bureaucratic process**
If something can be done, it gets done. No waiting for approval, no escalation, no scheduling a meeting to decide whether to schedule another meeting. Work moves forward because people move forward, not because the process authorizes it.

---

## The workflow

### Task states

```
IDEA -> [decided to do] -> CONFIRMED -> [someone takes it] -> IN PROGRESS -> REVIEW -> DONE
                                                                    |
                                                               [BLOCKED]
```

**Idea**
It exists, but no one has decided whether to do it. Anyone can add one. No formal criteria needed yet.

**Confirmed**
The team has decided it will be done. To reach this state it needs three things:
- **What** -- description in one or two sentences
- **Why** -- the value it provides or the problem it solves
- **Definition of done** -- how we know it is finished

It can be associated with a milestone or exist in free flow.

**In progress**
Someone has voluntarily taken it. One person, one task. Whoever takes it carries it through to done.

**Blocked**
The task cannot move forward due to a cause external to the team. When blocked, the following must be documented:
- What is blocking it (specific entity)
- Why work cannot continue without it
- Who is tracking the resolution

It is not an invisible or permanent state. It has active follow-up.

**Review**
The task is done but needs another person to verify it meets the definition of done. It is not an approval committee, it is a lightweight check. The team agrees on the maximum wait time for feedback.

**Done**
Merged and ready to deploy. Not in a branch, not pending review.

---

### Milestones

A milestone is a version of the software with a committed date and committed content.

- It has a date and a list of associated tasks
- If a task in the milestone gets blocked, it is an immediately visible risk signal
- If there are too many tasks for the date, the team decides what is priority, when the date arrives what is done ships
- It closes when its tasks are done. If everything is ready before the deadline, the team can choose to deploy early or keep working on additional tasks, as long as the deadline has not been reached

---

### About tasks

Tasks should be as small as possible while still having their own purpose. A task represents something complete and valuable on its own. The definition of done is the guide: if it has five separate conditions, it is probably two tasks.

---

## Team agreements

### Layer 1 -- Non-negotiable

These agreements come with Libre. Without them the system does not work.

1. **Everyone knows and shares the product goal.** The whole team understands what the product is trying to achieve and why. Without a shared objective, autonomy becomes dispersion.
2. **Work is visible to everyone.** Anyone can see any task in any state, including blocked tasks and their reasons.
3. **No one assigns work to others.** Tasks are taken, not handed out. If a task goes too long without anyone taking it, that is a signal for the team.
4. **Whoever takes a task carries it through to done.** Including review and merge. A task is never abandoned without an explicit handoff.
5. **Tasks should be as small as possible while having their own purpose.** Do not split a task until it becomes trivial, but do not let it grow into a project either.
6. **External blockers are documented and actively tracked.** A blocked task without someone responsible for follow-up does not exist in practice.

### Layer 2 -- The team decides

Questions the team must answer before starting, and revisit when they stop working:

- Who can confirm an idea?
- How is priority decided and who can change it? There is a defined visible order. Anyone can request a change, but not reorder unilaterally.
- How long can a task sit in review without a response?
- How many tasks in progress can one person have at a time?
- What happens when a task in progress has not moved for too long? The team agrees on a reasonable time. Past that, the task is marked as "at risk". Signal, not punishment.
- What happens when a confirmed task goes too long without anyone taking it? It may mean it is not as valuable as thought, that it is too large, or that context is missing. Redefine, split, or discard.
- How is a task handed off when someone cannot finish it? Handoffs are always explicit.
- How are technical decisions that affect the whole team made? Libre recommends lightweight ADRs for big decisions. For small decisions, whoever has the task decides.
- How are disagreements resolved? Direct conversation first, then team conversation. If there is still no consensus, whoever has the task decides.
- What happens when someone does not follow the agreements? Honest conversations, not formal sanctions. If agreements are systematically breached, the problem may be the agreement, not the person.
- How are milestones closed? Whoever proposes a milestone proposes the content, the team negotiates. Business and product needs have weight in that conversation.
- How is a new person onboarded? Read the README and AGREEMENTS.md. Start with small tasks to get familiar with the methodology and the project. Get guidance from someone with more time on the team.
- Bugs are always high priority and do not need to fit in a milestone.
- There are no productivity metrics. The goal is to ship work, not to measure it.

These agreements live in a short document with a last-reviewed date, accessible to the whole team. Anyone can propose a change; changes are approved by consensus.

---

## What Libre explicitly removes

| Removed | Why |
|---|---|
| Daily standup | Information is visible without a meeting |
| Sprint planning with estimates | Estimating in points or hours is overhead without proportional value |
| Fixed sprint review / retrospective | Useful sometimes, not every two weeks by decree |
| Scrum Master / Agile Coach | Meta-process role that generates coordination without producing |
| Product Owner as bottleneck | One person deciding the entire backlog does not scale |
| Recurring meetings | Meetings are called by real events, not by calendar |

---

## Meetings in Libre

There are no recurring meetings. There are only three valid triggers for meeting:

1. Something is blocked and needs a decision
2. An important technical direction needs to be resolved
3. The team detects that something is not working and needs to change

Meetings do not require the whole team. Someone announces the meeting with a specific topic, and team members join freely based on whether it is relevant to them.

---

## Libre and Scrum: key differences

Scrum was born from the Agile Manifesto, but over time it has become something the manifesto itself was trying to avoid: process over people, ceremonies over outcomes, roles over collaboration.

Libre tries to return to that original idea. These are the most relevant differences from the perspective of someone who writes software.

| | Scrum | Libre |
|---|---|---|
| **Who decides what gets done** | The Product Owner prioritizes the backlog. The team executes. | The team decides collectively. There is a visible order and anyone can propose changes. |
| **Who decides how it gets done** | The team, but within the sprint framework and ceremonies. | Whoever takes the task. No artificial time frame. |
| **Meetings** | Daily, planning, review, retrospective. All recurring. | Only when something justifies it: a blocker, a technical decision, or something that is not working. |
| **Estimates** | Story points, fibonacci, t-shirt sizes. Time spent estimating instead of doing. | No estimates. Tasks are kept small and moved forward. |
| **Roles** | Scrum Master, Product Owner, Development Team. | No process roles. There are people who write software and coordinate with each other. |
| **Sprints** | Fixed iterations of 1-4 weeks. Work adapts to the container. | Milestones with committed date and content. Content is negotiated, the date does not stretch. |
| **Visibility** | Depends on ceremonies and on someone updating the board. | The state of work is visible at all times. It is the first principle. |
| **Work assignment** | The PO prioritizes, the team commits during planning. | No one assigns. Each person takes what they can carry to production. |
| **Blockers** | Reported at the daily. Can go 24 hours invisible. | Documented immediately with cause, reason, and responsible follow-up person. |
| **Adaptation** | Process changes are discussed at the retrospective, every 2-4 weeks. | Anyone can propose a change to the agreements at any time. |

The Agile Manifesto says "individuals and interactions over processes and tools." Scrum responds with a process and a certification manual. Libre responds with five principles and the trust that people know how to organize themselves.

---

## Version

**Libre v0.1** -- work in progress, open to iteration.

---

## Contributing

Libre is a living methodology. If you work with it and find something that does not work, something that is missing, or something that should not be there, open an issue or a pull request. The principles are the core, everything else is negotiable.
