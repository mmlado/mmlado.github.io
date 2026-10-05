---
layout: default
---

# Mladen Milankovic

mmlado - <span class="sc">walleteer</span>. Air-gapped wallets that do not phone home.
{: .tag}

Freelance engineer. Author of
[Keycard Pal](https://keycardpal.com), an air-gapped wallet for
Status Keycard, and of the [keycard-py](https://github.com/mmlado/keycard-py) and
[keycard-nim](https://github.com/mmlado/keycard-nim) SDKs. Contributed two instructions
to the Status Keycard JavaCard applet: GET CHALLENGE and an
[ECDH key-agreement instruction](https://github.com/keycard-tech/status-keycard/pull/127)
(both released in [applet 4.0](https://github.com/keycard-tech/status-keycard/releases/tag/4.0)). Delivered two Rust RFP libraries for Logos spel.

Independent, open to work in the privacy space.
{: .tag}

> I believe sovereignty begins the moment someone realizes: you don't have to
> accept the default.

## Writing

{% for post in site.posts -%}
- [{{ post.title }}]({{ post.url }}), {{ post.date | date: "%B %Y" }}
{% endfor %}

## Building on Logos

- [spel-admin-authority](https://github.com/mmlado/spel-admin-authority) -
  Admin Authority library for Logos spel
  ([RFP-001, won and delivered](https://github.com/logos-co/rfp/issues/46))
- [spel-freeze-authority](https://github.com/mmlado/spel-freeze-authority) -
  Freeze Authority library for Logos spel
  ([RFP-002, won and delivered](https://github.com/logos-co/rfp/issues/47))
- Built the [SPEL extension mechanism](https://github.com/logos-co/spel/pull/257),
  merged upstream into the [Logos spel](https://github.com/logos-co/spel) framework
- Two Logos Lambda Prizes:
  [Keycard NIP-46 Nostr signer](https://github.com/logos-co/lambda-prize/blob/master/solutions/LP-0009.md)
  ([repo](https://github.com/mmlado/nip46-keycard)) and
  [Shell dApp integration proof of concept](https://github.com/logos-co/lambda-prize/blob/master/solutions/LP-0010.md)
  ([live demo](https://shelldappprototype.vercel.app/))

## Talks

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
- [Writing (mmlado.eth)](https://paragraph.com/mmlado.eth)
- [Keycard Pal F-Droid repo](https://fdroid.keycardpal.com/repo/)
- Digital Self-Defense on YouTube:
  [Serbian](https://www.youtube.com/@DigitalnaSamoodbrana) /
  [Hungarian](https://www.youtube.com/@DigitalisOnvedelem)
