# figdiff-demo

A live demo of the [figdiff](https://github.com/bintangyoga/figdiff) GitHub Action.

`design/app.figcraft` is a tiny FigCraft file. The open pull request changes it (a new button color and width, a new link, a removed card). The **Design changes** comment on that pull request is what figdiff produces.

The file is synthetic, written to match the `.figcraft` format, so it can be inspected here but is not meant to be opened as a real design.

To try it yourself, copy `.github/workflows/figdiff.yml` into a repository that contains `.figcraft` files.
