# Protein Quantification Calculator

## 日本語

タンパク質定量用のシンプルなHTMLカリキュレーターです。

STD濃度とAbs値、サンプルのAbs値を貼り付けると、標準曲線を作成し、サンプル濃度を計算します。サンプル点はグラフ上に表示され、検量線範囲内・範囲外を視覚的に確認できます。

### 主な機能

- STD濃度とAbs値の貼り付け入力（1行＝1点。入力順に処理。反復は列方向に入力し、1列ならn=1、2列ならn=2）
- Sample Abs値の貼り付け入力（1行＝1サンプル。入力順に Sample 1, 2, … と命名。同一サンプルの反復は列方向に入力し、1列ならn=1、2列ならn=2）
- 標準曲線、傾き、切片、R²の自動計算
- サンプル濃度の算出
- 希釈倍率を反映した最終濃度の計算
- 必要タンパク量、total volume、サンプル数から調製量を計算
- サンプルごとのグラフ表示のオン・オフ（Plot列のチェック。計算や調製量には影響しません）
- 引き出し線が重ならないサンプルラベル表示
- 調製量テーブルのクリップボードコピー
- 入力データのJSONファイルへの書き出し（Export）と読み込み（Import）。STD・Sampleの入力欄に加え、Use・濃度・サンプル名・希釈倍率・Plot・調製条件の編集内容も復元されます
- 印刷対応（A4縦1枚。サンプル数に応じて自動で縮小。目安として28サンプルまで）

### 使い方

`index.html` をブラウザで開いて使用します。

### 免責事項

本アプリは研究・実験作業を補助するための簡易計算ツールです。計算結果の正確性、実験条件への適合性、および本アプリの使用によって生じたいかなる損害についても、作成者は責任を負いません。実際の使用前に、必ずユーザー自身で結果を確認してください。

---

## English

A simple standalone HTML calculator for protein quantification.

Paste standard concentrations, standard Abs values, and sample Abs values to generate a standard curve and calculate sample concentrations. Sample points are plotted on the graph, making it easy to see whether they fall within or outside the calibration range.

### Features

- Paste input for standard concentrations and Abs values (one row per STD point in input order; replicates go across columns: 1 column = n=1, 2 columns = n=2)
- Paste input for sample Abs values (one row per sample, named Sample 1, 2, ... in input order; replicates of a sample go across columns: 1 column = n=1, 2 columns = n=2)
- Automatic standard curve, slope, intercept, and R² calculation
- Sample concentration calculation
- Final concentration calculation with dilution factor
- Preparation volume calculation from required protein amount, total volume, and number of samples
- Per-sample toggle for showing points on the graph (Plot checkbox; calculations and preparation volumes are unaffected)
- Sample labels with non-overlapping leader lines
- Copy preparation table to clipboard
- Export all inputs to a JSON file and import them later; restores the paste fields plus table edits (Use, concentrations, sample names, dilutions, Plot) and preparation settings
- Print support (one A4 portrait page; scales down automatically with the number of samples, up to about 28 samples)

### Usage

Open `index.html` in a web browser.

### Disclaimer

This application is a simple calculation tool intended to support research and experimental workflows. The author assumes no responsibility for the accuracy of the results, suitability for specific experimental conditions, or any damage arising from the use of this application. Please verify all results independently before use.

---

Created with Codex & Claude | kamel
