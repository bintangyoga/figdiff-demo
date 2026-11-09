# figdiff-demo

A live demo of the [figdiff](https://github.com/bintangyoga/figdiff) GitHub Action.

`design/ridgeline-onboarding.figcraft` is the Ridgeline onboarding example that ships with [FigCraft](https://github.com/storytold/figcraft) (MIT OR Apache-2.0). The open pull request edits it: the Get started button turns orange, the headline and a name change, and the account link is removed. The **Design changes** comment on that pull request is what figdiff produces.

To try it yourself, copy `.github/workflows/figdiff.yml` into a repository that contains `.figcraft` files.

## What you should see

Open [pull request #1](https://github.com/bintangyoga/figdiff-demo/pull/1). A single comment titled **Design changes** lists, per frame:

- the Get started button's color on the Welcome screen,
- the new headline,
- the removed "I already have an account" link,
- the changed name on the All set screen.

Push another commit to the branch and the same comment is updated instead of a new one being added. The full HTML report is attached to the workflow run as the `figdiff-reports` artifact.

Before/after images are optional and experimental (`images: true` in the workflow), and appear in that report, not in the comment.
