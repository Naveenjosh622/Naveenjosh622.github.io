
# Runtime Enhancement Proposals (REPs)

The Runtime Enhancement Proposals (REPs) for Intra-Chain Network encompass critical aspects, including core functionalities, networking, consensus mechanisms, and all enhancements related to ICN node and global state. As the ICN operates on the Substrate Framework, it employs a forkless upgrade approach, where the runtime is directly updated through a specialized extrinsic transaction. Governance participants have the authority to accept or reject proposed runtime upgrades, which are detailed here as formal proposals.

## REP Status Terms

[![](https://mermaid.ink/img/pako:eNplkk1vwjAMhv9KlMNOlI6y8VGkXYBJSBtDRdqF7OA2KY1okypJNyHU_z63HQLGJXIeO6-TNz7RRHNBQ5rm-ifJwDjyFjFlq3hvoMwI7KLlhmwduMp-zZjaGOHNIc-Z6tZP7QRTr1IBbhZGl0wJxa8E4t1C2qSyVmpFHsiqKHNRCIWCCBrFj1Ko1XztbbR1qCQEjyE5MLXGe3mRKLW3iTzJ_3Svq4nnvZDLgXPU4lvVf1ptxeUld5p3rc-1mMV0E806AzrQmDDrvOhA68cNaaxBQHu0EKYAydHyE1OEMOoyNITREEMO5sAoUzXWQeX09qgSGjpTiR6tSg5OLCSgr8UtXHLptKFhCrlFmGvgArcn6o5l87d7aR0qJlqlct_wyuSIM-dKG_p-k-7vpcuquJ_owreSN4OQfU9H_igYTSAYitF4CM_DIU_iwXSSBk-DlI8fBwHQuu5R0fZ_7wapnaf6FwczyqA?type=png)](https://mermaid.live/edit#pako:eNplkk1vwjAMhv9KlMNOlI6y8VGkXYBJSBtDRdqF7OA2KY1okypJNyHU_z63HQLGJXIeO6-TNz7RRHNBQ5rm-ifJwDjyFjFlq3hvoMwI7KLlhmwduMp-zZjaGOHNIc-Z6tZP7QRTr1IBbhZGl0wJxa8E4t1C2qSyVmpFHsiqKHNRCIWCCBrFj1Ko1XztbbR1qCQEjyE5MLXGe3mRKLW3iTzJ_3Svq4nnvZDLgXPU4lvVf1ptxeUld5p3rc-1mMV0E806AzrQmDDrvOhA68cNaaxBQHu0EKYAydHyE1OEMOoyNITREEMO5sAoUzXWQeX09qgSGjpTiR6tSg5OLCSgr8UtXHLptKFhCrlFmGvgArcn6o5l87d7aR0qJlqlct_wyuSIM-dKG_p-k-7vpcuquJ_owreSN4OQfU9H_igYTSAYitF4CM_DIU_iwXSSBk-DlI8fBwHQuu5R0fZ_7wapnaf6FwczyqA)

### Pre-Call
The "Pre-Call" status is self-assigned by the REP author when updating their REP to the REPs repository. Subsequently, the maintainers will review and assess its formatting suitability. Once they find it appropriate, the status will transition to "Call," initiating further review and awaiting votes.

When $a \ne 0$, there are two solutions to 
$ (ax^2 + bx + c = 0) $
and they are 
\\[ x = {-b \pm \sqrt{b^2-4ac} \over 2a} \\]

### Call
Upon acceptance of the new `rep-n.md` by the maintainers, the status will be updated to "Call." This phase entails a peer-review process by various voters and the general public. It precedes the REP going live for voting on potential amendments. The "Vote" status will only be updated from "Call" status once the author updates the runtime transaction hash, updates REP after base branch merge, and confirms it with maintainers.

### Vote
For the voting process, only one runtime upgrade transaction can be posted at a time, and it must adhere to the sequential order of REPs awaiting the "Call" status. Any other transaction carried out in parallel will not be synchronized with the REPs and open pull requests, leading to automatic rejection by the voters. It is not advisable to attempt such transactions, as they may incur unnecessary fees.

### Final
When the voting period concludes with a decision to accept the runtime upgrade, the node will execute a forkless upgrade. Subsequently, the maintainers will be authorized to change the REP's status to "Final."

### Drop
In the event of a vote against the runtime upgrade, the REP will be updated to "Drop," signaling that the upgrade will not proceed. In such cases, the author has the option to submit another REP with an updated proposal, potentially more likely to be accepted by the voters.

## Guidelines for Preparing a REP Submission

To streamline your Runtime Enhancement Proposal (REP) submission, follow these steps:

1. **Ideate and Discuss:** Create a forum post on OpenICN to introduce your proposal. Seek feedback and reviews, especially if you already have a research post.
2. **Refine Your Proposal:** Incorporate feedback from the community to enhance your proposal. Make adjustments as needed to improve your ideas, findings, or algorithms.
3. **Implement Changes:** Fork the ICN Node Repository and start implementing your enhancements.
4. **Stay Updated:** Regularly sync your fork with the main repository to keep your changes current.
5. **Document Thoroughly:** Clearly document each code modification with comprehensive comments. Ensure clarity to assist future contributors; unclear submissions may be declined.
6. **Draft Your REP:** Fork the REPs Repository and begin drafting your proposal using the provided template `rep-template.md`.
7. **Acquire REP ID**: To obtain your REP's ID, you can extract it from your ICN-Node-Repo's Pull Request URL slug (pull/id) or the Pull Request Title (#id). This ID corresponds to the REP number.
8. **Sequential PR Merging**: Understand that Pull Requests will be merged sequentially in order of their assigned IDs. Ensure that the base branch is updated with the PR's branch before merging.
9. **Update REP Details**: After opening a Pull Request, update the PR-ID in the front-matter/header and the REP's name. For example, `rep-1.md`.
10. **REP Status and Process**: Be aware of the different statuses and processes associated with a REP before its implementation PR can be merged into the main ICN repository.

## Exclusions from REP

It is important to note that REP is not intended for proposals pertaining to the application layer, specifically involving smart contracts. For matters related to application-layer enhancements, ICN offers a distinct proposal format known as Contract Interface Announcements (CIAs). This separate format is designed to facilitate the announcement of interface standards developed by individuals and for-profit organizations, proceeding to public-peer-review for their adoption. 

## Core Principles

Every REP should encompass and affirm these core principles: neutral stance, non-profit ethos, decision approval, and open source publication.

By submitting this REP, I affirm my commitment to the following core principles for ICN Node Runtime Upgrades & Proposals:

- [x] **Protocol Neutrality**: I ensured that this specific upgrade adheres to the principle of protocol neutrality by refraining from imposing specific rules and by upholding absolute freedom of choice for developers, validators, users, and organizations.

- [x] **Non-Profit Ethos**: I ensured the non-profit ethos of this upgrade, which ensures that profit decisions remain within the purview of independent smart contracts.

- [x] **Majority Decision**: I agree with the decision-making process outlined in this upgrade, which relies on the majority votes of contract owners or an approval committee for protocol amendments.

- [x] **Open Source**: I advocate for the commitment to keeping the source code open and accessible, as well as fostering open discussions within the inclusive ICN open forum.

## What to Include in a Successful REP

1. **Header**: 
2. **OpenICN Discussions**:
3. **Abstract**:
4. **Motivation**:
5. **Specification**:
6. **Backwards Compatibility**:
7. **Test Cases**:
8. **Security Considerations**:
9. **Video-Submission**:

## REP Template and Format Fit

The REP Template is available [here](rep-template.md) and is written in [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) format with Jekyll front-matter.

## Copyright

All Copyright and related rights should be waived via [CC0 LICENSE](LICENSE).

# Governance

All Governance-related information will be included in a separate REP proposal. Till its live, the REPs are manually amended by Auguth Tech.
