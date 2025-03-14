# FS_CFD_database
## General
このデータベースは学生フォーミュラの空力開発に勤しむ方々に少しでも役に立てばと思って制作したものです。
CFDの正当性を評価することは時間や資源の観点からも容易ではありません。
設計のみでなく制作までを学生自らが行う学生フォーミュラのような競技においては尚のこと難しく、CFDの結果がどれぐらい正しいのかという評価をする機会はそう多くないのではないでしょうか。
そこで今回、ストレート、10, 15m/s、車半分の条件において30万メッシュから7000万メッシュまでのシミュレーションを実施しました。
最も確からしい計算結果はK-Omega SST(a1 = 1, Realizablity coefficient=1.5, Coupled solver)で計算された結果で、70M-KOmegaにCpTのスライスとCp, CfのSurface plotをアップロードしてあります。
計算の詳細設定やデータの解析はAnalysisのフォルダの中にあるPDFを参照ください。
**その他のデータは後述している通り、Google Driveに置いています。**

## How to use this?
想定している活用方法は以下の通りですが、好きにデータを扱っていただいて構いません。
1. 公開されているCADデータから自分でCFDを回しデータを比較する。
2. 結果を眺める

## Limitation of this data
7000万セルでも完全に正しい結果が得られているわけではありません。
CFDの確かさの評価をするには風洞との結果比較が重要な上に、K-Omega SSTモデルも剥離部の渦粘性に修正などを加えていないので剥離部分の予測は実際と比較して大きく広がっていると推測されます。
7000万セルのシミュレーションをお手本データ、としてスライドに記載しましたが、これはあくまで最も確からしいという意味であり、この結果が正しいことは担保できていません。
あくまで比較用として使用していただけると幸いです。

## Important note
08/02/2025追記 (dd/mm/yyyy)
情報に誤りはありませんが、70Mのケースに関してはさらにCFDのセッティングをブラッシュアップすることでより現実的なシミュレーションが回せることがここ１年間の勉強でわかりました。
それにiteration 1500では十分に結果が収束しているとは言えず、ここで得た統計的な平均値には大きな誤差が含まれています。なので今後、シミュレーションをさらに回し、結果が揃い次第、解析結果をPDFにアップロードします。初期の状態でデータを比較された方もいると思うので、以下にUpdate logというセクションを設けました。GithubにあがっているCFDの生データが更新されるごとにこのセクションを書き換えていきます。

## Update log
08/02/2025 (dd/mm/yyyy)
- Analysisフォルダーを作成、元のスライドに加え、計算条件の詳細を記載したスライドをアップロード

- K-Omega SSTの結果をK-Omega SST (a1=1, Realizability coefficient = 1.5, coupled solver, 2500 itr)の結果に変更
- K-Epsilonの結果をK-Epsilon (coupled solver, 2500 itr)の結果に変更
![CzT_Cx](https://github.com/user-attachments/assets/c95ca8b5-c8eb-43dd-b4ab-760c03bbad90)

## Google Drive
GitHubを使いこなせない僕に、大量のファイルをUIを通してGitHubに張り付けていく作業は非常に骨が折れる作業でした。なので以下Google Driveにデータを公開することにします。
- CpTのスライスの写真、およびSurface Plotの生データ: 

https://drive.google.com/drive/folders/1mf5Cxq2XfC3gGprzztVWZNoMcPCSArbq?usp=sharing
- Matlabで処理した数値的データ: 

https://drive.google.com/drive/folders/1vYF1jgxsOkcHK8NPQzyqU2smVBAyfWsw?usp=sharing
- Matlabコード、CpTコンター変換コード、デルタプロット生成コード:

https://drive.google.com/drive/folders/1yoeuZD6_OnBSm2FAL_QEOhWRNrElsWxB?usp=sharing

ダウンロード方法は以下の通り
![image](https://github.com/tagdtm/FS_CFD_database/assets/96266042/9cf2cd26-b17c-49d0-bc45-4f0f12558f31)

## Future Plan
- 渦粘性係数のモデルに用いられている係数の調整（流れ場の安定性向上目的）(WIP)
- Segregated vs Coupled solver (WIP)
- - 流れ場に応じて局所的にメッシュの解像度を変化
- K-Omega SSTにTransition modelを用いた結果との比較
- DESとの結果比較

## Request and contribution
追加データのリクエスト、および協力していただける方は以下のアドレスまでご連絡お願いします。

yt7u21@soton.ac.uk
