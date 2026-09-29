# Plasmid Dilution Calculator

## 日本語

qPCRの検量線（標準系列）に使うplasmidの希釈を計算するHTMLツールです。

plasmidの長さと濃度から1分子の質量を求め、テンプレート量あたり10^10 copies（変更可）になる希釈倍率を計算します。続けて10倍などの段階希釈の手順（元の液の量・DDWの量・残量・コピー数）を表にします。Numbers版「plasmid希釈ソフト Ver.4」をWeb化したものです。

### 使い方

1. **Plasmid** パネルに入力します。
   - Plasmid name、Date（メモ用。印刷とExportに残ります）
   - Insert length（bp）と Vector length（bp）。Full length = Insert length + Vector length です。
     - Vector はプリセット（pGEM-T Easy 3015 bp、pGEM-T 3000 bp、pCR2.1-TOPO 3931 bp、pCRII-TOPO 3973 bp）から選べます。
     - plasmid全体の長さが分かっている場合は、Insert length を 0 にして Vector length に全長を入れてください。
   - Plasmid concentration：濃度（ng/µL または µg/µL）
   - Max copy number：Tube ① をテンプレート量あたり何copiesにするか（10^x の指数。既定は 10^10）
   - Stock volume：Tube ① を作るときに取る原液の量（既定 1 µL）
   - Template volume for standard curve：検量線の qPCR 1 well に使うテンプレート量（µL）
2. **計算** パネルに途中の計算式と、Tube ① の調製量（原液 + DDW）が表示されます。
3. **Dilution series** の表に沿って希釈します。
   - ② 以降は Source（元の液）と DDW の量を自由に変更できます（既定は 10 µL + 90 µL の10倍希釈）。
   - 「Add tube」「Remove tube」で本数を変えられます。「All 10×」で 10 µL + 90 µL に戻します。
   - Remaining は、次の段に取った後に残る量です。足りない場合は赤字になります。
   - 「Copy」で表をタブ区切りでコピーし、Excel / Numbers に貼り付けられます。
4. 「Export」で入力内容をJSONファイルに保存し、「Import」で読み込めます。「Print」でA4 1枚に印刷できます。

### 計算式

```
分子量 (g/mol)        = Plasmid全長 (bp) × 330 × 2
1分子の質量 (g)       = 分子量 ÷ 6.022×10^23
10^10 copiesの質量 (pg) = 1分子の質量 × 10^10 × 10^12
原液濃度 (pg/µL)      = 濃度 (ng/µL) × 10^3   または 濃度 (µg/µL) × 10^6
① の希釈倍率          = 原液濃度 ÷ 10^10 copiesの質量 × テンプレート量
```

例：6,329 bp、2.33 µg/µL、Template 5 µL → 約168倍希釈（原液 1 µL + DDW 167 µL）で 10^10 copies / 5 µL。

### 免責事項

本アプリは研究・実験作業を補助するための簡易計算ツールです。計算結果の正確性、実験条件への適合性、および本アプリの使用によって生じたいかなる損害についても、作成者は責任を負いません。実際の使用前に、必ずユーザー自身で結果を確認してください。

---

## English

A simple HTML calculator for preparing a plasmid dilution series used as a qPCR standard curve.

It calculates the mass of one plasmid molecule from its length, then the dilution factor needed to reach 10^10 copies (adjustable) per template volume, followed by a serial dilution table (transfer volume, diluent volume, remaining volume, copy number). Web version of the Numbers spreadsheet "plasmid希釈ソフト Ver.4".

### Usage

1. Enter the plasmid information: plasmid name, date, insert length and vector length (presets available), concentration (ng/µL or µg/µL), template volume per well, top copy number (10^x per template) and the stock volume used for tube ①.
2. The calculation panel shows each step and how to prepare tube ① (stock + DDW).
3. Follow the dilution series table. From tube ② onward, transfer and diluent volumes are editable; add or remove tubes as needed. Remaining volumes turn red when there is not enough liquid for the next step. "Copy" copies the table as tab-separated text.
4. Export/Import saves and restores all inputs as a JSON file. Print fits on one A4 page.

Molecular weight is calculated as bp × 660 g/mol, with Avogadro's number 6.022×10^23.

### Disclaimer

This application is a simple calculation tool intended to support research and experimental workflows. The author assumes no responsibility for the accuracy of the results, suitability for specific experimental conditions, or any damage arising from the use of this application. Please verify all results independently before use.

---

Created with Claude | 2026/9/29 kamel
