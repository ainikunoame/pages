# Excel Tips
- [名前の定義](#名前の定義)
- [トピック2](#トピック2)
- [tips](#tips)
- [参考](#参考)

<a id="名前の定義"></a>
## 名前の定義
セル、範囲、数式に名前を定義できる

ctrl + F3で名前の管理ウィンドウを操作する

### 非表示になっている名前の定義を再表示させる
VBAにて以下のマクロを実行する

```
Public Sub VisibleNames()
    Dim name As Object
    For Each name In Names
        If name.Visible = False Then
            name.Visible = True
        End If
    Next
    MsgBox "すべての名前の定義を表示しました。", vbOKOnly
End Sub
```




<a id="トピック2"></a>
## トピック2

<a id="tips"></a>
## tips

<a id="参考"></a>
## 参考
[お名前ドットコムでドメインを無料で取得する方法と注意点](https://kagechiku.com/freedomain/)

## version
1.0.0
