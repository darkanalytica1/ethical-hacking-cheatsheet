# Anonymity and OPSEC

Understanding anonymity tools matters for two honest reasons: knowing their real
limits, and understanding how privacy technologies work. What follows is
conceptual, and none of it makes an unlawful action lawful.

## The tools and what they actually do

| Tool | What it does | What it does NOT do |
| --- | --- | --- |
| VPN | Routes your traffic through another server, hiding your address from the destination | Make you anonymous to the VPN provider, who can see everything |
| Tor | Routes traffic through several volunteer relays so no single one knows both ends | Protect you if you then log into an account tied to your name |
| MAC changing | Changes the hardware address your device advertises on the local network | Hide anything beyond the local network segment |

The recurring lesson: **each tool hides one specific thing, and people
overestimate all of them.** Anonymity is a property of your whole behaviour, not
a switch a tool flips.

## Why MAC changing exists

A device's MAC address identifies it on the local network. Changing it is a
routine privacy and testing action (it is how you avoid being trivially tracked
across a network you are authorised to be on). It is supported on Linux, Windows
and macOS. It affects only the local segment; it says nothing about your
identity to anything past the local router.

## OPSEC, the real subject

Operational security is the discipline of not undermining your own tools. The
tools rarely fail; the person using them does, by:

- Logging into a personal account over an anonymity network, tying it to their
  identity anyway.
- Mixing anonymous and identified activity on the same connection or profile.
- Leaking identity through metadata, writing style, or timing.
- Trusting a single tool to do a job it was never designed for.

## The honest framing

For an ethical tester, anonymity techniques matter mostly so you can:

- **Understand attacker tradecraft** you will see in investigations.
- **Test your own detection**: can your monitoring spot traffic that has been
  routed to obscure its origin.
- **Protect legitimate privacy** in research.

They do not confer permission and they do not confer real invisibility.
Investigators defeat weak anonymity routinely, precisely by finding the OPSEC
mistakes above. The defensive value of this sheet is understanding that
"anonymous" traffic is a claim to be tested, not a fact.
