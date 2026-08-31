# Web Tools

複数の静的Webツールをまとめて公開するためのリポジトリです。

## 構成

```
web-tools/
├── index.html                                # 目次ページ (各ツールの起動リンク＋ソースリンク)
└── tools/
    ├── protein-quantification-calculator/
    │   └── index.html                        # 各ツール本体 (静的HTML/CSS/JSのみ)
    ├── aav-titer-calculator/
    │   └── index.html
    └── reagent-cal/
        └── index.html
```

## 新しいツールを追加する

1. `tools/<tool-name>/` フォルダを作り、そこにHTML/CSS/JSを置く（`index.html` をエントリポイントにする）
2. ルートの `index.html` の `<ul class="tools">` に `<li>` を1つ追加する
   - 起動リンク: `tools/<tool-name>/`
   - ソースリンク: `https://github.com/kameluke/web-tools/tree/main/tools/<tool-name>`

## GitHub Pagesで公開する

1. GitHubに `web-tools` という名前でリポジトリを作成し、このディレクトリの中身をpushする
2. リポジトリの Settings → Pages で、Source を `Deploy from a branch`、Branch を `main` / `/(root)` に設定する
3. 数分後に `https://kameluke.github.io/web-tools/` で公開される
