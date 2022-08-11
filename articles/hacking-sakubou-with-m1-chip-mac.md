---
title: "Hacking:美しき策謀 のLive CDイメージをApple M1プロセッサ搭載のMacで動かす"
emoji: "🌏"
type: "tech" 
topics: [m1, mac, hacking, 策謀本]
published: true
---

## こんな人のために・・・

- M1 Macで策謀本を進めてみたいけど、LiveCDがx86(i686)のため、Macで動かすことができない
- qemuじゃなくてサクッとLiveCDイメージを動かしたい

## 導入

1. [Hacking：美しき策謀のウェブサイト](https://www.oreilly.co.jp/books/9784873115146/) にアクセスし、関連ファイル -> LiveCDをクリックして、LiveCDイメージをダウンロード

2. [UTM](https://mac.getutm.app)をダウンロードしてインストール（無料です）

3. UTMを起動

4. Create a New Virtual Machineをクリックし、仮想環境を作成

![](https://storage.googleapis.com/zenn-user-upload/7703e805fcfd-20220811.png)

5. Emulateをクリック

m1のアーキテクチャはarmベースのアーキテクチャだが、LiveCDはx86アーキテクチャなのでエミュレーションをする。

![](https://storage.googleapis.com/zenn-user-upload/8e1c6625ed86-20220811.png)

6. Linuxをクリック

![](https://storage.googleapis.com/zenn-user-upload/5a945a0b6eb8-20220811.png)

7. Boot ISO ImageのBrowseをクリックし、LiveCDのISOイメージを選択

![](https://storage.googleapis.com/zenn-user-upload/9450815c026a-20220811.png)

8. architectureをi386(x86)に変更

![](https://storage.googleapis.com/zenn-user-upload/06d0e3db5035-20220811.png)

9. Nextをクリック

![](https://storage.googleapis.com/zenn-user-upload/d4c7672dbaf4-20220811.png)

10. ファイルをホストと共有しない場合はNextをクリック

![](https://storage.googleapis.com/zenn-user-upload/b52018729670-20220811.png)

11. Nameを任意の名前に変更して、Saveをクリック

![](https://storage.googleapis.com/zenn-user-upload/7cdee2cef663-20220811.png)

12. 作った仮想環境をクリックし（今回の場合は”策謀Linux”）右上の設定ボタンをクリック

![](https://storage.googleapis.com/zenn-user-upload/902a3e8e882f-20220811.png)

13. QEMUタブのUEFI Bootのチェックを外してSaveをクリック

![](https://storage.googleapis.com/zenn-user-upload/3cea9467fe0b-20220811.png)

14. 再生ボタンをクリックして、仮想環境を起動

２０秒ぐらいで以下の画面が出るのでEnterキーを押す

![](https://storage.googleapis.com/zenn-user-upload/94a834304ec6-20220811.png)

15. 多分２分ぐらいでGUIが表示される。やったね！

![](https://storage.googleapis.com/zenn-user-upload/8b6c86b4d9d0-20220811.png)


## 参考

- バカ重いので（OSをエミュレートなので）GUIでぐりぐりいじってるとフリーズすると思う
- 楽しいhackingライフを！
