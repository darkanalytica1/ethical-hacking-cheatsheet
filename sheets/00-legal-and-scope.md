# Legal and scope

The most important sheet in the repository, and the one most people skip.

## The one rule

**Test only what you own or have written permission to test.** Everything else
in this repository is subordinate to that sentence.

Unauthorised access to a computer system is a criminal offence in most
jurisdictions (in the UK under the Computer Misuse Act, in the US under the
Computer Fraud and Abuse Act, and under equivalent laws across the EU),
and intent to learn is not a defence. The moment your packets reach a system
you were not authorised to touch, you have potentially committed an offence,
whether or not anything was damaged.

Laws vary by country and change over time. If you are unsure whether something
is lawful where you are, assume it is not until you have checked.

## What "authorised" actually means

A verbal "sure, have a look" from a friend is not authorisation. Authorisation
for a real engagement is written, specific, and signed by someone with the
authority to grant it. It states:

| Element | What it pins down |
| --- | --- |
| **Scope** | Exactly which systems, IP ranges, domains, and applications are in bounds, and which are explicitly out |
| **Time window** | When testing may happen, and when it must not |
| **Methods** | What is permitted (for example, is social engineering allowed? denial-of-service testing? is it forbidden?) |
| **Data handling** | What you may access, what you must not exfiltrate, how findings are stored |
| **Contacts** | Who to call when something breaks, and it will |
| **Get-out** | How to prove you were authorised if a defender or the police ask |

This document is usually called the **rules of engagement**. Do not start
without one on a real target.

## Scope discipline

Scope creep is how well-meaning testers get into trouble. Some habits that keep
you safe:

- **Confirm the scope resolves to what you expect.** A domain in scope may
  resolve to shared hosting where the other tenants are not yours to touch.
- **Stay inside the listed ranges.** If a discovered host is not in scope, note
  it and ask before touching it. Do not follow the trail off the map.
- **Third parties are usually out of scope by default.** A target's cloud
  provider, CDN, or payment processor is not yours to test just because the
  target uses them.
- **Stop and report anything you were not expecting**, such as evidence of a
  prior real compromise. That is now an incident, not a test.

## Practise legally without a client

You do not need a paying engagement to learn. Lawful practice grounds:

- A lab you built yourself, fully isolated. See [the lab guide](../lab/README.md).
- Deliberately vulnerable applications and images designed for practice.
- Public capture-the-flag competitions and their archives.
- Online hacking ranges and labs that grant explicit permission within their
  own platform.
- Bug-bounty programmes, but only strictly within the published scope and
  rules of that specific programme.

## The report is the product

In professional security testing, the finding is not the achievement. The
**clearly written, reproducible, prioritised report that lets someone fix the
problem** is the achievement. A cheatsheet like this teaches the techniques;
the actual job is turning them into something a defender can act on. Every
offensive sheet here ends with the defensive side for that reason.
