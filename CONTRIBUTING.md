# Contributing

Thank you for your interest in tensorOmics.

## What this repository is

This repository is the record of the case studies reported in the tensorOmics
manuscript. Its job is to let anyone follow how those analyses were run. For that reason,
once the paper is published **we will not merge changes that alter the analyses or their
results**, even improvements, because the published version must stay reproducible.

We will still fix broken links, typos and installation problems, and we may add notes
where a newer package version changes the output.

Case studies 1 and 3 report results produced with the development version of
`tensorOmics`, and their analysis chunks are not evaluated when the files are rendered.
Both will be updated to run against the released package once it is available.

## Where to raise things

- **A problem with a case study** (an error, a missing file or a result that does not
  match): please
  [open an issue](https://github.com/lecaolab/lecaolab-paper-tensorOmics/issues) here.
  Include your R version, your tensorOmics version and the output of `sessionInfo()`.
- **A bug or feature request in the tensorOmics package itself:** please open an issue in
  [brendanlu/tensorOmics](https://github.com/brendanlu/tensorOmics/issues), where the
  methods are maintained.

## Security

If you find a security problem, for example data that should not have been published,
please report it privately through this repository's **Security** tab rather than in a
public issue.

## Conduct

Everyone taking part is expected to follow our [Code of Conduct](CODE_OF_CONDUCT.md).
