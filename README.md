# GPT-5.6 Marp Slides (public edition)

ICOON MONOなどの外部画像を含めない、GitHub公開向けのMarpテンプレートとサンプル資料です。

## 収録物

| 種別 | Marpソース | PDF |
| --- | --- | --- |
| 37種類のスライドテンプレート | `marp-master-template-public.md` | `marp-master-template-public.pdf` |
| テンプレート一覧 | `TEMPLATE-CATALOG-public.md` | - |
| GPT-5.6 モデル選び | `gpt-5.6-model-guide-public.md` | `gpt-5.6-model-guide-public.pdf` |
| GPT-5.6 / Claude 比較 | `gpt56-claude-comparison-guide-public.md` | `gpt56-claude-comparison-guide-public.pdf` |

## 使い方

1. `marp-master-template-public.md` を複製する。
2. 必要なレイアウトだけを残し、見出し・本文・図のプレースホルダーを書き換える。
3. Marp CLIでPDFへ出力する。

```bash
npx @marp-team/marp-cli marp-master-template-public.md --pdf
```

## 公開時の扱い

このリポジトリの `*-public.*` ファイルは、外部のアイコン画像を参照しません。`assets/` と、ICOON MONO画像を含むローカル編集版はGitHubへコミットしない設定です。

## 出典

GPT-5.6の内容は、[OpenAI Model guidance](https://developers.openai.com/api/docs/guides/latest-model) および資料内に記載した公式情報を参照しています。モデル提供範囲・料金・利用上限は更新されるため、利用時には公式情報を再確認してください。
