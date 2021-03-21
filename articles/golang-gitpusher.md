---
title: "gitコマンドに音付けませんか？"
emoji: "🌈"
type: "tech"
topics: ["golang", "git", "push", "tool"]
published: true
---

# gitコマンドに音付けませんか？

![](https://storage.googleapis.com/zenn-user-upload/x719gdg99xhsz8mrkxxlum37p561)

```git push```した時に励ましてくれる存在を探している自分が常にいます
そこで、gitコマンドで```git push``` or ```git commit```した時に自動的に音楽が流れるツールを作りました

## 使い方

- githubリポジトリからgit pusherをダウンロード

terminalで```git clone https://github.com/jumang4423/gpshr.git```と打ち込みます

- README.mdに従ってインストール

terminalで/gpshrに移動し、以下のコマンドを実行します

```bash
chmod +x install.sh
./install.sh
```

コマンドがインストールできました、```gpshr```と打ってみましょう

![](https://storage.googleapis.com/zenn-user-upload/185knx435od1u6ry05dakwol354s)

この様なヘルプが出てくればインストールは完了です

- gitで初期化されたフォルダーに音声を再生させる設定をインストールする

```git init```されたgitで管理されているフォルダーに移動します
そこでgpshrコマンドを利用することで音を追加できます

```ls -al``` で.gitフォルダーがあることを確認したら以下のコマンドを使います

```bash
gpshr -install . -hooks push
```
または
```bash
gpshr -install . -hooks commit
```
そうすると、どの音声ファイルをpush || commitした時に鳴らすか聞いてくるので、番号を打って設定します

- gitコマンドを使って実際に検証

以下のコマンドのどれかを実行した際に音楽が流れるハズです
```bash
git add *
git commit -m "hoge"
git push origin main
```


