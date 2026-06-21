# seeing-black

An interactive demonstration of the three-card problem (Bertrand's box): see a
black face and watch the chance its hidden side is also black settle onto
two-thirds — first by simulation, then by a counting proof.

Open [`index.html`](index.html) in any browser, or visit the GitHub Pages site.
Draw cards one at a time or in batches of a thousand; a live convergence chart
plots the running estimate of P(other side black | a black face is showing)
against the number of black faces seen, with the 2⁄3 target marked. Below the
simulation, a short "count the ways" argument and the matching line of Bayes'
rule show why the answer must be 2⁄3 — the experiment corroborates, the counting
proves.

## The problem

Three cards go in a bag: one black on both sides, one black/white, one white on
both. You draw at random and the face you see is black. What's the probability
the other side is black? The intuition says one-half; it is two-thirds. Of the
three equally likely black faces you could be looking at, two belong to the
black/black card — so its reverse, also black, wins two times out of three.

## Design

Built in the in-house **Tunnel** aesthetic (`tunnel-aesthetic`, from
[`cuddly-lamp`](https://github.com/nihilisticiconoclast/cuddly-lamp)): the locked
chart-paper palette and Fraunces / Public Sans / IBM Plex Mono type, hard edges,
no shadows or gradients. The single red `route` is spent on the primary **Draw**
control; amber lives only in the convergence chart (the page's one figure), where
the running-estimate line is teal and the 2⁄3 target is amber. The locked layer
and the signature generator are **linked from cuddly-lamp's CDN, never inlined**,
so a design-system update propagates here automatically. The fixed house mark
sits in the masthead with a per-page doodle in the margin.

No build step and no dependencies beyond the CDN-hosted Tunnel assets and the web
fonts.
