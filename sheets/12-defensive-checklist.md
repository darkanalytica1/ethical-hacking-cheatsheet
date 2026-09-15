# Defensive checklist

Every offensive sheet in this repository ends with a defence. This sheet
collects them, because the whole point of learning the attacks is to shut them
down. If you only read one page, read this one.

## Network

- [ ] Encrypt everything in transit. This single control defeats
      man-in-the-middle attacks regardless of attacker position.
- [ ] Segment the network so one compromised host is contained.
- [ ] Harden switches (port security; ARP and DHCP protections where available).
- [ ] Secure IPv6 as thoroughly as IPv4, or disable it if unused.
- [ ] Monitor for scans, unexpected services, and sudden ARP changes.

## Wireless

- [ ] Use WPA3 where supported; otherwise WPA2 with a long, random passphrase.
- [ ] Never run WEP or WPA.
- [ ] Separate guest Wi-Fi from the internal network.
- [ ] Use per-user (enterprise) authentication for sensitive environments.
- [ ] Watch for rogue access points broadcasting your network name.

## Web applications

- [ ] Use parameterised queries everywhere. This ends SQL injection.
- [ ] Encode output for its context; validate input on the way in.
- [ ] Never build a file path or trust a file from user input.
- [ ] Run the application and its database account at least privilege.
- [ ] Layer defences: content security policy, secure cookie flags, patched
      components, a web application firewall as a backstop.

## Identity and email

- [ ] Enforce phishing-resistant multi-factor authentication.
- [ ] Publish and enforce SPF, DKIM and DMARC on your domains.
- [ ] Mark external email visibly; filter inbound mail.
- [ ] Give people a simple, blame-free way to report suspicious messages.
- [ ] Verify unusual requests (money, credentials) out of band.

## Systems and access

- [ ] Assume breach: design so one foothold is not a skeleton key.
- [ ] Apply least privilege to every account, service and file.
- [ ] Patch by version; most findings are "old version, known problem".
- [ ] Log activity on the inside, and actually watch it. Undetected is the
      most common real finding.

## People and process

- [ ] Run realistic, authorised phishing simulations that teach, not punish.
- [ ] Measure the reporting rate, not just the click rate.
- [ ] Reduce your public attack surface: audit what search engines and
      certificate logs reveal about you.
- [ ] Have an incident process ready before you need it.

## The one-line summary

Do not trust input, do not trust the network, encrypt everything, grant the
least access that works, patch what you run, and watch what happens. Almost every
attack in this repository is stopped by some item on that list.
