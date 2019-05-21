---
bup: 1
title: BUP Process
author:
  - Christopher Hall <hsw+bup@bitmark.com>
status: active
type: process
date: 2019-04-08
license: CC0
...


# Abstract {#abstract}

A Bitmark Upgrade Proposal (BUP) is a design document providing
information to the Bitmark community, or describing a new feature for
Bitmark or its processes or environment. The BUP shall provide a
concise technical specification of the feature and a rationale for the
feature.

We intend BUPs to be the primary mechanism for proposing new features,
for collecting community input on an issue, and for documenting the
design decisions that have gone into the Bitmark Blockchain. The BUP
owner is responsible for building consensus within the community and
documenting dissenting opinions.

The BUPs are maintained as Markdown files in a versioned repository,
so that their revision history is preserved to document the progress
of the feature proposal.


# Copyright {#copyright}

This BUP is licensed under the Creative Commons CC0 1.0 Universal
license.


# BUP workflow {#bup-workflow}

The BUP process begins with a new idea for the Bitmark
Blockchain. Each potential BUP must have an owner -- someone who
writes the BUP using the style and format described below, shepherds
the discussions in the appropriate forums, and attempts to build
community consensus around the idea. The BUP owner (by default, the
Author) should first attempt to ascertain whether the idea is
BUP-able. Small enhancements or patches to a particular piece of
software often do not require standardisation between multiple
projects; these do not need a BUP and should be injected into the
relevant project-specific development workflow with a patch submission
to the applicable issue tracker. The first step should be to search
past discussions to see if an idea has been considered before, and if
so, what issues arose in its progression. After investigating past
work, the best way to proceed is by posting about the new idea to the
[Bitmark Blockchain Daemon](https://github.com/bitmark-inc/bitmarkd)
[development issue tracker](https://github.com/bitmark-inc/bitmarkd)

Vetting an idea publicly before going as far as writing a BUP is meant
to save both the potential owner and the wider community.  Asking
the Bitmark Blockchain community first if an idea is original helps
prevent too much time being spent on something that is guaranteed to
be rejected based on prior discussions (searching the internet does
not always do the trick). It also helps to make sure the idea is
applicable to the entire community and not just the owner. Just
because an idea sounds good to the owner does not mean it will work
for most people in most areas where the Bitmark Blockchain is used.

Once the owner has asked the the Bitmark Blockchain community as to
whether an idea has any chance of acceptance, a draft BUP should be
presented to the the Bitmark Blockchain development mailing list. This
gives the owner a chance to flesh out the draft BUP to make it
properly formatted, of high quality, and to address additional
concerns about the proposal. Following a discussion, the proposal
should be submitted to the [BUPs git
repository](https://github.com/bitmark-property-system/bups) as a pull
request. This draft must be written in BUP style as described below,
and named with an alias such as "bup-aliceblue-timelockedtransfer"
until the editor has assigned it a BUP number (owners MUST NOT
self-assign BUP numbers).

BUP owners are responsible for collecting community feedback on both
the initial idea and the BUP before submitting it for review. However,
wherever possible, long open-ended discussions on public mailing lists
should be avoided. Strategies to keep the discussions efficient
include: setting up a separate special interest group mailing list for
the topic, having the BUP owner accept private comments in the early
design phases, setting up a wiki page or git repository, etc. BUP
owners should use their discretion here.

It is highly recommended that a single BUP contain a single key
proposal or new idea. The more focused the BUP, the more successful it
tends to be. If in doubt, split your BUP into several well-focused
ones.

When the BUP draft is complete, the BUP editor will assign the BUP a
number, label it as Standards Track, Informational, or Process, and
merge the pull request to the BUPs git repository. The BUP editor will
not unreasonably reject a BUP. Reasons for rejecting BUPs include
duplication of effort, disregard for formatting rules, being too
unfocused or too broad, being technically unsound, not providing
proper motivation or addressing backwards compatibility, or not in
keeping with the Bitmark Blockchain philosophy. For a BUP to be
accepted it must meet certain minimum criteria. It must be a clear and
complete description of the proposed enhancement. The enhancement must
represent a net improvement. The proposed implementation, if
applicable, must be solid and must not complicate the protocol unduly.

The BUP owner may update the draft as necessary in the git repository.
Updates to drafts should also be submitted by the owner as pull
requests.


## Transferring BUP Ownership {#transferring-bup-ownership}

It occasionally becomes necessary to transfer ownership of BUPs to a
new owner. In general, we would like to retain the original author as
a co-author of the transferred BUP, but that is really up to the
original author. A good reason to transfer ownership is because the
original owner no longer has the time or interest in updating it or
following through with the BUP process, or has become unreachable or
does not respond to email. A bad reason to transfer ownership is
because you do not agree with the direction of the BUP. We try to
build consensus around a BUP, but if that is not possible, you can
always submit a competing BUP.

If you are interested in assuming ownership of a BUP, send a message
asking to take over, addressed to both the original author and the BUP
editor. If the original author does not respond to email in a timely
manner, the BUP editor will make a unilateral decision, however such
decisions can be reversed if necessary.


## BUP Editors {#bup-editors}

The current BUP editor can be contacted at [bupeditor@bitmark.com](mailto:bupeditor@bitmark.com).


## BUP Editor Responsibilities & Workflow {#bup-editor-responsibilities-workflow}

The BUP editor subscribes to the the Bitmark Blockchain development
issue tracker. Off-list BUP-related correspondence should be sent (or
CC'd) to [bupeditor@bitmark.com](mailto:bupeditor@bitmark.com)

For each new BUP that comes in an editor does the following:

-   Read the BUP to check if it is ready: sound and complete. The ideas
    must make technical sense, even if they do not seem likely to be
    accepted.
-   The title should accurately describe the content.
-   The BUP draft must have been sent to the the Bitmark Blockchain
    development mailing list for discussion.
-   Motivation and backward compatibility (when applicable) must be
    addressed.
-   The defined Layer header must be correctly assigned for the given
    specification.
-   Licensing terms must be acceptable for BUPs.

If the BUP is not ready, the editor will send it back to the author for
revision, with specific instructions.

Once the BUP is ready for the repository it should be submitted as a
"pull request" to the [BUPs git
repository](https://github.com/bitmark-property-system/bups) where it
may get further feedback.

The BUP editor will:

-   Assign a BUP number in the pull request.
-   Merge the pull request when it is ready.
-   List the BUP in [README.markdown](readme.markdown)

The BUP editors are intended to fulfil administrative and editorial
responsibilities. The BUP editors monitor BUP changes, and update BUP
headers as appropriate.


# BUP format and structure {#bup-format-and-structure}


## Specification {#specification}

BUPs shall be written in markdown format as described in the [Pandoc
manual page](https://pandoc.org/MANUAL).  Section headers must use the
[ATX-style header](https://pandoc.org/MANUAL#atx-style-headings)
notation.

Each BUP should have the following parts:

-   Preamble -- Headers containing metadata about the BUP ([see
    below](#bup-header-preamble)).
-   Abstract -- A short (\~200 word) description of the technical
    issue being addressed.
-   Copyright -- The BUP must be explicitly licensed under acceptable
    copyright terms ([see below](#acceptable-licenses)).
-   Specification -- The technical specification should describe the
    syntax and semantics of any new feature. The specification should
    be detailed enough to allow competing, interoperable
    implementations for any of the current the Bitmark Blockchain
    platforms.
-   Motivation -- The motivation is critical for BUPs that want to
    change the the Bitmark Blockchain protocol. It should clearly
    explain why the existing protocol is inadequate to address the
    problem that the BUP solves.
-   Rationale -- The rationale fleshes out the specification by
    describing what motivated the design and why particular design
    decisions were made. It should describe alternate designs that
    were considered and related work. The rationale should provide
    evidence of consensus within the community and discuss important
    objections or concerns raised during discussion.
-   Backwards compatibility -- All BUPs that introduce backwards
    incompatibilities must include a section describing these
    incompatibilities and their severity. The BUP must explain how the
    author proposes to deal with these incompatibilities.
-   Reference implementation -- The reference implementation must be
    completed before any BUP is given status "Final", but it need not
    be completed before the BUP is accepted. It is better to finish
    the specification and rationale first and reach consensus on it
    before writing code. The final implementation must include test
    code and documentation appropriate for the the Bitmark Blockchain
    protocol.


### BUP header preamble] {#bup-header-preamble}

Each BUP must begin with a YAML header preamble. The headers must
appear in the following order. Headers marked with "\*" are optional
and are described below. All other headers are required.

~~~
  bup: [ BUP number | "?" before being assigned ]
* layer: [ "Consensus (soft fork)" | " Consensus (hard fork)" | "Peer Services" |
           "API/RPC" | "Applications" ]
  title: [ BUP title; maximum 44 characters ]
  author: [ list of authors' real names and email addresses ]
* owner: [ real name and email address, if absent first author is the owner ]
* discussion: [ email address ]
* comments-summary: [ summary tone ]
  comments: [ list of links to wiki pages for comments ]
  status: [ "Draft" | "Active" | "Proposed" | "Deferred" | "Rejected" |
            "Withdrawn" | "Final" | "Replaced" | "Obsolete" ]
  type: [ "Standards Track" | "Informational" | "Process" ]
  date: [ date created in ISO 8601 format: (yyyy-mm-dd) ]
  license: [ abbreviation for approved license(s) ]
* code-license: [ abbreviation for code under different approved license(s) ]
* requires: [ BUP number(s) ]
* replaces: [ BUP number ]
* superseded-by: [ BUP number ]
~~~


#### Layer header {#layer-header}

The Layer header (only for Standards Track BUPs) documents which layer
of the Bitmark Blockchain the BUP applies to. The acceptable values
are:

Consensus (soft fork)

Involves modification of the consensus protocol such the compatibility
is retained with existing network nodes.

Consensus (hard fork)

A change which breaks backwards compatibility such that existing nodes
will no be able to validate the new chain.

Peer Services

Any changes to the underlying peer-to-peer networking protocols.

API/RPC

Any changes to the users accessible RPC channels such as addition,
modification or removal of an API.

Applications

Changes to associated applications such as command line tools or
mining programs. Payment services programs and proxies are also
included here.


#### Author header {#author-header}

The Author header lists the names and email addresses of all the
authors/owners of the BUP. The format of the Author header value must
be a YAML list specifying each author on a separate line preceded by a
"-". Additional authors can be appended to the list as necessary.

~~~
author:
  - user name one <one@domain.tld>
  - user name two <two@domain.tld>
~~~


#### Owner header {#owner-header}

The Owner header, if present, defines who is responsible for
coordinating actions related to the BUP. If absent the first (or only)
author is the owner. When an ownership transfer occurs just add or
modify the Owner header to reflect the current owner.


#### Discussion header {#discussion-header}

While a BUP is in private discussions (usually during the initial Draft
phase), a Discussion header will indicate the mailing list or URL where
the BUP is being discussed. No Discussion header is necessary if the BUP
is being discussed privately with the author.


#### Type header {#type-header}

The Type header specifies the type of BUP: Standards Track,
Informational, or Process.


#### Created header {#created-header}

The Created header records the date that the BUP was assigned a number,
while Post-History is used to record when new versions of the BUP are
posted to bitcoin mailing lists. Dates should be in yyyy-mm-dd format,
e.g. 2001-08-14. Post-History is permitted to be a link to a specific
thread in a mailing list archive.


#### Requires header {#requires-header}

BUPs may have a Requires header, indicating the BUP numbers that this
BUP depends on.


#### Superseded-By header {#superseded-by-header}

BUPs may also have a Superseded-By header indicating that a BUP has
been rendered obsolete by a later document; the value is the number of
the BUP that replaces the current document. The newer BUP must have a
Replaces header containing the number of the BUP that it rendered
obsolete.


### Auxiliary Files {#auxiliary-files}

BUPs may include auxiliary files such as diagrams. Auxiliary files
shall be included in a sub-directory for that BUP, that is
named bup-XXXX, where "XXXX" is the BUP number.


# BUP types {#bup-types}

There are three kinds of BUP:

-   A Standards Track BUP describes any change that affects most or all
    the Bitmark Blockchain implementations, such as a change to the
    network protocol, a change in block or transaction validity rules,
    or any change or addition that affects the interoperability of
    applications using the Bitmark Blockchain. Standards Track BUPs
    consist of two parts, a design document and a reference
    implementation.
-   An Informational BUP describes the Bitmark Blockchain design
    issue, or provides general guidelines or information to
    the Bitmark Blockchain community, but does not propose a new
    feature. Informational BUPs do not necessarily represent
    the Bitmark Blockchain community consensus or recommendations, so
    users and implementers are free to ignore Informational BUPs or
    follow their advice.
-   A Process BUP describes a process surrounding the Bitmark
    Blockchain, or proposes a change to (or an event in) a process.
    Process BUPs are like Standards Track BUPs but apply to areas other
    than the the Bitmark Blockchain protocol itself. They may propose an
    implementation, but not to the Bitmark Blockchain's code base; they
    often require community consensus; unlike Informational BUPs, they
    are more than recommendations, and users are typically not free to
    ignore them. Examples include procedures, guidelines, changes to the
    decision-making process, and changes to the tools or environment
    used in the Bitmark Blockchain development. Any meta-BUP is also
    considered a Process BUP.


# BUP status field {#bup-status-field}


## Specification {#specification-1}

The typical paths of the status of BUPs are as follows:

[process](bup-0001/process.png)

Owners of a BUP may decide on their own to change the status between
Draft, Deferred, or Withdrawn. The BUP editor may also change the status
to Deferred when no progress is being made on the BUP.

A BUP may only change status from Draft (or Rejected) to Proposed, when
the author deems it is complete, has a working implementation (where
applicable), and has community plans to progress it to the Final
status.

BUPs should be changed from Draft or Proposed status to Rejected
status, upon request by any person, if they have not made progress in
three years. Such a BUP may be changed to Draft status if the owner
provides revisions that meaningfully address public criticism of the
proposal, or to Proposed status if it meets the criteria required as
described in the previous paragraph.

A Proposed BUP may progress to Final only when specific criteria
reflecting real-world adoption has occurred. This is different for each
BUP depending on the nature of its proposed changes, which will be
expanded on below. Evaluation of this status change should be
objectively verifiable, and/or be discussed on the development mailing
list.

When a Final BUP is no longer relevant, its status may be changed to
Replaced or Obsolete (which is equivalent to Replaced). This change must
also be objectively verifiable and/or discussed.

A process BUP may change status from Draft to Active when it achieves
rough consensus on the mailing list. Such a proposal is said to have
rough consensus if it has been open to discussion on the development
mailing list for at least one month, and no person maintains any
unaddressed substantiated objections to it. Addressed or obstructive
objections may be ignored/overruled by general agreement that they have
been sufficiently addressed, but clear reasoning must be given in such
circumstances.


### Progression to Final status {#progression-to-final-status}

A soft-fork BUP strictly requires a clear miner majority expressed by
blockchain voting (e.g. using BUP 9). In addition, if the economy seems
willing to make a "no confidence" hard-fork (such as a change in
proof-of-work algorithm), the soft-fork does not become Final for as
long as such a hard-fork might have majority support, or at most three
months. Soft-fork BUPs may also set additional requirements for their
adoption. Because of the possibility of changes to miner dynamics,
especially in light of delegated voting (mining pools), it is highly
recommended that a super-majority vote around 95% be required by the BUP
itself, unless rationale is given for a lower threshold.

A hard-fork BUP requires adoption from the entire
Bitmark Blockchain economy, particularly including those selling
desirable goods and services in exchange for bitcoin payments, as well
as the Bitmark Blockchain holders who wish to spend or would spend their
bitcoins (including selling for other currencies) differently in the
event of such a hard-fork. Adoption must be expressed by de facto usage
of the hard-fork in practice (i.e. not merely expressing public support,
although that is a good step to establish agreement before adoption of
the BUP). This economic adoption cannot be established merely by a
super-majority, except by literally forcing the minority to accept the
hard-fork (whether this is viable or not is outside the scope of this
document).

Peer services BUPs should be observed to be adopted by at least 1% of
public listening nodes for one month.

API/RPC and application layer BUPs must be implemented by at least two
independent and compatible software applications.

Software authors are encouraged to publish summaries of what BUPs their
software supports to aid in verification of status changes. Good
examples of this at the time of writing this BUP, can be observed in
[the Bitmark Blockchain BUPs README
file](https://github.com/bitmark-property-system/bups/blob/master/README.markdown).

These criteria are considered objective ways to observe the de facto
adoption of the BUP, and are not to be used as reasons to oppose or
reject a BUP. Should a BUP become actually and unambiguously adopted
despite not meeting the criteria outlined here, it must be updated to
Final status.


## Rationale {#rationale}

Why is this necessary at all?

-   BUP 1 defines an ambiguous criteria for the Status field of BUPs,
    which is often a source of confusion. As a result, many BUPs with
    significant real-world use have been left as Draft or Proposed
    status longer than appropriate. By giving objective criteria to
    judge the progression of BUPs, this proposal aims to help keep the
    Status accurate and up-to-date.

What if a single participant wishes to block a hard-fork?

-   This BUP addresses only the progression of the BUP Status field,
    not the deployment of the hard-fork (or any other change)
    itself.
-   Regardless, one participant cannot operate in a vacuum: if they are
    indeed alone, they will soon find themselves no longer able to
    interoperate with the majority. If they are not connecting
    with the rest of the network, they cease to meet the criteria herein
    which enables their veto.

How can economic agreement veto a soft-fork?

-   The group of miners is determined by the consensus rules for the
    dynamic-membership multi-party signature (for the Bitmark
    Blockchain, the proof-of-work algorithm), which can be modified with
    a hard-fork. Thus, if the same conditions required to modify this
    group are met in opposition to a soft-fork, the miner majority
    supporting the soft-fork is effectively void because the economy can
    decide to replace them with another group of would-be miners who do
    not support the soft-fork.

What happens if the economy decides to hard-fork away from a
controversial soft-fork, more than three months later?

-   The controversial soft-fork, in this circumstance, changes from
    Final to Replaced status to reflect the nature of the hard-fork
    replacing the previous (final) soft-fork.

What is the ideal percentage of listening nodes needed to adopt peer
services proposals?

-   This is unknown, and set rather arbitrarily at this time. For a
    random selection of peers to have at least one other peer
    implementing the extension, 13% or more would be necessary, but
    nodes could continue to scan the network for such peers with perhaps
    some reasonable success. Furthermore, service bits exist to help
    identification upfront.

Why is it necessary for at least two software projects to
release an implementation of API/RPC and application layer BUPs, before
they become Final?

-   If there is only one implementation of a specification, there is no
    other program for which a standard interface is used with or
    needed.
-   Even if there are only two projects rather than more, some standard
    coordination between them exists.

What if a BUP is proposed that only makes sense for a single specific
project?

-   The BUP process exists for standardisation between independent
    projects. If something only affects one project, it should be done
    through that project's own internal processes, and never be
    proposed as a BUP in the first place.


# BUP comments {#bup-comments}


## Specification {#specification-2}

Each BUP should, in its preamble, link to a public wiki
page with a summary tone of the comments on that page. Reviewers
of the BUP who consider themselves qualified, should post their own
comments on this wiki page. The comments page should generally only be
used to post final comments for a completed BUP. If a BUP is not yet
completed, reviewers should instead post on the applicable development
mailing list thread to allow the BUP author(s) to address any concerns
or problems pointed out by the review.

Some BUPs receive exposure outside the development community prior to
completion, and other BUPs might not be completed at all. To avoid a
situation where critical BUP reviews may go unnoticed during this
period, reviewers may, at their option, still post their review on the
comments page, provided they first post it to the mailing list and plan
to later remove or revise it as applicable based on the completed
version. Such revisions should be made by editing the previous review
and updating the timestamp. Reviews made prior to the complete version
may be removed if they are no longer applicable and have not been
updated in a timely manner (e.g. within one month).

Pages must be named after the full BUP number (e.g. "BUP 0001") and
placed in the "Comments" namespace. For example, the link for BUP 1
will be
[https://github.com/bitmark-property-system/bups/wiki/Comments:BUP-0001]().

Comments posted to this wiki must use the following format:

~~~
   <Your opinion> -- <Your name>, <Date of posting, as YYYY-MM-DD>
~~~

BUPs may also choose to list a second forum for BUP comments, in
addition to the BUPs wiki. In this case, the second forum's URI should
be listed below the primary wiki's URI.

After some time, the BUP itself may be updated with a summary tone of
the comments. Summary tones may be chosen from the following, but this
BUP does not intend to cover all possible nuances and other summaries
may be used as needed:

-   No comments yet
-   Unanimously Recommended for implementation
-   Unanimously Discourage for implementation
-   Mostly Recommended for implementation, with some
    Discouragement
-   Mostly Discouraged for implementation, with some
    Recommendation

For example, the preamble to BUP 1 might be updated to include the
lines:

~~~
comments-summary: No comments yet
comments:
  - https://github.com/bitmark-property-system/bups/wiki/Comments:BUP-0001
  - https://some-other-wiki.org/BUP-1-Comments
~~~

These fields must follow the Discussion header defined in BUP 1 (if
that header is not present, it should follow the position where it would
be present; generally this is immediately above the Status
header).

To avoid doubt: comments and status are unrelated metrics to judge a
BUP, and neither should be directly influencing the other.


## Rationale {#rationale-1}

What is the purpose of BUP comments?

-   Owing to the low barrier of entry for submission of new BUPs, it
    was deemed advisable to provide a mechanism for reviewers to express
    their opinions in a way that is readily accessible to the
    public without needing to review the entire development
    discussion.

Will BUP comments be censored or limited to particular participants or
experts?

-   Participants should freely refrain from commenting outside of their
    area of knowledge or expertise. However, comments should not be
    censored, and participation should be open to the public.


# BUP licensing {#bup-licensing}


## Specification {#specification-3}

New BUPs may be accepted with the following licenses. Each new BUP must
identify at least one acceptable license in its preamble. The License
header in the preamble must be placed after the Created header. Each
license must be referenced by their respective abbreviation given
below.

For example, a preamble might include the following License
header:

~~~
license: CC0-1.0
~~~

If the BUP contains source code then the Code License header must be
present and match the license use by the project the code applies
to.

~~~
code-license: ISC
~~~

BUPs are not required to be exclusively licensed under
approved terms, and may also be licensed under unacceptable licenses
in addition to at least one acceptable license. In this
case, only the acceptable license(s) shall be listed in the License and
Code License headers.


### Acceptable licenses {#acceptable-licenses}

-   BSD-2-Clause: [OSI-approved BSD 2-clause
    license](https://opensource.org/licenses/BSD-2-Clause)
-   CC0-1.0: [Creative Commons CC0 1.0
    Universal](https://creativecommons.org/publicdomain/zero/1.0/)
-   ISC: [Internet Systems Consortium
    License](https://opensource.org/licenses/ISC)

In addition, it is required that literal code included in the BUP be
licensed under the same license terms as the project it modifies. For
example, literal code intended for the Bitmark Blockchain Daemon would
be licensed under the ISC license terms.


### Not acceptable licenses {#not-acceptable-licenses}

All licenses not explicitly included in the above lists are not
acceptable terms for a the Bitmark Blockchain Improvement Proposal
unless a later BUP extends this one to add them.


## Rationale {#rationale-2}

Why is Public Domain not acceptable for new BUPs?

-   In some jurisdictions, public domain is not recognised as a
    legitimate legal action, leaving the BUP simply copyrighted with
    no redistribution or modification allowed at all.
-   CC0 is close to Public Domain and is a standard license.

Why is a specific software license specified?

-   Some BUPs, especially consensus layer, may include literal code in
    the BUP itself which may not be available under the exact license
    terms of the BUP.
-   Despite this, not all software licenses would be acceptable for
    content included in BUPs. This is the license the bitmarkd program
    uses.


# Acknowledgements {#acknowledgements}

This document was derived from the bitcoin BIP-0002. In many places
text was simply copied and modified. Although the BIP-002 text was
written by Amir Taaki, the BIP authors are not responsible for its use
in the Bitmark Blockchain Upgrade Proposal, and must not be bothered
with technical questions specific to Bitmark or the BUP
process. Please direct all comments directly to the BUP editors.


# See Also {#see-also}

-   [BIP 2: BIP Purpose and Guidelines](https://github.com/bitcoin/bips/blob/master/bip-0002.mediawiki)
-   [BUP 123: BIP Classification](https://github.com/bitcoin/bips/blob/master/bip-0123.mediawiki)
-   [RFC 7282: On Consensus and Humming in the IETF](https://tools.ietf.org/html/rfc7282)
-   [RFC 2119: Key words for use in RFCs to Indicate Requirement Levels](https://tools.ietf.org/html/rfc2119)
