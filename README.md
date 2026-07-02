# USB CABLE CHECKER Lite 取扱説明書

## はじめに

USBケーブルチェッカー Lite はUSBケーブルの結線の確認、電源線抵抗値の測定などができるUSBケーブルテストツールです。

**USB Cable Checker Lite 公式ページ： http://bit-trade-one.co.jp/adusbcimle**

電源はCR2032コイン型電池を使用します。

様々なケーブルのチェックに対応しています。

- USB-A – Micro-B（USB 2.0）
- Type-C – Micro-B
- USB-A – Type-C（USB 3.x）
- Type-C – Type-C（USB 2.0 / USB 3.x / 全結線）

※ USB4・Thunderboltケーブルも物理結線の確認は可能ですが、規格の識別はできません


## 各部説明

<img src="images/image1.png" width="640">

<!-- ![description](images/image1.png) -->


## ご使用の前に・注意事項

購入時、USBCableChecker Liteには動作確認用の電池が取り付けられています。  

絶縁用のシールが本体との間に挟まっていますので、取り除いてから使用してください。

また、基板をアクリルで保護しておりますがコネクタ等がむき出しになっている為、取扱いにはご注意下さい。

**本製品はケーブル検査専用デバイスです。他のUSBデバイスを接続しないでください。破損の危険があります。**

電池交換の際は「電池の交換方法」をお読みいただき、正しい向きでセットしてください。（電池の＋面が上になるようにセットします。）


## 使用方法

- **ケーブルの判定**

本製品の電源をONにしてから、A側のコネクタとB側のコネクタをUSBケーブルで繋ぎます。

本製品のUSBポートにはA側、B側という区分があります。左からポートA側Type-Cポート 、A側 USB Aポート、B側 Type-Cポート、B側Micro-Bポートというポート配置になっています。
USBケーブルをテストする際は必ずA側ポートとB側ポートのコネクタを接続するようにしてください。

**正しい接続方法**

<img src="images/image2.png" width="480">

<!-- ![](images/image2.png) -->

<img src="images/image3.png" width="480">

<!-- ![](images/image3.png) -->

**誤った接続**

下図のようにA側同士、B側同士のポートを接続してもケーブルはテストされないのでご注意ください

<img src="images/image4.png" width="480">

<!-- ![](images/image4.png) -->

<img src="images/image5.png" width="480">

<!-- ![](images/image5.png) -->

ワイヤが結線されていれば「Wire Connection」の所に対応したLEDが点灯します。

A側とB側に繋いだケーブルのVBUSとGNDの**両方**が結線されていれば、「VBUS+GND Line resistance」にVBUS線とGND線抵抗値の**合計**の抵抗値の目安が、LEDで表示されます。

両端がType-Cのケーブルを接続すると、そのケーブルの最大給電能力を「USBPD Power capability」にLEDで表示します。


## ケーブルタイプ別LED表示例

**電源線のみのケーブル**

<img src="images/image6.png" width="480">

<!-- ![](images/image6.png) -->

**レガシー(Micro-B / USB A)USB 2.0ケーブル**

<img src="images/image7.png" width="480">

<!-- ![](images/image7.png) -->

**USB A - Type-C USB 3.xケーブル**

<img src="images/image8.png" width="480">

<!-- ![](images/image8.png) -->

**Type-C - Type-C USB2.0ケーブル**

<img src="images/image9.png" width="480">

<!-- ![](images/image9.png) -->

**Type-C - Type-C 全結線ケーブル**

<img src="images/image10.png" width="480">

<!-- ![](images/image10.png) -->


## ワイヤ結線表示部の解説

<img src="images/image17.png" width="640">

<!-- ![description](images/image17.png) -->

結線されているワイヤに対応したLEDが光ります。D-、D+以外の差動ペアワイヤのSBU,TX1,RX1,TX2,RX2はそれぞれ差動ペア単位で結線チェックされます、これらの差動ペアは+線と-線両方が導通である場合のみLEDが光ります。結線か否かの判定のしきい値は20kΩです。


### VBUS+GND Line resistance

本製品にはVBUS線とGND線が導通である場合、VBUS線とGND線の抵抗値を測定し、その合計値を表示する機能があります。単位は mΩ（ミリオーム）です。20kΩを超えた場合は断線と判断されます。

**電源線抵抗値の表示例と抵抗値の読み方**

<img src="images/image11.png" width="480">

<!-- ![](images/image11.png) -->

例：右から3つ目のLEDが点灯しているとき、目盛りの100と150の中間のLEDが点灯していることになるので、抵抗値は100-150mΩの間、と読みます。

### USB Power Delivery 給電能力表示部


<img src="images/image13.png" width="480">

<!-- ![](images/image13.png) -->

両端がType-CであるケーブルのUSBPD最大給電能力を表示します。プラグにeMarkerが搭載されている場合はeMarkerから読み取った情報により最大給電能力を自動的に判別します。100Wまたは240WのLEDが光る場合はeMarker搭載ケーブルとなります。

両端がType-CでないケーブルやCC線が未結線の場合はUSBPDの給電能力が無いケーブルですので、この部位のLEDは光りません。

**eMarkerとは？**

USB Type-Cケーブルのプラグ部分に搭載されたICチップで、ケーブルの仕様（最大電流、電圧、データ転送速度など）を記録しています。主に60Wを超える電力供給に対応するために必要になり、このデータを読み取ることで、ケーブルがどのような機能に対応しているかを判別できます。


### CC/Vconn 抵抗表示部


<img src="images/image12.png" width="480">

<!-- ![](images/image12.png) -->

Type-CプラグのCC端子もしくはVconn端子とGND間もしくはVBUS間の抵抗を検出した場合、その抵抗値を表示します。左側のLED２つはプルダウン抵抗、右側３つはプルアップ抵抗の存在を示します。

**CC/Vconn Pull-down resistor**
- **Sink/5.1k**：CCに5.1kΩのプルダウン抵抗が接続されています。この抵抗によってポートパートナー
にシンクポートであることが通知されます。
- **eMaker/1k**： Vconnに1kΩのプルダウン抵抗がされています、プラグ内部のeMarkerの存在を示し
ます

**CC Pull-up resistor (Source)**
- **56k/0.5A**： CCに56kΩのプルアップ抵抗が接続されています。ポートパートナーに通知される給電
能力は0.5Aです。（補足：USB Type-C規格では通常この抵抗値のプルアップ抵抗をプラグに実装すること
は認められていません。）
- **22k/1.5A**： CCに22kΩのプルアップ抵抗が接続されています。ポートパートナーに通知される給電
能力は1.5Aです。
- **10k/3A**： CCに10kΩのプルアップ抵抗が接続されています。ポートパートナーに通知される給電能
力は3.0Aです。



### Wire connection

<img src="images/image17.png" width="640">

<!-- ![description](images/image17.png) -->

ケーブル内で実際に結線されているワイヤを表示します。結線の判定しきい値は20kΩです。

- **VBUS, GND**：電源供給に使用されるワイヤです。
- **CC**：TypeCケーブルにおいて主にホスト、デバイスの識別やUSB PD通信に使用されるワイヤです。様々な機能を「使用できるかどうか」がこのワイヤを通してデバイス間でやり取りされます。  
- **SBU**：Side Band UseとしてUSBデータ通信以外のデータ（音声や映像等）をやり取りする際に使用するワイヤです。主にオルタネートモードで利用されます。  
- **USB2.0 D-/D+**：USB 2.0までのデータ通信（Low Speed, Full Speed, High Speed）で使用されるワイヤです。
- **SS Lane 1, SS Lane 2**：USB 3.0以上での通信（Super Speed, Super Speed+）に使用されるワイヤです。

SBU, SS Lane 1, SS Lane 2のLEDは差動ペア単位で結線チェックしています。+線と-線の両方が導通している場合にのみLEDが点灯します。



## 電池の交換方法

本製品のバッテリーはCR2032バッテリーを使用しています。スイッチを入れても電源がつかなくなっ
たり、電源LEDが点滅しはじめたら電池が消耗している状態ですので以下の手順でバッテリーを交
換してください。

① 本製品の電源をOFFにします \
② ドライバーを使って上面の４つのネジを回してフロントカバーを外します \
③ 爪などで下図電極タブを横にスライドさせます


<img src="images/image14.png" width="480">

<!-- ![battery swap 3](images/image14.png) -->

④ 電極タブをスライドさせた状態で電池を上に引き抜きます

<img src="images/image15.png" width="480">

<!-- ![battery swap 4](images/image15.png) -->

⑤ 新しいバッテリーを＋(プラス)面を上にして片側を電極タブの下に入れてから上から押し込んで
セットします

<img src="images/image16.png" width="480">

<!-- ![battery swap 5](images/image16.png) -->

⑥ 外したフロントカバーを取り付けます

上記画像のようにマイナス端子と電池の隙間にマイナスドライバーの先を滑り込ませるようにしてテコの原理を利用して外します。

その後、新しいCR2032バッテリーのプラス側を上にして装着します。


## USB Cable Checker 3 と Lite の比較

**USB Cable Checker 3** は、ケーブルとポートの両方のチェックに対応しています。チェック結果は液晶ディスプレイにテキストや数値で表示されます。ケーブル、USB充電器、タブレットやノートパソコンのポートなど、多彩な場面でのチェックにお役立ていただけます。

**USB Cable Checker Lite** は、ケーブルチェックに特化したシンプルな構成で、チェック結果はLEDで表示します。
ボタン電池一枚で動作し、軽量・薄型で携帯性に優れています。


| 機能 / 仕様 | USB Cable Checker 3 | USB Cable Checker Lite |
|---:|---|---|
| **―― ケーブルチェック ――** |  |  |
| ワイヤ導通・断線チェックVBUS, GND, CC, SBU, D+/D-, TX1/RX1, TX2/RX2 | ✓液晶ディスプレイに表示 | ✓LEDが点灯 |
| ケーブルタイプ自動判別 | ✓ | ✓LED点灯パターンで判別 |
| VBUS+GND抵抗値測定 | ✓数値で表示（mΩ） | ✓LED目盛りで目安表示（mΩ） |
| CC プルアップ/プルダウン抵抗値表示 | ✓実測値をLCDにテキストで表示（例: 56kΩプルアップ） | ✓専用LEDパネルで直接表示（Sink/5.1k, 56k/0.5A, 22k/1.5A, 10k/3A 等） |
| eMarker読み出し | ✓詳細データ表示 USB4 Gen3 / USB3.x / USB2等、最大電圧・電流 | ✓給電能力（60/100/240W）のみ表示 |
| **―― ポートチェック ――** |  |  |
| USBポートのPower role確認 | ✓Source / Sink / DRP | — |
| PDO取得・一覧表示 | ✓Fixed / PPS / EPR AVS 等 | — |
| EPR（240W）対応確認 | ✓ | — |
| Alternate Mode対応確認 | ✓DisplayPort / Thunderbolt | — |
| 充電モード解析（D+/D-） | ✓DCP / Apple divider / QuickCharge | — |
| Discover Identity レスポンス確認 | ✓ | — |
| **―― 操作・モード ――** |  |  |
| 動作モード | ケーブル / ポート / AUTO自動切替対応 | ケーブルチェックのみ |
| 自動パワーオフ | ✓3分無操作でOFF | — |
| 電池残量表示 | ✓種別選択で精度向上 | ✓電源LED点滅で警告 |
| **―― 対応コネクタ ――** |  |  |
| USB Type-C（A/B両側） | ✓ | ✓ |
| USB Type-A（A側） | ✓ | ✓ |
| Micro-B（B側） | ✓ | ✓ |
| **―― スペック ――** |  |  |
| 電源 | 単4電池 × 2アルカリ / マンガン / ニッケル水素 | CR2032コイン電池 |
| 本体サイズ | 約 70×40×22 mm | 約 76×52×15 mm |
| 重量（電池込） | 約 65 g | 約 40 g |
| 表示方式 | 1.77インチ LCD（テキスト・数値） | LED インジケーター |
