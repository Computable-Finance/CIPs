---
cip: 0
title: CIP Purpose and Guidelines
status: Drafted
author: CoFix Community
vote: https://snapshot.page/#/cofix/
discussion: https://github.com/Computable-Finance/CIPs/issues
created: 2020-11-12
updated: 2020-11-12
---

## What is an CIP?

CIP stands for CoFix Improvement Proposal, it has been adapted from the SIP (Synthetix Improvement Proposal). The purpose of this process is to ensure changes to CoFix are transparent and well governed. An CIP is a design document providing information to the CoFix community about a proposed change to the system. The author is responsible for building consensus within the community and documenting dissenting opinions.

## CIP Rationale

We intend CIPs to be the primary mechanisms for proposing new features, collecting community input on an issue, and for documenting the design decisions for changes to CoFix. Because they are maintained as text files in a versioned repository, their revision history is the historical record of the feature proposal.

It is highly recommended that a single CIP contain a single key proposal or new idea. The more focused the CIP, the more successful it is likely to be.

An CIP must meet certain minimum criteria. It must be a clear and complete description of the proposed enhancement. The enhancement must represent a net improvement.

## CIP Work Flow

Parties involved in the process are the *author*, the [*CIP editors*](#cip-editors), and the CoFix community.

:warning: Before you begin, vet your idea, this will save you time. Ask the CoFix community first if an idea is original to avoid wasting time on something that will be rejected based on prior research (searching the Internet does not always do the trick). It also helps to make sure the idea is applicable to the entire community and not just the author. Just because an idea sounds good to the author does not mean it will have the intend effect. The appropriate public forum to gauge interest around your CIP is [the unofficial CoFix Discord] or [the unofficial CoFix Telegram].

Your role as the champion is to write the CIP using the style and format described below, shepherd the discussions in the appropriate forums, and build community consensus around the idea. Following is the process that a successful CIP will move along:

```
Drafted -> Proposed -> Approved -> Implemented
         ^                     
         +----> Rejected       
         |         
         v
       Deferred
```

Each status change is requested by the CIP author and reviewed by the CIP editors. Use a pull request to update the status. Please include a link to where people should continue discussing your CIP. The CIP editors will process these requests as per the conditions below.

* **Drafted** -- Once the champion has asked the CoFix community whether an idea has any chance of support, they will write a draft CIP as a [pull request] and [github issue](https://github.com/Computable-Finance/CIPs). Consider including an implementation if this will aid people in studying the CIP.

* **Proposed** If agreeable, CIP editor will assign the CIP a number (generally the issue or PR number related to the CIP) and merge your pull request. The CIP editor will not unreasonably deny an CIP. Proposed CIPs will be discussed on [snapshots](https://snapshot.page/#/cofix). If there is a reasonable level of consensus around the change on the governance call the change will be moved to approved. If the change is contentious a vote of token holders may be held to resolve the issue or approval may be delayed until consensus is reached.

* **Approved** -- This CIP has passed community governance and is now being prioritised for development.

* **Implemented** -- This CIP has been implemented and deployed to mainnet.

* **Rejected** -- This CIP has failed to reach community consensus.

* **Deferred** -- This CIP is pending another CIP/some other change that should be bundled with it together.

## What belongs in a successful CIP?

Each CIP should have the following parts:

- Preamble - RFC 822 style headers containing metadata about the CIP, including the CIP number, a short descriptive title (limited to a maximum of 44 characters), and the author details.
- Simple Summary - “If you can’t explain it simply, you don’t understand it well enough.” Provide a simplified and layman-accessible explanation of the CIP.
- Abstract - a short (~200 word) description of the technical issue being addressed.
- Motivation (*optional) - The motivation is critical for CIPs that want to change CoFix. It should clearly explain why the existing specification is inadequate to address the problem that the CIP solves. CIP submissions without sufficient motivation may be rejected outright.
- Specification - The technical specification should describe the syntax and semantics of any new feature.
- Rationale - The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.
- Test Cases - Test cases may be added during the implementation phase but are required before implementation.
- Copyright Waiver - All CIPs must be in the public domain. See the bottom of this CIP for an example copyright waiver.

## CIP Formats and Templates

CIPs should be written in [markdown] format.
Image files should be included in a subdirectory of the `assets` folder for that CIP as follows: `assets/cip-X` (for cip **X**). When linking to an image in the CIP, use relative links such as `../assets/cip-X/image.png`.

## CIP Header Preamble

Each CIP must begin with an [RFC 822](https://www.ietf.org/rfc/rfc822.txt) style header preamble, preceded and followed by three hyphens (`---`). This header is also termed ["front matter" by Jekyll](https://jekyllrb.com/docs/front-matter/). The headers must appear in the following order. Headers marked with "*" are optional and are described below. All other headers are required.

` cip:` <CIP number> (this is determined by the CIP editor)

` title:` <CIP title>

` author:` <a list of the author's or authors' name(s) and/or username(s), or name(s) and email(s). Details are below.>

` vote:` <a url pointing to the voting at https://snapshot.page/#/cofix/>

` * discussion:` \<a url pointing to the official discussion thread at https://github.com/Computable-Finance/CIPs/issues \>

` status:` < Drafted | PROPOSED | APPROVED | IMPLEMENTED | Rejected | Defered >

` created:` <date created on>

` * updated:` <comma separated list of dates>

` * requires:` <CIP number(s)>

` * resolution:` \<a url pointing to the resolution of this CIP\>

Headers that permit lists must separate elements with commas.

Headers requiring dates will always do so in the format of ISO 8601 (yyyy-mm-dd).

#### `author` header

The `author` header optionally lists the names, email addresses or usernames of the authors/owners of the CIP. Those who prefer anonymity may use a username only, or a first name and a username. The format of the author header value must be:

> Random J. User &lt;address@dom.ain&gt;

or

> Random J. User (@username)

if the email address or GitHub username is included, and

> Random J. User

if the email address is not given.

#### `discussion` header

While an CIP is in Drafted or Proposed status, a `discussion` header will indicate the URL at [CoFix github](https://github.com/Computable-Finance/CIPs/issues) where the CIP is being discussed.

#### `vote` header

While an CIP is in Drafted or Proposed status, a `vote` header will indicate the URL at [CoFix snapshot](https://snapshot.page/#/cofix/) where the CIP is being voted.

#### `created` header

The `created` header records the date that the CIP was assigned a number. Both headers should be in yyyy-mm-dd format, e.g. 2001-08-14.

#### `updated` header

The `updated` header records the date(s) when the CIP was updated with "substantial" changes. This header is only valid for CIPs of Draft and Active status.

#### `requires` header

CIPs may have a `requires` header, indicating the CIP numbers that this CIP depends on.

## Auxiliary Files

CIPs may include auxiliary files such as diagrams. Such files must be named CIP-XXXX-Y.ext, where “XXXX” is the CIP number, “Y” is a serial number (starting at 1), and “ext” is replaced by the actual file extension (e.g. “png”).

## CIP Editors

The current CIP editors are:

` * Victor Zhang (@zhangzhongnan928)`

## CIP Editor Responsibilities

For each new CIP that comes in, an editor does the following:

- Read the CIP to check if it is ready: sound and complete. The ideas must make technical sense, even if they don't seem likely to get to final status.
- The title should accurately describe the content.
- Check the CIP for language (spelling, grammar, sentence structure, etc.), markup (Github flavored Markdown), code style

If the CIP isn't ready, the editor will send it back to the author for revision, with specific instructions.

Once the CIP is ready for the repository, the CIP editor will:

- Assign an CIP number (generally the PR number or, if preferred by the author, the Issue # if there was discussion in the Issues section of this repository about this CIP)

- Merge the corresponding pull request

- Send a message back to the CIP author with the next step.

The CIP editors monitor CIP changes, and correct any structure, grammar, spelling, or markup mistakes we see.

The editors don't pass judgment on CIPs. We merely do the administrative & editorial part.

## History

The CIP document was derived heavily from the SIP Synthetix Improvement Proposal document in many places text was simply copied and modified. Any comments about the CIP document should be directed to the CIP editors.

### Bibliography

[pull request]: https://github.com/Computable-Finance/CIPs/pulls
[markdown]: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
