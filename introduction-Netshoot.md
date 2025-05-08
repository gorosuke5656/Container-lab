
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

【事前準備】<br>
　①　netshootのインストール
　　Docker Hub からnetshootをダウンロードする<br>

　②　ymlファイルの作成（ファイル：ospf-lab-2.yml)<br>
　　　以下の条件で設定<br>

 

今回使用したymlファイルは以下に格納しています！<br>
　https://github.com/gorosuke5656/Container-lab/blob/main/yml-file/ospf-lab-2.yml<br>






 

 
### 今回の起動ファイル<br>
 ![Diagram](./images/ContanerLab-basic-operation/2.jpg)<br>
起動ファイルは　"ospf-lab-2.yml”になります。<br>
##### ContanerLab起動<br>
管理者権限(root)若しくはsudoコマンドで以下のように指定して起動します<br>
root@gorosuke-vartual-box:home/gorosuke/container_lab#ContanerLab　deploy -t ospf-lab-2.yml<br>
![Diagram](./images/ContanerLab-basic-operation/3.jpg)<br>

 ###### 起動後の表示<br>
 起動が完了すると以下のように表示されます！
![Diagram](./images/ContanerLab-basic-operation/4.jpg)<br>

#### 起動コンテナの状態確認<br>
root@gorosuke-vartual-box:home/gorosuke/container_lab#clab inspect --all<br>
![Diagram](./images/ContanerLab-basic-operation/5.jpg)<br>

また以下のようにDocker psコマンドでも確認できます<br>
root@gorosuke-vartual-box:home/gorosuke/container_lab#docker ps<br>
![Diagram](./images/ContanerLab-basic-operation/6.jpg)<br>
起動したコンテナは/etc/hostsファイルに登録されるためコンテナ名でアクセスが可能です！<br>
![Diagram](./images/ContanerLab-basic-operation/7.jpg)<br>

#### 起動コンテナへのアクセス<br>
起動するコンテナによって若干異なります<br>
〇 Aristaさんコンテナの場合<br>
root@gorosuke-vartual-box:home/gorosuke/container_lab#docker exec -it ”ラボ名+コンテナ名" Cli<br>
![Diagram](./images/ContanerLab-basic-operation/8.jpg)<br>

〇Linux(netshoot)の場合
 root@gorosuke-vartual-box:home/gorosuke/container_lab#docker exec -it ”ラボ名+コンテナ名" bash<br>
![Diagram](./images/ContanerLab-basic-operation/9.jpg)<br>

#### 起動NWのトポロジー表示<br>
以下のコマンドでトポロジーファイルを表示できます！<br>
 root@gorosuke-vartual-box:home/gorosuke/container_lab#containerlab graph -t  "起動ファイル" <br>
![Diagram](./images/ContanerLab-basic-operation/10.jpg)<br>

#### 起動コンテナの停止<br>
 root@gorosuke-vartual-box:home/gorosuke/container_lab#containerlab graph -t  "起動ファイル" <br>

