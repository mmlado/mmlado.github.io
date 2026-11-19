---
layout: default
---

# Mladen Milankovic

mmlado - <span class="sc">walleteer</span>. Air-gapped wallets that do not phone home.
{: .tag}

Freelance engineer. Author of
[Keycard Pal](https://keycardpal.com), an air-gapped wallet for
Status Keycard on Google Play, the App Store and F-Droid, and of the
[keycard-py](https://github.com/mmlado/keycard-py) and
[keycard-nim](https://github.com/mmlado/keycard-nim) SDKs. Contributed two instructions
to the Status Keycard JavaCard applet: GET CHALLENGE and an
[ECDH key-agreement instruction](https://github.com/keycard-tech/status-keycard/pull/127)
(both released in [applet 4.0](https://github.com/keycard-tech/status-keycard/releases/tag/4.0)).
Built the [hardware wallet QR signing](https://github.com/status-im/status-web/pull/1343)
in the Status wallet. Delivered two Rust RFP libraries for Logos spel.

Independent, open to work in the privacy space.
{: .tag}

> I believe sovereignty begins the moment someone realizes: you don't have to
> accept the default.

## Writing

{% for post in site.posts -%}
- [{{ post.title }}]({{ post.url }}), {{ post.date | date: "%B %Y" }}
{% endfor -%}
- Keycards for a Building Nobody Can Renovate, printed in the Logos zine
  [Local Area Network 02](https://logos.co/zines/lan-02) (p. 10), October 2026

## Building on Keycard

- [Keycard Pal](https://keycardpal.com) - air-gapped wallet, Android and iOS:
  [Google Play](https://play.google.com/store/apps/details?id=com.keycardpal),
  [App Store](https://apps.apple.com/us/app/keycard-pal/id6777478235),
  [F-Droid](https://f-droid.org/packages/com.keycardpal/) (reproducible builds);
  listed on [keycard.tech/wallets](https://keycard.tech/wallets)
- [ERC-4527 hardware wallet QR signing](https://github.com/status-im/status-web/pull/1343)
  for the Status wallet, merged upstream into
  [status-im/status-web](https://github.com/status-im/status-web), built on
  [qrkit](https://github.com/mmlado/qrkit)
- Three merged PRs in the [Status Keycard applet](https://github.com/keycard-tech/status-keycard):
  GET CHALLENGE, ECDH key agreement (both in applet 4.0) and a SELECT response fix
- [keycard-nostr-bunker](https://github.com/mmlado/keycard-nostr-bunker) - NIP-46 remote
  signer that keeps the Nostr key on the card
- SDKs: [keycard-py](https://github.com/mmlado/keycard-py), used by Keycard's own
  [firmware signing tool](https://github.com/keycard-tech/keycard-shell/blob/main/tools/keycardsign.py);
  [keycard-nim](https://github.com/mmlado/keycard-nim); merged PRs to
  [keycard-sdk](https://github.com/choppu/keycard-sdk) and
  [react-native-keycard](https://github.com/choppu/react-native-keycard)

## Building on Logos

- [spel-admin-authority](https://github.com/mmlado/spel-admin-authority) -
  Admin Authority library for Logos spel
  ([RFP-001, won and delivered](https://github.com/logos-co/rfp/issues/46))
- [spel-freeze-authority](https://github.com/mmlado/spel-freeze-authority) -
  Freeze Authority library for Logos spel
  ([RFP-002, won and delivered](https://github.com/logos-co/rfp/issues/47))
- Built the [SPEL extension mechanism](https://github.com/logos-co/spel/pull/257)
  and the [multi-signature witness exchange](https://github.com/logos-co/spel/pull/246),
  merged upstream into the [Logos spel](https://github.com/logos-co/spel) framework
- Wrote the [Extensions section](https://github.com/logos-co/logos-docs/pull/355)
  of the Logos docs
- Two Logos Lambda Prizes:
  [Keycard NIP-46 Nostr signer](https://github.com/logos-co/lambda-prize/blob/master/solutions/LP-0009.md)
  ([repo](https://github.com/mmlado/nip46-keycard)) and
  [Shell dApp integration proof of concept](https://github.com/logos-co/lambda-prize/blob/master/solutions/LP-0010.md)
  ([live demo](https://shelldappprototype.vercel.app/))

## Talks

### [Your Keys Never Leave the Card (Except Once): Hands-On Air-Gapped Signing](https://dark.events/speaker/mmlado/)

Dark Prague 2026, hands-on workshop in the Logos Attic - no recording
{: .novid}

### [Code Against the Machine: Cypherpunks, technoanarchists &amp; post-state futures](https://www.youtube.com/watch?v=waByT_FUTQo)

EthBelgrade 2025
{: .novid}

{% include video.html id="waByT_FUTQo" title="Code Against the Machine: Cypherpunks, technoanarchists and post-state futures - EthBelgrade 2025" %}

### [Dev Tooling track](https://2024.ethbelgrade.rs)

EthBelgrade 2024 - no recording (venue technical difficulties)
{: .novid}

### [Smart Contract Development with Vyper](https://youtu.be/BPAcZ5rnECI)

EthBelgrade 2023
{: .novid}

{% include video.html id="BPAcZ5rnECI" title="Smart Contract Development with Vyper - EthBelgrade 2023" %}

### [Tehnički aspekti blokčejna](https://youtu.be/hyF_n4d7gu4)

Serbian Academy of Sciences, 2022
{: .novid}

{% include video.html id="hyF_n4d7gu4" title="Tehnicki aspekti blokcejna - SANU 2022" %}
{% include video-script.html %}

## Elsewhere

- [GitHub](https://github.com/mmlado)
- [LinkedIn](https://www.linkedin.com/in/mladenmilankovic)
- [X](https://x.com/mmlado_eth)
- [Nostr](https://njump.me/npub1ccyxap7kpytvt2tdwcumflfll3yyk3hewvk5hmtv3zq7hrm2guesq2m2vl)
  `npub1ccyxap7kpytvt2tdwcumflfll3yyk3hewvk5hmtv3zq7hrm2guesq2m2vl`,
  verified as `mmlado.com`; the key lives on a Keycard
- [Older posts (Paragraph)](https://paragraph.com/mmlado.eth)
- Digital Self-Defense on YouTube:
  [Serbian](https://www.youtube.com/@DigitalnaSamoodbrana) /
  [Hungarian](https://www.youtube.com/@DigitalisOnvedelem)
