# App Store ASO Length Checker

A single-file, in-browser tool that checks App Store Connect metadata against Apple's character limits and flags wasted keyword space.

**Live:** https://fdarkaou.github.io/aso-length-checker/

## What it checks

| Field | Limit |
| --- | --- |
| App name | 30 |
| Subtitle | 30 |
| Keyword field | 100 |
| Promotional text | 170 |
| Description | 4,000 |

- Counts user-perceived characters (`Intl.Segmenter`), so emoji and accented letters count once.
- Warns about leading/trailing spaces, double spaces and unused characters.
- Keyword field: spaces after commas, duplicate keywords, and words already in the name or subtitle.
- **Clean up keywords** button removes those automatically.
- No build step, no dependencies, no network calls. Inputs stay in your browser's local storage.

The keyword tips are common ASO practice, not Apple rules. App Store Connect is the final authority on limits.

## Run locally

Open `index.html` in a browser, or:

```sh
python3 -m http.server
```

## Next step

When your metadata fits, see which searches your competitors rank for. [PeekPanda](https://peekpanda.com) keeps dated App Store evidence for iOS apps; see its [keyword gap docs](https://peekpanda.com/docs/keyword-gap).

## License

MIT
