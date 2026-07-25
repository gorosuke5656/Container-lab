自宅に導入したcontainerlabでのNW構築要領について説明します！<br>
（今回はAristaさんのコンテナイメージ(Arista CEOS）及びFRRを例を紹介します）<br>

## 内容<br>

### Containerlabとは？？<br>
Containerlabは、主要なネットワークコンテナをサポートしたネットワークラボツールです。<br>
 ※対応コンテナ：ARISTA cEOS, Juniper cRPD, Cisco XRd, Nokia SR Linux 他複数<br>
  Containerlabでは、yaml形式のトポロジーファイルをもとにコンテナをデプロイし、仮想配線も自動的に実施するため構築の手間を軽減してくれます。<br>

#### 参考サイト<br>
  〇　containerlab公式サイト<br>
  https://containerlab.dev/<br>
  〇　containerlab公式サイト（X）<br>
  https://x.com/go_containerlab<br>
  〇　Containerlabユーザ・マニュアル<br>
  　https://zenn.dev/moatdrive/books/containerlab-manual<br>
       
### １　Containerlabの導入(Ubuntu編）<br>
[次のチャプターへ進む](./introduction-1.md) <br>

### （参考）　Containerlabの導入(Aploma Linux編）<br>
[次のチャプターへ進む](./introduction-Aploma-Linux.md) <br>

### ２　Containerlabの基本操作<br>
[次のチャプターへ進む](./ContanerLab-basic-operation.md) <br>

### ３　Arista(cEOS)によるContainerlabによるネットワーク演習<br>
#### (1)  Aristaネットワークさん提供コンテナの導入<br>
[次のチャプターへ進む](./Arista-container-introduction.md) <br>

#### (2) コンテナイメージ起動及びマネージメントネットワークへのアクセス
　　[次のチャプターへ進む](./exercises-1.md) <br>

#### (3) Netshootの導入<br>
[次のチャプターへ進む](./introduction-Netshoot.md) <br>

#### (4) AristaEOSの基礎<br>
   [次のチャプターへ進む](./AristaEOS-BASIC.md) <br>

#### (5)　OSPF設定と確認<br>
  　[次のチャプターへ進む](./ospf.md) <br>

#### (6) IS-ISの設定と確認<br>

#### (7)　BGP設定と確認<br>
   [次のチャプターへ進む](./BGP-exercises.md) <br>

### (8) MLAGの設定と確認<br>

#### (9) VXLAN設定と確認<br>
　　[次のチャプターへ進む](./VXLAN-1.md) <br>　　

#### (10)EVPN/VXLAN設定と確認<br>
　  　[次のチャプターへ進む](./EVPN－VXLAN.md) <br>

### 5　FRRによるContainerlabによるネットワーク演習<br>

ブログもやってます~<br>
https://gorosuke5656.hatenablog.com/
