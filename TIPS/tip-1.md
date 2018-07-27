---
tip: 1
title: TIP Purpose and Guidelines
status: Active
type: Meta
author: trustfarm
        https://github.com/tao-foundation/TIPs/blob/master/TIPS/tip-1.md
created: 2017-7-27
---

## What is an TIP?

TIP stands for TAO Improvement Protocol Proposal. An TIP is a design document providing information to the TAO community, or describing a new feature for TAO or its processes or environment. The TIP should provide a concise technical specification of the feature and a rationale for the feature.

## TIP Rationale

We intend TIPs to be the primary mechanisms for proposing new features, for collecting community input on an issue, and for documenting the design decisions that have gone into TAO. Because the TIPs are maintained as text files in a versioned repository, their revision history is the historical record of the feature proposal.

For TAO implementers, TIPs are a convenient way to track the progress of their implementation. Ideally each implementation maintainer would list the TIPs that they have implemented. This will give end users a convenient way to know the current status of a given implementation or library.

## TIP Types

There are three types of TIP:

- A **Standard Track TIP** describes any change that affects most or all TAO implementations, such as a change to the the network protocol, a change in block or transaction validity rules, proposed application standards/conventions, or any change or addition that affects the interoperability of applications using Ethereum. Furthermore Standard TIPs can be broken down into the following categories. Standards Track TIPs consist of three parts, a design document, implementation, and finally if warranted an update to the [formal specification].
  - **Core** - improvements requiring a consensus fork, as well as changes that are not necessarily consensus critical but may be relevant to “core dev” discussions, and the miner/node strategy changes.
  - **Networking** - includes improvements around p2p network and [Light TAO TAM protocol], as well as proposed improvements to network protocol specifications of [TAM application machine], [EVM] and [swarm] .
  - **Interface** - includes improvements around client [API/RPC] specifications and standards, and also certain language-level standards like method names  and [contract ABIs]. The label “interface” aligns with the [interfaces repo] and discussion should primarily occur in that repository before an TIP is submitted to the TIPs repository.
  - **TRC** - application-level standards and conventions, including contract standards such as TAO token standards ([TRC20]), name registries , URI schemes , library/package formats , and wallet formats.
- An **Informational TIP** describes an TAO design issue, or provides general guidelines or information to the TAO community, but does not propose a new feature. Informational TIPs do not necessarily represent TAO community consensus or a recommendation, so users and implementers are free to ignore Informational TIPs or follow their advice.
- A **Meta TIP** describes a process surrounding TAO or proposes a change to (or an event in) a process. Process TIPs are like Standards Track TIPs but apply to areas other than the TAO protocol itself. They may propose an implementation, they often require community consensus; unlike Informational TIPs, they are more than recommendations, and users are typically not free to ignore them. Examples include procedures, guidelines, changes to the decision-making process, and changes to the tools or environment used in TAO development. Any meta-TIP is also considered a Process TIP.

It is highly recommended that a single TIP contain a single key proposal or new idea. The more focused the TIP, the more successful it tends to be. A change to one client doesn't require an TIP; a change that affects multiple clients, or defines a standard for multiple apps to use, does.

An TIP must meet certain minimum criteria. It must be a clear and complete description of the proposed enhancement. The enhancement must represent a net improvement. The proposed implementation, if applicable, must be solid and must not complicate the protocol unduly.

## TIP Work Flow

Parties involved in the process are you, the champion or *TIP author*, the [*TIP editors*](#tip-editors), and the [*TAO Core Developers*].

:warning: Before you begin, vet your idea, this will save you time. Ask the TAO community first if an idea is original to avoid wasting time on something that will be be rejected based on prior research (searching the Internet does not always do the trick). It also helps to make sure the idea is applicable to the entire community and not just the author. Just because an idea sounds good to the author does not mean it will work for most people in most areas where TAO is used. Examples of appropriate public forums to gauge interest around your TIP include [the TAO subreddit], [the Issues section of this repository], and [one of the TAO chat rooms and forums]. In particular, [the Issues section of this repository] is an excellent place to discuss your proposal with the community and start creating more formalized language around your TIP.

Your role as the champion is to write the TIP using the style and format described below, shepherd the discussions in the appropriate forums, and build community consensus around the idea. Following is the process that a successful TIP will move along:

```
[ WIP ] -> [ DRAFT ] -> [ LAST CALL ] -> [ ACCEPTED ] -> [ FINAL ]
```

Each status change is requested by the TIP author and reviewed by the TIP editors. Use a pull request to update the status. Please include a link to where people should continue discussing your TIP. The TIP editors will process these requests as per the conditions below.

* **Work in progress (WIP)** -- Once the champion has asked the TAO community whether an idea has any chance of support, they will write a draft TIP as a [pull request]. Consider including an implementation if this will aid people in studying the TIP.
  * :arrow_right: Draft -- If agreeable, TIP editor will assign the TIP a number (generally the issue or PR number related to the TIP) and merge your pull request. The TIP editor will not unreasonably deny an TIP.
  * :x: Draft -- Reasons for denying draft status include being too unfocused, too broad, duplication of effort, being technically unsound, not providing proper motivation or addressing backwards compatibility, or not in keeping with the [TAO philosophy]

* **Draft** -- Once the first draft has been merged, you may submit follow-up pull requests with further changes to your draft until such point as you believe the TIP to be mature and ready to proceed to the next status. An TIP in draft status must be implemented to be considered for promotion to the next status (ignore this requirement for core TIPs).
  * :arrow_right: Last Call -- If agreeable, the TIP editor will assign Last Call status and set a review end date, normally 14 days later.
  * :x: Last Call -- A request for Last Call status will be denied if material changes are still expected to be made to the draft. We hope that TIPs only enter Last Call once, so as to avoid unnecessary noise on the RSS feed. Last Call will be denied if the implementation is not complete and supported by the community.
* **Last Call** -- This TIP will listed prominently on the github and TAO Forum sites.
  * :x: -- A Last Call which results in material changes or substantial unaddressed complaints will cause the TIP to revert to Draft.
  * :arrow_right: Accepted (Core TIPs only) -- After the review end date, the TAO Core Developers will vote on whether to accept this change. If yes, the status will upgrade to Accepted.
  * :arrow_right: Final (Not core TIPs) -- A successful Last Call without material changes or unaddressed complaints will become Final.
* **Accepted (Core TIPs only)** -- This is being implemented by TAO Core Developers.
  * :arrow_right: Final -- Standards Track Core TIPs must be implemented in at least three viable TAO clients before it can be considered Final. When the implementation is complete and supported by the community, the status will be changed to “Final”.
* **Final** -- This TIP represents the current state-of-the-art. A Final TIP should only be updated to correct errata.
* **Archive** -- This TIP and A Final TIP should archive several places.

Other exceptional statuses include:

* Deferred -- This is for core TIPs that have been put off for a future hard fork.
* Rejected -- An TIP that is fundamentally broken and will not be implemented.
* Active -- This is similar to Final, but denotes an TIP which which may be updated without changing its TIP number.
* Superseded -- An TIP which was previously final but is no longer considered state-of-the-art. Another TIP will be in Final status and reference the Superseded TIP.

## What belongs in a successful TIP?

Each TIP should have the following parts:

- Preamble - RFC 822 style headers containing metadata about the TIP, including the TIP number, a short descriptive title (limited to a maximum of 44 characters), and the author details. See [below](https://github.com/tao-foundation/TIPs/blob/master/TIPs/tip-1.md#tip-header-preamble) for details.
- Simple Summary - “If you can’t explain it simply, you don’t understand it well enough.” Provide a simplified and layman-accessible explanation of the TIP.
- Abstract - a short (~200 word) description of the technical issue being addressed.
- Motivation (*optional) - The motivation is critical for TIPs that want to change the TAO protocol. It should clearly explain why the existing protocol specification is inadequate to address the problem that the TIP solves. TIP submissions without sufficient motivation may be rejected outright.
- Specification - The technical specification should describe the syntax and semantics of any new feature. The specification should be detailed enough to allow competing, interoperable implementations for any of the current TAO platforms (TEO rteo, TEOS, parity, ..) and others.
- Rationale - The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.
- Backwards Compatibility - All TIPs that introduce backwards incompatibilities must include a section describing these incompatibilities and their severity. The TIP must explain how the author proposes to deal with these incompatibilities. TIP submissions without a sufficient backwards compatibility treatise may be rejected outright.
- Test Cases - Test cases for an implementation are mandatory for TIPs that are affecting consensus changes. Other TIPs can choose to include links to test cases if applicable.
- Implementations - The implementations must be completed before any TIP is given status “Final”, but it need not be completed before the TIP is merged as draft. While there is merit to the approach of reaching consensus on the specification and rationale before writing code, the principle of “rough consensus and running code” is still useful when it comes to resolving many discussions of API details.
- Copyright Waiver - All TIPs must be in the public domain. See the bottom of this TIP for an example copyright waiver.

## TIP Formats and Templates

TIPs should be written in [markdown] format.
Image files should be included in a subdirectory of the `assets` folder for that TIP as follow: `assets/eip-X` (for eip **X**). When linking to an image in the TIP, use relative links such as `../assets/eip-X/image.png`.

## TIP Header Preamble

Each TIP must begin with an RFC 822 style header preamble, preceded and followed by three hyphens (`---`). The headers must appear in the following order. Headers marked with "*" are optional and are described below. All other headers are required.

` tip:` <TIP number> (this is determined by the TIP editor)

` title:` <TIP title>

` author:` <a list of the author's or authors' name(s) and/or username(s), or name(s) and email(s). Details are below.>

` * discussions-to:` <url>

` status:` <Draft | Last Call | Accepted | Final | Active | Deferred | Rejected | Superseded>

`* review-period-end: YYYY-MM-DD

` type: `<Standards Track (Core, Networking, Interface, ERC)  | Informational | Meta>

` * category:` <Core | Networking | Interface | ERC>

` created:` <date created on, in ISO 8601 (yyyy-mm-dd) format>

` * requires:` <TIP number(s)>

` * replaces:` <TIP number(s)>

` * superseded-by:` <TIP number(s)>

` * resolution:` <url>

#### Author header

The author header optionally lists the names, email addresses or usernames of the authors/owners of the TIP. Those who prefer anonymity may use a username only, or a first name and a username. The format of the author header value must be:

Random J. User &lt;address@dom.ain&gt;

or

Random J. User (@username)

if the email address or GitHub username is included, and

Random J. User

if the email address is not given.

Note: The resolution header is required for Standards Track TIPs only. It contains a URL that should point to an email message or other web resource where the pronouncement about the TIP is made.

While an TIP is a draft, a discussions-to header will indicate the mailing list or URL where the TIP is being discussed. As mentioned above, examples for places to discuss your TIP include [TAO topics on Forum](https://forum.tao.foundation), an issue in this repo or in a fork of this repo. No discussions-to header is necessary if the TIP is being discussed privately with the author.

The type header specifies the type of TIP: Standards Track, Meta, or Informational. If the track is Standards please include the subcategory (core, networking, interface, or TRC).

The category header specifies the TIP's category. This is required for standards-track TIPs only.

The created header records the date that the TIP was assigned a number. Both headers should be in yyyy-mm-dd format, e.g. 2001-08-14.

TIPs may have a requires header, indicating the TIP numbers that this TIP depends on.

TIPs may also have a superseded-by header indicating that an TIP has been rendered obsolete by a later document; the value is the number of the TIP that replaces the current document. The newer TIP must have a Replaces header containing the number of the TIP that it rendered obsolete.

Headers that permit lists must separate elements with commas.

## Auxiliary Files

TIPs may include auxiliary files such as diagrams. Such files must be named TIP-XXXX-Y.ext, where “XXXX” is the TIP number, “Y” is a serial number (starting at 1), and “ext” is replaced by the actual file extension (e.g. “png”).

## Transferring TIP Ownership

It occasionally becomes necessary to transfer ownership of TIPs to a new champion. In general, we'd like to retain the original author as a co-author of the transferred TIP, but that's really up to the original author. A good reason to transfer ownership is because the original author no longer has the time or interest in updating it or following through with the TIP process, or has fallen off the face of the 'net (i.e. is unreachable or isn't responding to email). A bad reason to transfer ownership is because you don't agree with the direction of the TIP. We try to build consensus around an TIP, but if that's not possible, you can always submit a competing TIP.

If you are interested in assuming ownership of an TIP, send a message asking to take over, addressed to both the original author and the TIP editor. If the original author doesn't respond to email in a timely manner, the TIP editor will make a unilateral decision (it's not like such decisions can't be reversed :)).

## TIP Editors

The current TIP editors are

` * trustfarm (@trustfarm)`

## TIP Editor Responsibilities

For each new TIP that comes in, an editor does the following:

- Read the TIP to check if it is ready: sound and complete. The ideas must make technical sense, even if they don't seem likely to get to final status.
- The title should accurately describe the content.
- Check the TIP for language (spelling, grammar, sentence structure, etc.), markup (Github flavored Markdown), code style

If the TIP isn't ready, the editor will send it back to the author for revision, with specific instructions.

Once the TIP is ready for the repository, the TIP editor will:

- Assign an TIP number (generally the PR number or, if preferred by the author, the Issue # if there was discussion in the Issues section of this repository about this TIP)

- Merge the corresponding pull request

- Send a message back to the TIP author with the next step.

Many TIPs are written and maintained by developers with write access to the TAO codebase. The TIP editors monitor TIP changes, and correct any structure, grammar, spelling, or markup mistakes we see.

The editors don't pass judgment on TIPs. We merely do the administrative & editorial part.

## History

This document was derived heavily from [Bitcoin's BIP-0001] written by Amir Taaki which in turn was derived from [Python's PEP-0001]. In many places text was simply copied and modified. Although the PEP-0001 text was written by Barry Warsaw, Jeremy Hylton, and David Goodger, they are not responsible for its use in the TAO Improvement Process, and should not be bothered with technical questions specific to TAO or the TIP. Please direct all comments to the TIP editors.

See [the revision history for further details](https://github.com/tao-foundation/TIPs/commits/master/TIPs/tip-1.md), which is also available by clicking on the History button in the top right of the TIP.

### Bibliography

[devp2p]: https://github.com/ethereum/wiki/wiki/%C3%90%CE%9EVp2p-Wire-Protocol
[Light Subprotocol]: https://github.com/ethereum/wiki/wiki/Light-client-protocol
[swarm]: https://github.com/ethereum/go-ethereum/pull/2959
[API/RPC]: https://github.com/ethereum/wiki/wiki/JSON-RPC
[contract ABIs]: https://github.com/ethereum/wiki/wiki/Ethereum-Contract-ABI
[interfaces repo]: https://github.com/ethereum/interfaces
[formal specification]: https://github.com/ethereum/yellowpaper
[markdown]: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
[Bitcoin's BIP-0001]: https://github.com/bitcoin/bips
[Python's PEP-0001]: https://www.python.org/dev/peps/

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
