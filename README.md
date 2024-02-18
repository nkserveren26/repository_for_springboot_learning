# Spring Boot学習用

## 環境構築

OS：Windows 10  
Amazon Corretto：21  
Maven：3.6.3

### ソフトウェアのインストール
#### Amazon Correttoインストール
以下ページの赤枠リンクからインストーラーをダウンロードする。
https://docs.aws.amazon.com/corretto/latest/corretto-21-ug/downloads-list.html

![img.png](img.png)

インストーラーを起動し、画面の指示に従いインストールを実行。

インストール後、以下の環境変数がセットされていることを確認。  
値が設定されていなければ追加する。  
　JAVA_HOME  
　　インストールディレクトリが値にセットされていること  
　PATH  
　　値に「インストールディレクトリ/bin」が含まれていること  

コマンドプロンプトを起動し、以下のコマンドを実行し、JDKのバージョン等の情報が帰ってくることを確認。  
　java --version  

```
openjdk 21.0.2 2024-01-16 LTS
OpenJDK Runtime Environment Corretto-21.0.2.13.1 (build 21.0.2+13-LTS)
OpenJDK 64-Bit Server VM Corretto-21.0.2.13.1 (build 21.0.2+13-LTS, mixed mode, sharing)
```

<br />

### Spring Bootプロジェクト作成
#### Spring Initializerを使ってプロジェクトを作成
Spring Initializerのサイトにアクセス。  
https://start.spring.io/

作成するSpring Bootプロジェクトの各種設定は以下。  
　Project：Maven  
　Language：Java  
　Spring Bootのバージョン：最新版を選択  
　Group、Artifact：任意の名前を入力  
　Packaging：Jar  
　Javaのバージョン：21  
　Dependencies：Spring Webを選択  

上記設定のうえ、GENERATEをクリックし、zipファイルをダウンロード。
![img_1.png](img_1.png)

zipファイルを展開し、中にあるフォルダを所定のディレクトリに配置する。  

<br />

IntelliJを開き、Open→配置したフォルダを選択

#### IntelliJで使用するJDKをAmazon Correttoに設定
プロジェクトを開いた後、JDKのセットアップができていない旨のメッセージが表示される場合がある。  
その場合、メッセージと共に表示されている「Setup JDK」をクリックし、  
Amazon Correttoインストールディレクトリを選択することで問題は解消される。