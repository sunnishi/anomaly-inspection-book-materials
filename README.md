# AI外観検査本の実行教材

『不良画像が少なくても始められる AI外観検査 — Python・PatchCoreで学ぶ異常検知と判定基準』の読者向け教材です。著者：西城戸 亮。

## 教材をダウンロードする

**[教材ZIPをダウンロード（v1.0.0／約24 MB）](https://github.com/sunnishi/anomaly-inspection-book-materials/releases/download/v1.0.0/anomaly_inspection_materials_v1.0.0.zip)**

GitHubへのログインは不要です。`anomaly_inspection_materials_v1.0.0.zip` を保存し、展開してください。[リリース一覧](https://github.com/sunnishi/anomaly-inspection-book-materials/releases)から選ぶ場合も同じファイル名を使います。「Source code (zip)」は実行教材一式ではありません。

展開後の `code/README.md` に、環境作成・追試・自分の画像で試す手順があります。

## 入っているもの

- Pythonによる教材用の簡略PatchCoreと画素差分の比較コード
- 公開データVisA PCB1の実写50枚と公式マスク20枚、固定した分割表
- 本文に対応するスコア・判定・異常マップ・条件変化の保存済み結果
- 自分で用意した画像の分割準備と、フォルダー検査のスクリプト
- 19件のテストと、データ・コードの出典および利用条件

初回はPython3.10の仮想環境を作成し、`requirements.txt` の依存ライブラリを導入します。学習済みResNet18重み約45MBは `download_weights.py` が公式配布元から取得します。重み自体はZIPには含めていません。

## この教材で確認できる範囲

原論文やAnomalibと同一ではなく、ResNet18を使った仕組みの説明用実装です。主実験の評価は簡略PatchCoreがTP10／FN0／FP10／TN0、画素差分がTP4／FN6／FP2／TN8でした。全件NGを採用成功として扱わず、見逃しと過検出を調べる教材にしています。

50枚は便宜的な部分集合です。工場での精度を証明する試験ではありません。保存済み結果を上書きせず、追試には別の出力名を使ってください。Windows実機、カメラ・PLC・自動排出、生産ラインでの動作は未検証です。

## ファイルの確認

v1.0.0のSHA-256：

```text
2fe91641764598014925d826d28710bebddcad9b450bf52e00886aa71074d300
```

ZIP内部の `SHA256-MANIFEST.json` に各ファイルの照合値を収録しています。

## 利用条件と出典

独自コードはMIT Licenseです。公開データVisAの実写・公式マスクと加工画像はCC BY 4.0です。[データの出典・加工内容](DATA_ATTRIBUTION.md)とZIP内のライセンスを確認してください。重みと依存ライブラリにはそれぞれの利用条件があります。

本リポジトリのライセンス表示が、データや書籍本文の権利を置き換えることはありません。教材の利用はデータ提供者による本書・方式の推奨を意味しません。

問い合わせ・教材の不具合報告は、このリポジトリの[Issues](https://github.com/sunnishi/anomaly-inspection-book-materials/issues)へお願いします。画像を添える場合は、公開してよい画像だけを使用してください。
