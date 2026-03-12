##

### ec2からRDSへの接続(postgres)


### キーペアについて
ec2起動時に作成した場合、ブラウザ経由でダウンロードされる
ssh等で接続する場合、キーの場所、権限によって接続できない場合があるので注意

* 権限の修正
  ```
  $path = ".ssh\SSH鍵名.pem"
  icacls.exe $path /reset
  icacls.exe $path /GRANT:R "$($env:USERNAME):(R)"
  icacls.exe $path /inheritance:r
  ```

###
[Windowsコマンドプロンプトからec2にsshする](https://qiita.com/sumomomomo/items/28d54e35bfa5bc524cf5)
