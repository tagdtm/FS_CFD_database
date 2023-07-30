# FS_CFD_database
## General
このデータベースは学生フォーミュラの空力開発に勤しむ方々に少しでも役に立てばと思って制作したものです。
CFDの正当性を評価することは時間や資源の観点からも容易ではありません。
設計のみでなく制作までを学生自らが行う学生フォーミュラのような競技においては尚のこと難しく、CFDの結果がどれぐらい正しいのかという評価をする機会はそう多くないのではないでしょうか。
そこで今回、ストレート、10m/s、車半分の条件において30万メッシュから7000万メッシュまでのシミュレーションを実施しました。

## How to use this?
想定している活用方法は以下の通りですが、好きにデータを扱っていただいて構いません。
1. 公開されているCADデータから自分でCFDを回し、7000万メッシュなどのデータと比較する。
2. ただただデータを眺める

## Limitation of this data
7000万セルでも完全に正しいデータが得られているわけではありません。
詳細な評価をするには風洞との結果比較が重要な上に、K-Omega SSTモデルも剥離部の数値粘性などに修正を加えていないので剥離部分の予測は実際と比較して大きく広がっているものと推測されます。
7000万セルのシミュレーションをお手本データ、としてプレゼンテーションに記載しましたが、これはあくまで最も確からしいという意味であり、この結果が正しいことは担保できていません。
あくまで比較用として使用していただけると幸いです。

## Google Driveへのリンク
GitHubを使いこなせない僕に、大量のファイルをUIを通してGitHubに張り付けていく作業は非常に骨が折れる作業でした。なので以下Google Driveにデータを公開することにします。
- CpTのスライスの写真、およびSurface Plotの生データ: 
https://drive.google.com/drive/folders/1mf5Cxq2XfC3gGprzztVWZNoMcPCSArbq?usp=sharing
- Matlabで処理した数値的データ: 
https://drive.google.com/drive/folders/1vYF1jgxsOkcHK8NPQzyqU2smVBAyfWsw?usp=sharing
- Matlabコード、CpTコンター変換コード、デルタプロット生成コード: 
https://drive.google.com/drive/folders/1yoeuZD6_OnBSm2FAL_QEOhWRNrElsWxB?usp=sharing

# データベースの追加
追加データのリクエスト、および協力していただける方は以下のアドレスまでご連絡お願いします。

yt7u21@soton.ac.uk
