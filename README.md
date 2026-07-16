# Marp Slides

外部画像を含めない、GitHub公開向けのMarpテンプレートとサンプル資料です。

## フォルダ構成

| フォルダ | 内容 |
| --- | --- |
| [`templates/`](templates/) | 37種類のスライドテンプレート、テンプレート一覧、PDF |
| [`sample-slides/`](sample-slides/) | GPT-5.6のモデル選び・Claude比較のサンプル、PDF |

## 収録物

| フォルダ | 種別 | Marpソース | PDF |
| --- | --- | --- | --- |
| `templates/` | 37種類のスライドテンプレート | `marp-master-template.md` | `marp-master-template.pdf` |
| `templates/` | テンプレート一覧 | `TEMPLATE-CATALOG.md` | - |
| `sample-slides/` | GPT-5.6 モデル選び | `model-guide.md` | `model-guide.pdf` |
| `sample-slides/` | GPT-5.6 / Claude 比較 | `model-comparison.md` | `model-comparison.pdf` |

## 使い方

1. `templates/marp-master-template.md` を複製する。
2. 必要なレイアウトだけを残し、見出し・本文・図のプレースホルダーを書き換える。
3. Marp CLIでPDFへ出力する。

```bash
npx @marp-team/marp-cli templates/marp-master-template.md --pdf
```

## 出典

GPT-5.6の内容は、[OpenAI Model guidance](https://developers.openai.com/api/docs/guides/latest-model) および資料内に記載した公式情報を参照しています。モデル提供範囲・料金・利用上限は更新されるため、利用時には公式情報を再確認してください。
