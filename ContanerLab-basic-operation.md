操作の説明として下記の例で説明します<br>
#### 今回の説明事例<br>
  ![Diagram](./images/ContanerLab-basic-operation/1.jpg)<br>
  図のようにCEOS２台とPC(Netshoot）が２台稼働する状態です<br>
###今回の起動ファイル<br>
 ![Diagram](./images/ContanerLab-basic-operation/2.jpg)<br>
起動ファイルは　"ospf-lab-2.yml”になります。<br>


#####　ContanerLab起動<br>
管理者権限(root)若しくはsudoコマンドで以下のように指定して起動します<br>

root@gorosuke-vartual-box:home/gorosuke/container_lab#ContanerLab　deploy -t ospf-lab-2.yml<br>
![Diagram](./images/ContanerLab-basic-operation/3.jpg)<br>

 ###### 起動後の表示<br>
 起動が完了すると以下のように表示されます！
![Diagram](./images/ContanerLab-basic-operation/4.jpg)<br>

#### 起動コンテナの状態確認<br>
root@gorosuke-vartual-box:home/gorosuke/container_lab#clab inspect --all<br>
![Diagram](./images/ContanerLab-basic-operation/5.jpg)<br>

また以下のようにDocker psコマンドでも確認できます
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
