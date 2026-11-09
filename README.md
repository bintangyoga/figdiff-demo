# figdiff-demo

A live demo of the [figdiff](https://github.com/bintangyoga/figdiff) GitHub Action.

`design/app.figcraft` is a tiny FigCraft file. The open pull request changes it (a new button color and width, a new link, a removed card). The **Design changes** comment on that pull request is what figdiff produces.

The file is synthetic, written to match the `.figcraft` format, so it can be inspected here but is not meant to be opened as a real design.

To try it yourself, copy `.github/workflows/figdiff.yml` into a repository that contains `.figcraft` files.

## What you should see

Open [pull request #1](https://github.com/bintangyoga/figdiff-demo/pull/1). A single comment titled **Design changes** lists, per frame:

- the sign-in button's color and width,
- the title text,
- the new "Forgot password" link,
- the removed card on the Home screen.

Push another commit to the branch and the same comment is updated instead of a new one being added. The full HTML report is attached to the workflow run as the `figdiff-reports` artifact.

Before/after images are optional and experimental (`images: true` in the workflow), and appear in that report, not in the comment.
