

## template

### yamlで書く
cloudfomationにおいてはyamlで書くほうがメリットが多い
* コメントが書ける
* 配列の最後に,をつけてformatエラーにならない

### 構成要素
```
AWSTemplateFormatVersion: 2010-09-09
Description: ---
Metadata: 

Parameters: 

Mappings: 

Conditions: 

Resources: 

Outputs:

```

* AWSTemplateFormatVersion(必須)
  テンプレートフォーマットのバージョン
  最新は公式ドキュメントを参照
* Description
  テンプレートの説明
* Metadata
  テンプレートの付加情報
* Parameters
  スタックを作成するときに値を設定したい場合にパラメータとして受け取る
  受け取った値をResourcesで宣言するリソースの設定値に指定が可能
* Mappings
  キーと値をマッピングする
* Conditions
  IF分岐などで使用
* Resources(必須)
  AWSリソースを宣言
* Outputs
  スタックの外にリソースの情報をアウトプットする
  Aスタックで宣言しているリソースのIDをBスタックで使用したい場合など
  

  
