---
title: "Keycards for a building nobody can renovate"
subtitle: "Building the admin and freeze authority libraries for Logos programs, RFP-001 and RFP-002"
description: "Two libraries give a Logos program an owner and an emergency brake, on a chain where nothing can be patched. How they were built, what the review caught, and what to check before you deploy on them."
image: /assets/keycards/card.jpg
hero: /assets/keycards/hero.jpg
hero_alt: "A keycard reader glowing blue on the frame of a frosted glass shop door, in an empty shopping mall corridor at night."
hero_credit: "Image generated with ChatGPT."
---

> Note: Points in this article are valid at the time of publication. If you're coming from the future... Hi, future! Take everything here with a grain of salt.

During a crypto event I got a Logos fanzine from someone I can now call a friend. I dropped it into a bag and didn't pay much attention to it. Some time passed and we met again, and talked properly this time. He told me to read the fanzine he gave me. I did, and it hooked me, though I didn't act on it. I had a steady job. Why rock the boat.

Then, my mom died, and I was looking at my own clock and the choices I'd made. Less than two months later I was on the EthBelgrade stage [telling my story](https://www.youtube.com/watch?v=waByT_FUTQo), telling the audience they don't need to ask for permission, and the target audience was me, all along. The ideas from that fanzine had been sitting in the back of my mind for years, and they all came out at once. Steady wasn't enough anymore. I joined the cypherpunk movement, and I didn't ask for permission.

Keycard pulled me in. The card in the title: a smartcard wallet where the key is made in the card and stays there. I wrote it a Python SDK, then a Nim one. Then Keycard Shell came out, a signing device built around the card, and I had an idea: an old phone could be the shell. [Keycard Pal](https://github.com/mmlado/keycard-pal/) was born.

I was looking for proof that my new freelancer life could work, by earning just a cent from something. Logos' λPrize opened with two Keycard-related entries, [LP-0009](https://github.com/logos-co/lambda-prize/blob/master/solutions/LP-0009.md) and [LP-0010](https://github.com/logos-co/lambda-prize/blob/master/solutions/LP-0010.md), which were right up my alley... and I snatched them! I tried to compete for other prizes too, and the tech drew me in. I sent in proposals for two of Logos' Requests for Proposals, RFP-001 and RFP-002, the admin and freeze authority. I knew these set a base that many programs on the Logos blockchain would build on.

I have been doing this long enough to see the bigger prize. Not two libraries. A system where anyone can write one without touching SPEL, the framework Logos programs are built with. That system is now part of SPEL, and [how to write a library](https://docs.logos.co/lez/extensions/build-a-spel-extension-library) is in the docs.

## The mall

Modern malls have card readers on their doors. Some doors open only for the owner's keycard, and the owner is whoever swiped first on opening day. There are doors, a store for example, that anyone's card opens, including the owner's. The owner can give their keycard to someone else, and they become the new owner of the building. The keycard can also be destroyed. Then those doors never open again and the mall is a public space without an owner. This is the first library, admin authority.

The builder can also install a lockdown system. Every door gets a lock by default, and the builder picks the ones that do not. Some doors don't need protection, and some must stay open, for example, the one in front of the lockdown release button. The owner can hire a security chief. The moment a visitor looks wrong, the chief can lock down every door that has the locking mechanism. Nobody gets in, not even the owner. The chief can also be picky and ban specific people instead of locking everything. A ban can be lifted, but the building never forgets. Nothing on this chain can be erased, so the name stays in the register with a line through it, for anyone to read. The security chief can leave, and let the owner pick a new chief. They can also stay on duty after the owner destroys their own keycard. That is on purpose. Somebody still has to watch the public floor. This is the second library, freeze authority.

Why give the mall an owner at all, and why let the owner walk away? Two things I want, and they pull against each other. As a user of a blockchain I want immutability. When I stake a token, I want all the information I need to make that decision, and I want the underlying mechanism to stay as it is. I don't want to join another Discord server, just to hear when something changes. As a dev I know a program is not finished on the first day. Nobody ships the final version on day one.

The owner is there for the program's early days, when it needs someone who can act fast, without a vote. Once a community forms around the project, the owner can let go, renounce, destroy their keycard, and leave the program to whatever rules the community runs it by. If the program doesn't have a mechanism to continue, the admin authority can transfer the rights to an account another program controls, a vote or a multisig with its own rules, instead of renouncing. If there is neither, no mechanism in the program and no hand-off, the values are final. That is the promise.

Freeze authority carries no such weight. It is a duty, not a promise, and whoever holds it can walk away whenever they want. When the cracks show, it is the last brake left. Pull it, the mall is locked. Nobody pulls it, the mall gets looted. Which doors get a lock is the builder's call.

The two libraries fill different roles, and their renounces are deliberately opposite. Admin renounce must be permanent, or the promise is worthless. Freeze renounce leaves the post empty, it does not seal it. A security post nobody can ever fill again is the emergency. As long as an owner still exists, the owner can seat a new chief at any time, even while the mall is locked down. That recovery runs through the owner, so it dies with the owner.

## When cracks appear

Immutable cuts both ways, and on the Logos blockchain it cuts harder. There's no renovation. Not by the owner, not by anyone. Renovation was never the owner's job.

On the Logos blockchain a fixed program is a new program with a new address. The crack stays where it was.

What happens next depends on two decisions, one made when the program was written and one made when the owner left. If the security post was kept, the chief pulls the lockdown, and nobody walks into it. If the builder marked the exit doors as ones that stay open during a lockdown, people leave with what they came in with and build a new mall next door, with a fixed wall. That is a migration, not a walk. Bring boxes. The new mall opens with no owner at all, and if it uses the same open initialize as the first one, whoever swipes the first keycard becomes the owner. I come back to that race, and how to close it, in the advice below.

If the exits are not there, then yes, everyone is stuck, and there is nobody to call. That is not a flaw the library can fix. It is the price of rules that cannot change under your feet. This is the bargain every one of us makes, every time.

One more thing, and this one bites. If the owner has already destroyed their keycard, nobody can hire a new chief, and a locked building with no chief stays locked. Locked, no chief, no owner. That is forever, and on the Logos blockchain forever means forever.

Which is why the owner's last decision is the one that matters. The security post can only be reassigned by the owner, so whoever holds it when the keycard is destroyed is the last chief the building will ever have. A community-run program should hand that post to the community itself, a program account it controls, not one person's keycard.

## The person on the list

Why would someone who just told you not to ask for permission build a door that locks people out? Because the lock is not part of the chain. A builder chooses to install one, and on this chain a mall that opens without locks stays without locks. And every ban is public, forever. That is one more reason to hand the security post to a community, and the best reason I know to think twice before you install the lock at all.

## How it was built

The mall is a program on the Logos blockchain. The city, the place for the programs, is the LEE (Logos Execution Environment). SPEL is the framework the builder uses to put up the mall. In LEE information is stored in accounts, and every account is owned by a program. If you worked with Solana this will be familiar. The program that pulls a library in, I call the consumer. A gate is what hangs on a door. In code it is a marker, an attribute you put on the module or on a function, and at build time the framework wires the library's check into whatever you marked. The build checks the wiring: that the marker is in the right place and that the accounts it names are the ones the library declares. Whether the check turns the right caller away, you only find out at runtime. The build can't tell you. The review section below is the proof.

The RFP came in three milestones. The hardest part fell between the second and the third. The plan was one program account per library, each with its own initialize. Then someone in the Discord suggested one account for all of the program's parameters. Simple to say, hard to do, because the data is plainly byte-serialized into the account. To read or write its own field, a library would have to know the layout of the whole account and leave the rest untouched. I did not go that far. What shipped is the plain version: every library declares the byte range it uses inside the shared account, and the build refuses two ranges that overlap. It shipped as one of two modes. A library can also get an account of its own, and the mall below uses that mode, which is why its call passes `admin_config` and `freeze_config` as two accounts. The whole-layout problem is still open. What I would like to see in LEE is TLV, tag, length, value, the layout Solana already uses for its token extensions. Find your tag, take your bytes, ignore the rest.

During implementation, [r4bbit](https://github.com/0x-r4bbit) hit a problem with the token program's mint authority and [wrote it up](https://gist.github.com/0x-r4bbit/ead1077de7b5ab6a5ed67b8b6a69f5bc). I read his notes with the admin library open. Same problem, sitting right there. The original design had the caller pass in the account of the new admin. But in LEE the caller is itself passed into the function as a parameter, and LEE rejects the same account appearing twice. So the most common case, a caller naming themselves as admin, was impossible as specified. The fix was simple: initialize now self-designates the caller as the authority. I tried three other shapes before this one. Why each one lost is in [ADR-0005](https://github.com/mmlado/spel-admin-authority/blob/main/docs/adr/0005-self-election-via-caller.md), the design note for that decision. I ran it end to end on a local node. The node rejected transfer-to-self with the exact duplicate-id error the whole decision rested on. And at acceptance the RFP asks for one thing here: the authority is set at initialization. Self-election sets it.

What surprised me was the framework itself. Everything a library does has to work in three places: the macro expansion, and the two IDL generators, which produce the interface description for callers and parse the plain source without expanding the macros. Three places, three ways to get it wrong. The same machinery is what amazes me. Rust's macros and Cargo's metadata carry the whole library system: a library declares in its manifest what it gates and what it injects, and the framework reads that at build time and generates the code into the consumer's binary. I expected to need a runtime or a change to the LEE. I needed neither.

Everything up to the next heading is code, simplified. It shows the libraries. It is not the rabbit hole.

<figure>
<a href="/assets/keycards/floorplan.png"><img src="/assets/keycards/floorplan.png" alt="Floor plan of the mall. Four doors: open and set_rent carry the owner's keycard reader, set_rent and shop carry the lockdown lock, open and leave are exempt from the lockdown."></a>
<figcaption>The mall as a floor plan. Four doors, and what hangs on each.</figcaption>
</figure>

Here is the mall, in code. Two lines in Cargo.toml bring the libraries in:

```toml
admin-authority = { git = "https://github.com/mmlado/spel-admin-authority.git", tag = "v0.1.2" }
freeze-authority = { git = "https://github.com/mmlado/spel-freeze-authority.git", tag = "v0.1.3" }
```

Two markers on the module install the keycard readers and the lockdown wiring. The owner's first swipe, the injected initialize, is not in the listing. The framework generates it. Every door is a function, and what you put on the door is what it checks:

```rust
#[lez_program]
#[admin_authority]  // the owner's keycard
#[freeze_authority] // the lockdown wiring
mod mall {
    // Opening day, after the owner's first swipe. Owner only, and exempt from
    // the lockdown because the lockdown system is installed right after.
    #[require_admin]
    #[freeze_exempt]
    #[instruction]
    pub fn open(config) { ... }

    // A door only the owner's keycard opens. Locks down with the rest.
    #[require_admin]
    #[instruction]
    pub fn set_rent(config, rent) { ... }

    // A door anyone's card opens. Locks down with the rest, and a
    // banned visitor is turned away here.
    #[instruction]
    pub fn shop(config) { ... }

    // The exit. The builder marked it to stay open during a lockdown.
    #[freeze_exempt]
    #[instruction]
    pub fn leave(config) { ... }
}
```

The framework adds the accounts each gate needs to every door, so a caller passes the keycard reader and the lockdown state along with the door's own accounts. A stranger at the owner's door:

```rust
let err = mall::set_rent(admin_config, stranger, freeze_config, freeze_account, config, 42);
assert!(matches!(err, Err(SpelError::Unauthorized { .. })));
```

The whole project, with the lockdown, the ban, and the destroyed keycard as tests, is at [spel-blog-mall](https://github.com/mmlado/spel-blog-mall).

## The review

The loop was simple. I wait, comments arrive, I fix. From the reviewers' side it was thorough. They pinned the exact commit and framework revision, ran the full test suite, compiled the sample programs, and replayed my committed command-line walkthrough until it matched byte for byte. Then they read what the crate promised and counted what it shipped. [Five of seven is not a passing grade.](https://github.com/mmlado/spel-freeze-authority/pull/1#pullrequestreview-4740339227) That review checked the deliverables against the RFP. It is not a security audit, and neither library has had one.

The finding that taught me the most was small on the page. The per-account freeze gate looked for the signer by the parameter's name. Name that parameter anything else in your program and the framework quietly injected a stand-in with the name it expected. The gate checked the stand-in. The real caller walked straight through. Everything compiled, the tests were green. Green is a mood, not a verdict. One line in a review: it blocks a frozen key, not a frozen principal. The fix reshaped how every gate finds the accounts, by the role and not by the name. [I added a self-test](https://github.com/mmlado/spel-freeze-authority/pull/1#pullrequestreview-4785969760) so the accounts a library declares it injects can never again drift from what the generated wiring accepts. It never reached a tagged release.

The bug had passed silently. Python has one rule about that, and the review made it the rule for the rest of the work: "[Errors should never pass silently. Unless explicitly silenced.](https://peps.python.org/pep-0020/)"

A big thank you to the Logos review team. Their testing and comments are all over these libraries. And to [danisharora099](https://github.com/danisharora099) separately, who stuck with it from the first milestone to the last and kept finding the next thing to fix.

## For the builders

The admin library is barely out of development and the lending protocol that won [RFP-008](https://github.com/logos-co/rfp/issues/141) already lists it as a dependency. That made me grin. It was the whole point. I built the libraries so nobody else would have to. One proposal in, and the bet already holds. And now I'm on the hook. The gates I wrote are permanent. If I got something wrong, their program carries it forever.

The advice below is what I owe for that, with a date on it. **If you read this a year from now, check it still holds.**

First, the race from the migration story. Logos deployment transactions carry only bytecode, no instructions, so deploy and initialize cannot be one transaction, and the chain records no deployer to check against. That much is the platform. The rest is a choice I made: the injected initialize is open, and whoever calls it first becomes the admin. Send it as your very next transaction. Before you tell anyone the address. Before you post on X. That narrows the window, it does not close it, and once the owner is set, it is set. The freeze library went the other way, its initialize requires the admin's signature, so the security post cannot be raced. If you want the closed version for admin today, do not use the injected initialize: call the library's bootstrap helper from your own initialize handler and assert the caller against an address you compile in.

Admin renounce is permanent. Anything behind an admin gate with no other way in is final. In a lending protocol that could be the rate model. You better be damn sure this is what you want before you destroy that keycard.

Have a test that calls each gated function as a stranger and expects a rejection, [the admin sample ships one to copy](https://github.com/mmlado/spel-admin-authority/blob/main/admin-authority-sample/src/main.rs). If the stranger gets in, you shipped a decoration.

Deploying is signing your name on a building nobody can renovate, so check that what you are about to sign is what you meant. Look at the generated IDL for every function and type, and run `cargo expand` to see the code after the framework has expanded it, because that is what you are actually signing. It was the most useful tool I had during development.

The rest of the rules, transfer, renounce, and which doors the lockdown skips, are in the docs for [admin authority](https://docs.logos.co/lez/extensions/admin-authority) and [freeze authority](https://docs.logos.co/lez/extensions/freeze-authority).

## After the contract

A program you deploy on these libraries today is never touched, and nothing I do later can reach it. New versions may need changes on your side. That is what the version number is for. This doesn't mean development has stopped. I have a pile of ideas for these two, written down as design notes between milestones, on my own clock. The contract ended at the last milestone. The work didn't. I'm not done with these two.

The code is MIT/Apache-2.0, on GitHub: [admin-authority](https://github.com/mmlado/spel-admin-authority) and [freeze-authority](https://github.com/mmlado/spel-freeze-authority). Open an issue. Complain, suggest, argue. If you want a first contribution that is small and matters, [here is one](https://github.com/mmlado/spel-freeze-authority/issues/13). The freeze library names the three admin instructions it leaves ungated as plain strings in its manifest, and nothing checks that they still match what the admin library ships. A single test closes that gap, and there is one of the same shape in the crate to copy from.

The framework side [landed upstream](https://github.com/logos-co/spel/pull/257) on 11 September. The libraries move to it with the next SPEL release, and then I go back to the issue list.

## Your turn

Cypherpunks don't need permission to build. But it helps when the ecosystem tells you what it needs and gives grants for building it, and Logos does both. The RFPs are listed at [github.com/logos-co/rfp](https://github.com/logos-co/rfp), and new ones are coming. Pick one where the requirements read like something you can build, and tell them how you would build it.

Things that I've learned the expensive way. Link everything: a merged PR beats a paragraph about the merged PR. Answer the reviewer's questions in the proposal, before the reviewer asks them. The proposal also holds your time commitment and price, and both count when they pick a winner.

If you'd rather start small, build a toy with the admin and freeze libraries. If the libraries get in your way, that's exactly the feedback I crave.

There is also the [λPrize](https://github.com/logos-co/lambda-prize) list, where prizes come in sizes and the small ones are a way into the ecosystem. That is the door I came through.

I was looking for proof that the freelancer life could work by earning a cent. It worked. The keycard readers are ready. Go build a mall. Your turn.
