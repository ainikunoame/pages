#

## dd：データをブロック多淫委でコピー・変換する

- **fomat:** `dd [option]`
- **option:**
    - `if=file` : 標準出力の代わりにファイルから読み出す。デバイスファイルも指定可能
    - `of=file` : 標準出力の代わりにファイルへ書き込む。デバイスファイルも指定可能
    - `bs=バイト数` : 1回に読み書きするブロックサイズ
    - `count=` : 指定したサイズのブロックを入力から指定数コピーする
- **ex:**
    ```bash
    dd if=/dev/zero of=test.txt bs=1024 count=1
    # /dev/zeroからtest.txtへ1024bytesコピーする
    ```
- **tips:**
    - `/dev/zero` : 0x00を常に出力し続ける特殊なデバイスファイル
    - `/dev/null` : 入力はすべて破棄。読み取り時は常にEOFを返す特殊なデバイスファイル
---

## awk：テキストファイルやストリームをフィールドごとに処理・編集する

- **fomat:** `awk 'pattern {action}' file`
- **pattern:**
    - `/正規表現/`
    - `BEGIN`
    - `END`
    - `評価式`
- **option:**
    - `-f commandfile` : awkコマンドが書かれたファイルを指定
    - `-F 区切り文字` : 区切り文字を指定。複数指定可能
    - `-v 変数=値` : 変数を定義する
- **ex:**
    ```bash
    echo 1;2;3;4 | awk -F '[;]' '{print $1}'
    1
    ```
---

## ss：desc

- **fomat:** `command [options] [args]`
- **option:**
    - `-x` : 説明
    - `-y` : 説明
- **ex:**
    ```bash
    よく使う実行例
    ```
---
<!-- template

## command：desc

- **fomat:** `command [options] [args]`
- **option:**
    - `-x` : 説明
    - `-y` : 説明
- **ex:**
    ```bash
    よく使う実行例
    ```
---

-->
