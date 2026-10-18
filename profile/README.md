# MonDevHub

Open tools for the Mon language (ISO 639-3 `mnw`). Mon is listed as vulnerable in
UNESCO's Atlas of the World's Languages in Danger.

**Start here:** read printed Mon in the browser at [ocr.mondevhub.com](https://ocr.mondevhub.com).

## How the pieces fit

```
Mon text corpus ──▶ training (private) ──▶ model weights ──▶ SDKs ──▶ apps
                                                      language detector · tokenizer
```

| Piece | What it is | Where |
|---|---|---|
| Apps | Web app (live), Android and iOS (build from source), `monocr-cli` for PDFs and folders | [MonDevHub/monocr](https://github.com/MonDevHub/monocr) |
| SDKs | One SDK in four languages: `monocr-onnx` on PyPI, `monocr` on npm and crates.io, and a Go module | [MonDevHub/monocr-onnx](https://github.com/MonDevHub/monocr-onnx) |
| Model weights | What every SDK and app runs, with the evaluation and its limits | [janakhpon/monocr](https://huggingface.co/janakhpon/monocr) on Hugging Face |
| Corpus | Mon text for NLP and OCR training. Read its licence before reusing any shard | [MonDevHub/MonCorpusCollection](https://github.com/MonDevHub/MonCorpusCollection) |
| Language detector | Tells Mon, Burmese and English apart (`mon-language-detector` on PyPI) | [janakhpon/mon-language-detector](https://github.com/janakhpon/mon-language-detector) |
| Tokenizer | Unigram tokenizer for mixed Mon, Burmese and English text (`mon-tokenizer` on PyPI) | [Code-Yay-Mal/mon_tokenizer](https://github.com/Code-Yay-Mal/mon_tokenizer) |
| Reading list | Mon NLP resources | [MonDevHub/awesome-mon-nlp](https://github.com/MonDevHub/awesome-mon-nlp) |

## Four things called `monocr`

| You saw | It is |
|---|---|
| `MonDevHub/monocr` on GitHub | the apps above |
| `monocr` on npm or crates.io | the SDK, from `MonDevHub/monocr-onnx` (on PyPI it is `monocr-onnx`) |
| `monocr` on PyPI | a separate, Python-only package with its own line segmentation, from [janakhpon/monocr](https://github.com/janakhpon/monocr); its output need not match the apps line for line |
| `janakhpon/monocr` on Hugging Face | the model weights |

## Where things live

This organisation holds what you install or use. Some packages stay under the
accounts where they were first published, and moving them would break existing
installs. Training and research code is private.
