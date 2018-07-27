# TIPs (TAO Improvement Protocol Proposals)
TAO Improvement Protocol Proposal (TIPs) and discussion Threads.

TIPs describe standards for the TAO Blockchain Architecture, including core protocol specifications, client APIs, and contract standards.

# Contributing

 1. Review [TIP-xx](TIPs/tip-xx.md).
 2. Fork the repository by clicking "Fork" in the top right.
 3. Add your TIP to your fork of the repository. There is a [template TIP here](tip-X.md).
 4. Submit a Pull Request to TAO's [TIPs repository](https://github.com/tao-foundation/TIPs).

Your first PR should be a first draft of the final TIP. It must meet the formatting criteria enforced by the build (largely, correct metadata in the header). An editor will manually review the first PR for a new TIP and assign it a number before merging it. Make sure you include a `discussions-to` header with the URL to a discussion forum or open GitHub issue where people can discuss the TIP as a whole.

If your TIP requires images, the image files should be included in a subdirectory of the `assets` folder for that TIP as follow: `assets/tip-X` (for tip **X**). When linking to an image in the TIP, use relative links such as `../assets/tip-X/image.png`.

Once your first PR is merged, we have a bot that helps out by automatically merging PRs to draft TIPs. For this to work, it has to be able to tell that you own the draft being edited. Make sure that the 'author' line of your TIP contains either your Github username or your email address inside <triangular brackets>. If you use your email address, that address must be the one publicly shown on [your GitHub profile](https://github.com/settings/profile).

When you believe your TIP is mature and ready to progress past the draft phase, you should do one of two things:

 - **For a Standards Track TIP of type Core**, ask to have your issue added to the agenda of an upcoming All Core Devs meeting, where it can be discussed for inclusion in a future hard fork. If implementers agree to include it, the TIP editors will update the state of your TIP to 'Accepted'.
 - **For all other TIPs**, open a PR changing the state of your TIP to 'Final'. An editor will review your draft and ask if anyone objects to its being finalised. If the editor decides there is no rough consensus - for instance, because contributors point out significant issues with the TIP - they may close the PR and request that you fix the issues in the draft before trying again.

# TIP Status Terms
* **Draft** - an TIP that is open for consideration.
* **Accepted** - an TIP that is planned for immediate adoption, i.e. expected to be included in the next hard fork (for Core/Consensus layer TIPs).
* **Final** - an TIP that has been adopted in a previous hard fork (for Core/Consensus layer TIPs).
* **Deferred** - an TIP that is not being considered for immediate adoption. May be reconsidered in the future for a subsequent hard fork.

