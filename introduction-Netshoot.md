
### NetShootについて<br>
Netshootとは？？<br>
netshoot は、Docker Hub で公開されている Docker イメージで、<br>
ネットワークトラブルシューティングやデバッグに役立つ多機能なツールです<br>
事前に色々なツールがインストールされています！！<br>


〇参考にしたサイト<br>
本家サイト<br>
　https://github.com/nicolaka/netshoot<br>
Dockerのサイト<br>
　https://hub.docker.com/r/nicolaka/netshoot<br>
Qiitaで参考にしたサイト<br>
　https://qiita.com/iwaseyusuke/items/c82e810479f9537719c4<br>

 
### ContainerLabにおけるnetshootのインストール及び確認<br>

今回、以下の構成でnetshoowを導入してみました！<br>
![Diagram](./images/introduction-netshoot/1.jpg)<br>

以下、実施手順です。<br>

【事前準備】<br>
###### ①　netshootのインストール<br>
　　　　Docker Hub から Docker pull コマンドにより　”netshoot”をダウンロードする<br>
　②　ymlファイルの作成（ファイル：ospf-lab-2.yml)<br>
　③　ContainerLabの起動　【①のymlファイルを読みこみ起動】<br>
　④　CEOSにおける設定（OSPF）<br>

【確認】
　①　netshootにログインし、経路情報を確認<br>
　②　netshootにログインし、Tracerouteによる確認<br>
　③　Iperfでの確認<br>

【設定保存】
　　ContainerLab saveコマンドによる設定保存（CEOSにおいては事前に copy run start を実施しておく）<br>
 
今回使用したymlファイルは以下に格納しています！！<br>
　https://github.com/gorosuke5656/Container-lab/blob/main/yml-file/ospf-lab-2.yml<br>


#### 事前準備<br>
###### ①　netshootのインストール<br>
　　　　Docker Hub から Docker pull コマンドにより　”netshoot”をダウンロードする<br>
    ![Diagram](./images/introduction-netshoot/2.jpg)<br>
    ![Diagram](./images/introduction-netshoot/3.jpg)<br>
    ![Diagram](./images/introduction-netshoot/4.jpg)<br>

###### ②　ymlファイルの作成（ファイル：ospf-lab-2.yml)<br>
   ![Diagram](./images/introduction-netshoot/5.jpg)<br>
   ここでポイントですが、事前にnetshootに設定するIPアドレスおよび経路情報を明示して設定しておきます<br>

###### ③　ContainerLabの起動　【①のymlファイルを読みこみ起動】<br>
   ![Diagram](./images/introduction-netshoot/6.jpg)<br>

###### ④　CEOSにおける設定（OSPF）<br>
    ![Diagram](./images/introduction-netshoot/7.jpg)<br>


 #### 【確認】
###### ①　netshootにログインし、経路情報を確認<br>
　  ![Diagram](./images/introduction-netshoot/8.jpg)<br>
  
###### ②　netshootにログインし、Tracerouteによる確認<br>
　  ![Diagram](./images/introduction-netshoot/9.jpg)<br>
    ![Diagram](./images/introduction-netshoot/10.jpg)<br>
    
###### ③　Iperfでの確認<br>
   ![Diagram](./images/introduction-netshoot/11.jpg)<br>
   
    
   

   

   

    
    



 

 
#
