# FS_CFD_database
## General
このデータベースは学生フォーミュラの空力開発に勤しむ方々に少しでも役に立てばと思って制作したものです。
CFDの正当性を評価することは時間や資源の観点からも容易ではありません。
設計のみでなく制作までを学生自らが行う学生フォーミュラのような競技においては尚のこと難しく、CFDの結果がどれぐらい正しいのかという評価をする機会はそう多くないのではないでしょうか。
そこで今回、ストレート、10, 15m/s、車半分の条件において30万メッシュから7000万メッシュまでのシミュレーションを実施しました。**このReadmeはあくまで玄関みたいなもので、データそのものは後述している通り、Google Driveに置いています。**

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
08/02/2025追記
情報に誤りはありませんが、70Mのケースに関してはさらにCFDのセッティングをブラッシュアップすることでより現実的なシミュレーションが回せることがここ１年間の勉強でわかりました。
今後結果が揃い次第データを更新する予定です。

## Google Drive
GitHubを使いこなせない僕に、大量のファイルをUIを通してGitHubに張り付けていく作業は非常に骨が折れる作業でした。なので以下Google Driveにデータを公開することにします。
- CpTのスライスの写真、およびSurface Plotの生データ: 

https://drive.google.com/drive/folders/1mf5Cxq2XfC3gGprzztVWZNoMcPCSArbq?usp=sharing
- Matlabで処理した数値的データ: 

https://drive.google.com/drive/folders/1vYF1jgxsOkcHK8NPQzyqU2smVBAyfWsw?usp=sharing
- Matlabコード、CpTコンター変換コード、デルタプロット生成コード:

https://drive.google.com/drive/folders/1yoeuZD6_OnBSm2FAL_QEOhWRNrElsWxB?usp=sharing
- プレゼンテーション：

https://docs.google.com/presentation/d/1yfOy6vDAZ8dyjhNIJWsjwiJqCvI9ZmI0/edit?usp=sharing&ouid=114974693398715275822&rtpof=true&sd=true

ダウンロード方法は以下の通り
![image](https://github.com/tagdtm/FS_CFD_database/assets/96266042/9cf2cd26-b17c-49d0-bc45-4f0f12558f31)

## Future Plan
- 流れ場に応じて局所的にメッシュの解像度を変化
- 渦粘性係数のモデルに用いられている係数の調整（流れ場の安定性向上目的）
- Segregated vs Coupled solver
- K-Omega SSTにTransition modelを用いた結果との比較
- DESとの結果比較

## Request and contribution
追加データのリクエスト、および協力していただける方は以下のアドレスまでご連絡お願いします。

yt7u21@soton.ac.uk
