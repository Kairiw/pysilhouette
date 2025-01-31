概要
================================================================================
pysilhouetteは、逐次的に登録されたジョブ(コマンド)を実行する機能を有するジョブマネジャーです。
主にウェブアプリケーションのバックグラウンド処理を実現するために開発されています。

pysilhouetteは、以下の特長を持っています。
    * 100% Pure Pythonで開発されているアプリケーションです。
    * シンプルな監視機能を有し、信頼性を向上させています。
    * ジョブグループ単位で実行されそのなかで複数のジョブを実行することができます。
    * 各ジョブ単位でロールバック処理を追加することができます。
    * 複数のデータベースをサポートしています。


インストールについて
================================================================================
同一フォルダにあるINSTALLを参照してください。


入手法
================================================================================
pysilhouetteはリポジトリにGitを採用しています。
最新のソースコードは次のコマンドで取得できます。
    # git clone https://github.com/karesansui/pysilhouette


ホームページ
================================================================================
pysilhouetteのホームページのURLは
    http://pysilhouette.sourceforge.jp/
です。


依存パッケージ
================================================================================
必須パッケージ
    * python >= 2.7
    * SQLAlchemy = 1.4

SQLLiteを使用する場合
    SQLite >= 3.3.x
    pysqlite >= 2.5.x

MySQLを使用する場合
    MySQL >= 5.0.x
    MySQLdb >= 1.2.x

PostgreSQLを使用する場合
    PostgreSQL >= 8.1.x
    psycopg2 >= 2.0.x


ディレクトリ構成
================================================================================
.
|-- AUTHORS # 著作者
|-- ChangeLog # チェンジログ
|-- INSTALL # 英語版インストールマニュアル
|-- INSTALL.ja # 日本語版インストールマニュアル
|-- LICENSE # ライセンス
|-- MANIFEST.in # distutilsを利用したパッケージングをするのに使用する。
|-- README # 英語版インストールマニュアル
|-- README.ja # 日本語版インストールマニュアル
|-- debian # 仮
|   |-- README.Debian
|   |-- changelog
|   |-- compat
|   |-- control
|   |-- copyright
|   |-- dirs
|   |-- docs
|   |-- performerd.init
|   |-- postinst
|   |-- postrm
|   |-- preinst
|   |-- prerm
|   |-- pycompat
|   |-- rules
|   |-- schedulerd.init
|   |-- silhouetted.default
|   `-- silhouetted.init
|-- doc # ドキュメントや設定ファイル関連置き場
|   `-- epydoc.cfg # epydoc設定ファイル
|-- sample # サンプルプログラム関連
|   |-- log.conf.example # ログ設定ファイルのテンプレート
|   |-- rc.d # 起動スクリプト
|   |   `-- init.d
|   |       |-- asynperformerd # 並列処理用デーモンの起動スクリプト
|   |       |-- asynschedulerd # 並列処理用スケジュールデーモンの起動スクリプト
|   |       |-- performerd # 逐次処理用デーモンの起動スクリプト
|   |       |-- schedulerd # 逐次処理用スケジュールデーモンの起動スクリプト
|   |       `-- silhouetted # アプリケーション(監視を含む)の起動スクリプト
|   |-- redhat.spec # RPM用のspecファイル
|   |-- scripts
|   |   |-- dummy.py
|   |   |-- insert_dummy.py
|   |   |-- sendmail.py
|   |   |-- test_failure.py
|   |   `-- test_success.py
|   |-- silhouette.conf.example # Pysilhouette設定ファイルのテンプレート
|   |-- sysconfig # システム設定ファイル
|   |   `-- silhouetted
|   `-- whitelist.conf.example # ホワイトリスト設定ファイルのテンプレート
|-- pysilhouette # プログラム本体
|   |-- __init__.py
|   |-- asynperformer.py
|   |-- asynscheduler.py
|   |-- command.py
|   |-- daemon.py # デーモン化で利用する関数群
|   |-- db # Database関連
|   |   |-- __init__.py
|   |   |-- access.py # Databaseの操作
|   |   |-- model.py # Databaseのテーブルモデル
|   |-- er.py
|   |-- log.py
|   |-- performer.py
|   |-- prep.py # 初期処理で利用する関数群
|   |-- scheduler.py
|   |-- silhouette.py
|   |-- tests # テスト関連
|   |   |-- __init__.py
|   |   |-- suite.py
|   |   |-- testprep.py
|   |   |-- testutil.py
|   |   `-- testworker.py
|   |-- uniqkey.py # Unique key for the instance.
|   |-- util.py
|   `-- worker.py
|-- setup.cfg # distutilsを利用したパッケージングをするのに使用する設定ファイル
|-- setup.py # distutilsを利用したパッケージングをするのに使用する実行ファイル
`-- tools # 開発時や運用時に利用するコマンドベースの実行ファイル
    |-- epydoc.sh # Javadoc風なドキュメントを自動生成する実行ファイル
    |-- psil-cleandb # Databaseを初期化する実行ファイル
    |-- psil-set # コマンドラインからジョブコマンドを登録する実行ファイル
    `-- sqlite2other.py

著作権/ライセンス
================================================================================

Copyright (c) 2009-2010 HDE, Inc.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.


感謝
================================================================================
SQLAlchemy people.
HDE, Inc. and other related members.
All people in Python community.
