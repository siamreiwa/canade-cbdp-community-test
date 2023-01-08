
## CANADEチェーンとは
Symbolブロックチェーンをベースとした弊社の独自チェーンです。
商品購入に使用できるポイント、トレーサビリティ、NFTなど事業に関わるコンソーシアムチェーンとしての運用を予定しております。

## CBDPとは
CBDPはこのCANADEチェーンで発行したポイントトークン（モザイク）となります。

## 本テストの目的
CANADEチェーンにおいて、以下の機能が問題なく動作するかを検証する。

- トランザクション
- アグリゲートトランザクション
- ハーベスティング
- ネームスペース・モザイクの発行
- ウォレット、エクスプローラなどの周辺ツール
- その他

## テストツール類

- [ウォレット](https://wallet.test.siamreiwa.com/)
- [フォーセット](https://faucet.test.siamreiwa.com/)
- [エクスプローラ](https://explorer.test.siamreiwa.com/)

※本テストでは、上記WEBウォレット以外のウォレットの提供はありません。
※ウォレットにはSymbolパブリックチェーンの既存のニーモニックフレーズをインポートせず新しいプロファイルを作成してください。
万が一、Symbolメインネットのフレーズ/秘密鍵をインポートして資産の流出等が発生した場合でも当社は一切の責任を負いかねます。

### 大量のCBDPが必要な方

Votingノードを立てる・意図的にハーベスティングの頻度を高めて検証したいなど、大量のCBDPが必要な方は下記フォームからご連絡ください。
[https://forms.gle/GfjEyTKq3DkQQ8ZL9](https://forms.gle/GfjEyTKq3DkQQ8ZL9)

※手動での対応となりますので送金までお時間を頂く場合があります。
※数に限りがありますのでご了承ください。また、検証後は速やかに下記アドレスまで返送をお願い致します。
TA4K2ZYFBGIW4YHRYVGCLNHIE3QQJSCEGQB6UWA

## テストの流れ
1. ウォレットのURLにアクセスし、新しいウォレットを作成します。
1. 上記フォーセットから、テスト用の通貨をお受け取りください。
1. 通貨が入金されましたらテストをお願い致します。

## 不具合・改善点のご連絡
本テストにおいて不具合や改善点がある場合、下記フォームよりご連絡をお願い致します。
[https://forms.gle/kZMxZcreXUaTSPo39](https://forms.gle/kZMxZcreXUaTSPo39)

## テスト参加の特典
今回のテストにご参加頂いた方には特典として後日CBDZを配布いたします。
※CBDZはCBDPとは異なり、Symbolブロックチェーン上のモザイクで発行されたものとなります。

### 特典の詳細
- 送金・アグリゲートトランザクション・ハーベスティングなど、種類を問わずなにか一つでもテスト頂けたら対象となります。
- お一人あたり200CBDZを配布予定です。（※複数アドレスを作成された場合でも特典は1回のみとさせていただきます。）
- 後日用意するGoogleフォームにTwitterIDと送付先のアドレスを入力して頂きます。


## CBDPのノードを建てる手順

CBDPテストネットのノードを建てて頂ける場合は下記の手順に沿って構築をお願い致します。
恐れ入りますがサーバー代などノード運用にかかる費用は参加者様にてご負担をお願い致します。

1. 通常のsymbolノードを運用できるスペックのサーバーを用意する
1. 	Node.js,docker,docker-composeなど、symbolノードを運用する際に必要なパッケージをインストールする
1. 下記コマンドにてノードの設定ファイルをサーバにダウンロードします。

	`wget https://raw.githubusercontent.com/siamreiwa/canade-cbdp-community-test/main/preset/custom-preset.tar.gz`
1. 圧縮ファイルを展開します。
	
	`tar -xvf custom-preset.tar.gz`

1. 必要に応じてSymbolノードと同じようにmy-preset.ymlファイルを編集します。(host, friendlyNameなど)
1. 以下のコマンドでノードを起動します。

   `symbol-bootstrap start -p custom-network-preset.yml -a dual -c custom-preset.yml -d`
     - symbol-bootstrapのバージョンは現在最新の1.1.9をインストールしてください。
