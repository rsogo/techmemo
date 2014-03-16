手順はwls12120.zipに含まれている
README.txtを参照して行った。

# 準備
## ファイルの解凍
	unzip wls1212_dev.zip -d wls1212
      cd wls1212/wls12120/
	[ncdc@www3225ug wls12120]$ pwd
	/home/ncdc/wls1212/wls12120
	[ncdc@www3225ug wls12120]$ ls -al
	合計 68
	drwxr-xr-x 5 ncdc ncdc 4096  6月  7 17:23 2013 .
	drwxrwxr-x 3 ncdc ncdc 4096  3月 16 18:39 2014 ..
	-rw-r--r-- 1 ncdc ncdc 6598  8月 23 03:19 2013 README.txt
	-rw-r--r-- 1 ncdc ncdc 6770  8月 23 03:21 2013 README_WIN.txt
	drwxr-xr-x 5 ncdc ncdc 4096  6月  7 17:22 2013 coherence
	-rw-r--r-- 1 ncdc ncdc 5500  6月  7 17:22 2013 configure.cmd
	-rwxr-x--- 1 ncdc ncdc 6451  6月  7 17:23 2013 configure.sh
	-rw-r--r-- 1 ncdc ncdc 3699  6月  7 17:22 2013 configure.xml
	-rw-r--r-- 1 ncdc ncdc  171  6月  7 17:22 2013 domain-registry.xml
	drwxr-xr-x 8 ncdc ncdc 4096  6月  7 17:22 2013 oracle_common
	-rw-r--r-- 1 ncdc ncdc 4998  6月  7 17:22 2013 osarch.xml
	drwxr-xr-x 8 ncdc ncdc 4096  6月  7 17:22 2013 wlserver

 
## JAVA_HOME
	[ncdc@www3225ug wls12120]$ echo $JAVA_HOME
	/usr/java/default/
	[ncdc@www3225ug wls12120]$ which java
	/usr/java/default/bin/java
	[ncdc@www3225ug wls12120]$ /usr/java/default/bin/java -version
	java version "1.7.0_40"
	Java(TM) SE Runtime Environment (build 1.7.0_40-b43)
	Java HotSpot(TM) 64-Bit Server VM (build 24.0-b56, mixed mode)

## MW_HOME
	[ncdc@www3225ug wls12120]$ echo $MW_HOME
	[ncdc@www3225ug wls12120]$ export MW_HOME=/home/ncdc/wls1212/wls12120
	[ncdc@www3225ug wls12120]$ echo $MW_HOME
	/home/ncdc/wls1212/wls12120



# インストール
## start install

	[ncdc@www3225ug wls12120]$ . ./configure.sh 
	**************************************************
	WebLogic Server 12g (12.1.2.0) Zip Configuration

	MW_HOME:   /home/ncdc/wls1212/wls12120
	JAVA_HOME: /usr/java/default/
	**************************************************

	Please wait while 745 jars are unpacked ...
	Unpacking glassfish.jsf_1.0.0.0_2-1-20.jar                          


	Please wait while 745 jars are unpacked ...
	...Unpacking done                       0.0.jar                                              0 to goo goto go


	BUILD SUCCESSFUL
	Total time: 0 seconds
	CLASSPATH=/usr/java/default//lib/tools.jar:/home/ncdc/wls1212/wls12120/wlserver/server/lib/weblogic_sp.jar:/home/ncdc/wls1212/wls12120/wlserver/server/lib/weblogic.jar:/home/ncdc/wls1212/wls12120/wlserver/server/lib/webservices.jar:/home/ncdc/wls1212/wls12120/oracle_common/modules/org.apache.ant_1.7.1/lib/ant-all.jar:/home/ncdc/wls1212/wls12120/oracle_common/modules/net.sf.antcontrib_1.1.0.0_1-0b2/lib/ant-contrib.jar:/home/ncdc/wls1212/wls12120/wlserver/modules/features/oracle.wls.common.nodemanager_1.0.0.0.jar:

	PATH=/home/ncdc/wls1212/wls12120/wlserver/server/bin:/home/ncdc/wls1212/wls12120/oracle_common/modules/org.apache.ant_1.7.1/bin:/usr/java/default//jre/bin:/usr/java/default//bin:/usr/local/rbenv/shims:/usr/local/rbenv/bin:/usr/java/default/bin:/usr/local/bin:/bin:/usr/bin:/usr/local/sbin:/usr/sbin:/sbin:/home/ncdc/bin:/home/ncdc/wls1212/wls12120/oracle_common/modules/org.apache.maven_3.0.4/bin

	Your environment has been set.
	Configuring WLS...

	BUILD SUCCESSFUL
	Total time: 0 seconds

	Do you want to configure a new domain?  [y/n]? y
	<2014/03/16 18時58分13秒 JST> <Info> <Security> <BEA-090905> <起動パフォーマンスを向上するためにCryptoJ JCEプロバイダ自己整合性チェックを無効にしています。このチェックを有効にするには、-Dweblogic.security.allowCryptoJDefaultJCEVerification=trueを指定します。> 
	<2014/03/16 18時58分14秒 JST> <Info> <Security> <BEA-090906> <RSA CryptoJのデフォルトの乱数ジェネレータをECDRBGからFIPS186PRNGに変更しています。この変更を無効にするには、-Dweblogic.security.allowCryptoJDefaultPRNG=trueを指定します。> 
	<2014/03/16 18時58分15秒 JST> <Info> <WebLogicServer> <BEA-000377> <WebLogic ServerをOracle CorporationからJava HotSpot(TM) 64-Bit Server VMバージョン24.0-b56で起動しています。> 
	<2014/03/16 18時58分15秒 JST> <Info> <Management> <BEA-140013> </home/ncdc/wls1212/wls12120/user_projects/domains/mydomain/configが見つかりません> 
	<2014/03/16 18時58分15秒 JST> <Info> <Security> <BEA-090065> <ユーザーから起動アイデンティティを取得しています。> 
	WebLogic Serverを起動するためのユーザー名を入力してください:weblogic
	WebLogic Serverを起動するためのパスワードを入力してください:
	確認のために、WebLogic Serverの起動に必要なパスワードを再入力してください:
	<2014/03/16 18時58分49秒 JST> <Info> <Management> <BEA-141254> </home/ncdc/wls1212/wls12120/user_projects/domains/mydomainに新しいドメイン・ディレクトリを生成しています。> 
	<2014/03/16 18時59分24秒 JST> <Info> <Management> <BEA-141255> <ドメインの生成は34,388ミリ秒で完了しました。> 
	<2014/03/16 18時59分24秒 JST> <Info> <Management> <BEA-141107> <バージョン: WebLogic Server 12.1.2.0.0  Fri Jun 7 15:16:15 PDT 2013 1530982 WLS_12.1.2.0.0_GENERIC_130607.1100> 
	<2014/03/16 18時59分25秒 JST> <Notice> <WebLogicServer> <BEA-000365> <サーバー状態がSTARTINGに変化しました。> 
	<2014/03/16 18時59分25秒 JST> <Info> <WorkManager> <BEA-002900> <自己チューニング・スレッド・プールを初期化しています。> 
	<2014/03/16 18時59分26秒 JST> <Notice> <Log Management> <BEA-170019> <サーバー・ログ・ファイル/home/ncdc/wls1212/wls12120/user_projects/domains/mydomain/servers/myserver/logs/myserver.logを開きました。すべてのサーバーサイド・ログ・イベントはこのファイルに書き込まれます。> 
	<2014/03/16 18時59分40秒 JST> <Notice> <Security> <BEA-090082> <セキュリティはセキュリティ・レルムmyrealmを使用して初期化しています。> 
	<2014/03/16 18時59分45秒 JST> <Notice> <WebLogicServer> <BEA-000365> <サーバー状態がSTANDBYに変化しました。> 
	<2014/03/16 18時59分45秒 JST> <Notice> <WebLogicServer> <BEA-000365> <サーバー状態がSTARTINGに変化しました。> 
	<2014/03/16 18時59分45秒 JST> <Notice> <Log Management> <BEA-170027> <サーバーはドメイン・レベルの診断サービスとの接続を正常に確立しました。> 
	<2014/03/16 18時59分45秒 JST> <Notice> <WebLogicServer> <BEA-000365> <サーバー状態がADMINに変化しました。> 
	<2014/03/16 18時59分45秒 JST> <Notice> <WebLogicServer> <BEA-000365> <サーバー状態がRESUMINGに変化しました。> 
	<2014/03/16 18時59分45秒 JST> <Warning> <Server> <BEA-002611> <ホスト名"localhost"は複数のIPアドレスにマップされています: 127.0.0.1, 0:0:0:0:0:0:0:1。> 
	<2014/03/16 18時59分45秒 JST> <Notice> <Server> <BEA-002613> <チャネル"Default"は、現在49.212.158.239:7001でプロトコルiiop, t3, ldap, snmp, httpをリスニングしています。> 
	<2014/03/16 18時59分45秒 JST> <Notice> <Server> <BEA-002613> <チャネル"Default[1]"は、現在fe80:0:0:0:5054:7ff:fe00:3225:7001でプロトコルiiop, t3, ldap, snmp, httpをリスニングしています。> 
	<2014/03/16 18時59分45秒 JST> <Notice> <Server> <BEA-002613> <チャネル"Default[3]"は、現在127.0.0.1:7001でプロトコルiiop, t3, ldap, snmp, httpをリスニングしています。> 
	<2014/03/16 18時59分45秒 JST> <Notice> <Server> <BEA-002613> <チャネル"Default[2]"は、現在0:0:0:0:0:0:0:1:7001でプロトコルiiop, t3, ldap, snmp, httpをリスニングしています。> 
	<2014/03/16 18時59分45秒 JST> <Notice> <WebLogicServer> <BEA-000331> <ドメイン"mydomain"で、WebLogic Server管理サーバー"myserver"を開発モードで起動しました。> 
	<2014/03/16 18時59分45秒 JST> <Notice> <WebLogicServer> <BEA-000365> <サーバー状態がRUNNINGに変化しました。> 
	<2014/03/16 18時59分45秒 JST> <Notice> <WebLogicServer> <BEA-000360> <サーバーがRUNNINGモードで起動しました。> 

#　起動停止
## 起動

	[ncdc@www3225ug mydomain]$ nohup ./startWebLogic.sh > start_std.log 2> start_err.log &
	[1] 31876

## 停止

	[ncdc@www3225ug mydomain]$ bin/stopWebLogic.sh 




