# iSCSIとは

ストレージは大きく分けて2種類ある。

1つはファイルストレージで、一般的には**NAS**と呼ばれている。

もう1つはブロックストレージで、これはさらにSASケーブル等の専用ケーブルでサーバと直結する
「**DAS（Direct Attached Storage）**」と、SAN（Storage Area Network）というネットワークでサーバと接続する「**SANストレージ**」の2つに分かれる。

iSCSIはSANストレージとの接続方式に該当する。。
つまり、iSCSIとはSANの一種。

## DASとは
DASとは、ブロックストレージの1種で、主にSASケーブルを使ってサーバと直接（Direct）に接続される。
構成としてはエンクロージャと呼ばれる筐体が中心となり、エンクロージャにHDDを詰めていく。

ストレージの種類によって搭載できるHDDのk図や利用できるHDDの種類、RAIDコントローラーの種類などが決まっている。



## SANの種類とメリット、デメリット
SANとはFibre Channel（FC）やFC over Ethernet（FCoE）、iSCSIといったプロトコルを使ってブロックアクセスを行わせる、ストレージ専用ネットワークのこと。

そしてSANストレージはSANを介してサーバと接続されるブロックストレージの一種。

FC/FCoE/iSCSIのいずれのプロトコルもSCSIコマンドをカプセルかするものですので、基本的にはDASと同様のブロックアクセスを行う。

つまり、SANストレージはファイルシステムを理解せず、接続元であるサーバOSがファイルシステムを理解したうえでSANストレージにSCSIコマンドによるブロックレベルでのアクセスを行う。

例:DELL PowerVault MD1000 1つのエンクロージャにSAS/SATAのいずれかを15個搭載でき、エンクロージャを6つ拡張でき、RAIDは0, 1, 5, 6, 10, 50, 60が使える。

https://milestone-of-se.nesuke.com/sv-basic/architecture/das-nas-san-storage/
https://www.softbank.jp/biz/blog/business/articles/202007/storage-difference/
