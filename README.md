kintone Plug-in Gantt
==========================

kintone でガントチャートを表示するプラグインです。  
[cybozu社が作成したプラグインサンプル](https://developer.cybozu.io/hc/ja/articles/203716110-%E3%82%AC%E3%83%B3%E3%83%88%E3%83%81%E3%83%A3%E3%83%BC%E3%83%88%E3%83%97%E3%83%A9%E3%82%B0%E3%82%A4%E3%83%B3#step5)をカスタマイズしたものです。
* 着色設定を任意に（全てデフォルト色）
* 担当者をツールチップに表示
* 担当者ごとに色分け（着色指定しない場合）


## Requirement

* Node.js v6 or later

## How to Use

```bash
$ npm install -g @kintone/plugin-packer
$ kintone-plugin-packer <plug-in dir> [--ppk <key file>]
```

For more information, please check the following pages.

* https://github.com/kintone/plugin-packer
* https://developer.cybozu.io/hc/ja/articles/360000910783 (in Japanese)

## Output Files

### Plug-in Package
パッケージングされたプラグイン。

```bash
plugin.zip
```

### Private Key
kintoneでプラグインを一意に識別するためのキー。

```bash
<plug-in id>.ppk
```
**Do not lose the private key!** Keep the .ppk file secret and in a safe place. You'll need it later if you want to update the plug-in.

## Example

```bash
$ cd /tmp
$ git clone https://github.com/kintone/plugin-examples
$ cd plugin-examples
$ npm install -g @kintone/plugin-packer
$ kintone-plugin-packer examples/colorcell
Succeeded: /tmp/plugin-examples/examples/plugin.zip
$ ls examples/*.ppk
examples/dhcpcmonencgafiddfaofdfednmjnbem.ppk
```

## 1回め（例）
```bash
kintone-plugin-packer ganttchart/
```


## 2回め（例）
プラグインのIDキーを指定する。
```bash
$ kintone-plugin-packer --ppk pluginid.ppk ganttchart/
```


## Install Plug-in

パッケージングしたZipファイルは[こちら](https://github.com/january108/kintone-plugin-gantt/blob/master/plugin.zip)をどうぞ。  
ただし、不具合がある場合はご容赦ください。また、問い合わせはご容赦ください。  

インストール方法は、以下のリンクを参照してください。
See the following document.

en

https://help.cybozu.com/en/k/admin/plugin.html

ja

https://help.cybozu.com/ja/k/admin/plugin.html

## Using

* [PleaseJS](https://github.com/Fooidge/PleaseJS)
 ランダムな色を生成

## Licence

Copyright(c) 2021 january108  
Release under MIT License  
https://opensource.org/licenses/mit-license.php

Copyright(c) Cybozu, Inc.  
Release under MIT License

