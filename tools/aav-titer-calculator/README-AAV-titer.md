# AAV Titer Calculator

## 日本語

AAVベクターのqPCR/ddPCR結果からtiterを計算するためのシンプルなHTMLカリキュレーターです。

ExcelなどからCt/Cq結果を貼り付けると、標準系列から検量線を作成し、未知サンプルのコピー数およびtiterを計算します。NTCのCt値や検量線範囲外のサンプルも視覚的に確認できます。

### 主な機能

- qPCR結果の貼り付け入力
- STDのCq/Ct値とcopy numberから検量線を自動作成
- NTC Ctの表示
- 未知サンプルのcopy numberとtiter計算
- 希釈倍率の指定
- サンプルごとの平均titer計算
- lot、コメント、total volume、dish数の入力
- gc/dishの計算
- 表の印刷対応

### 使い方

`qpcr-calculator-standalone.html` をダウンロードしてブラウザで開いて使用するか、そのままWebで使ってください。

### 免責事項

本アプリは研究・実験作業を補助するための簡易計算ツールです。計算結果の正確性、実験条件への適合性、および本アプリの使用によって生じたいかなる損害についても、作成者は責任を負いません。実際の使用前に、必ずユーザー自身で結果を確認してください。

---

## English

A simple standalone HTML calculator for estimating AAV vector titer from qPCR/ddPCR results.

Paste Ct/Cq results from Excel or similar software to generate a standard curve from standard samples and calculate copy number and titer for unknown samples. NTC Ct values and out-of-range samples can be checked visually.

### Features

- Paste input for qPCR result tables
- Automatic standard curve generation from STD Cq/Ct values and copy number
- NTC Ct display
- Copy number and titer calculation for unknown samples
- Dilution factor selection
- Average titer calculation by sample
- Manual entry for lot, comments, total volume, and dish count
- gc/dish calculation
- Print support

### Usage

Download `qpcr-calculator-standalone.html` and open it in a web browser, or use it directly on the web.

### Disclaimer

This application is a simple calculation tool intended to support research and experimental workflows. The author assumes no responsibility for the accuracy of the results, suitability for specific experimental conditions, or any damage arising from the use of this application. Please verify all results independently before use.

---

Created with Codex | 2026/8/21 kamel
