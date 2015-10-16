ms。ContentId: FBBAADE6-F1A1-4B5C-8FD2-BDCA3FCF81CA
タイトル: 手順 6: 使用するとチェックポイント

#チェックポイントを使用して、手順 6: 実験

チェックポイントでは、更新プログラムを適用する、ソフトウェアのインストール設定を変更するなどの変更を行う前に、仮想マシンの現在の状態を保存するときに便利なツールは。
変更に問題が発生した場合は、チェックポイントを復元して戻ます。



チェックポイントの 2 つの種類があります。
**運用チェックポイント**: 実稼働環境でのサーバーでは主に使用します。
**標準的なチェックポイント**: 開発に使用される、またはテスト環境


実稼働のチェックポイントは、Windows 10 では、HYPER-V の既定値です。


##チェックポイントの種類を変更します。

まず、チェックポイントの古いスタイルをダウンロードして **標準的なチェックポイント**です。
実稼働のチェックポイントは、既定では、仮想マシンの設定に、チェックポイントの種類を変更する必要があります。

1. 右クリックし **Windows チュートリアルの仮想マシン** 選択 **設定**です。
2.  **管理** セクションで、 **チェックポイント**です。
3. 選択 **標準的なチェックポイント**です。
    ダイアログ ボックスは、次のようになります。
    
    ![](media/standard1.png)
4.  [**OK**] をクリックして、ダイアログ ボックスを閉じます。

##チェックポイントをテストするメモ帳を開く

チェックポイントの種類ごとで発生する内容を表示するのには、VM で、アプリケーションを実行おをします。

1. 右クリックし **Windows チュートリアルの仮想マシン** 選択 **接続**です。
2. 仮想マシンを開きます **メモ帳** ] をクリックして、 **開始** メニューと入力して **メモ帳** し、結果から選択します。
    
3. メモ帳で、次のように入力します **これは、チェックポイントのテスト。**。ファイルは、次のようになります。
    
    ![](media/standard_notepad.png)
4. としてファイルを保存 **test.txt**, 、メモ帳を閉じますはありませんが。
    仮想マシンで実行されていることをそのまま使用します。

##標準的なチェックポイントを作成します。

1. チェックポイントを作成する] をクリックして、 ![](media/checkpoint_button.png) **チェックポイント** メニュー バーのボタンをクリックします。
    
2. チェックポイントの名前] ダイアログ ボックスで次のように入力します。 **標準**です。
    ダイアログ ボックスは、次のようになります。
    
    ![](media/save_standard.png)
    
3. チェックポイントが下に表示されますが、プロセスが完了すると、 **チェックポイント** で、 **HYPER-V Manager**です。
    
    ![](media/standard_complete.png)
    

##実稼働のチェックポイントを作成します。

ここで、変更する必要があるためにバックアップする必要があるのチェックポイントの種類を変更 **運用チェックポイント** 2 番目のチェックポイントを実行する前にします。

1.  仮想マシンを右クリックし、をクリックして **設定**です。
2.   **管理** セクションで、 **チェックポイント**です。
3.  選択 **運用チェックポイント**です。
4.  フォールバック オプションをオフにします。
    システムが実稼働のチェックポイントを実行できない場合に、標準的なチェックポイントを使用せずに失敗します。
    
    ![](media/production.png)
5.  クリックして **OK** ] ダイアログ ボックスを閉じます。
6.  VM でもう一度右クリックして **接続**です。
7.  VM でメモ帳でという別の行を入力 **これは、テストの実稼働のチェックポイントの** し、ファイルを再度保存します。
8.  クリックして、 ![](media/checkpoint_button.png) **チェックポイント** メニュー バーのボタンをクリックします。
9.  入力を求めるメッセージが表示されたら、という名前を付けます **実稼働** 順にクリック **はい**です。
    
    ![](media/production_CheckpointName.png)
    
10. VMConnect を閉じます。
    VM が実行を継続、するだけに接続されませんがこれ以上。
11. HYPER-V マネージャーでは、チェックポイントの一覧は次のようになりますようになりました。
    
    ![](media/production_complete.png)



##標準のチェックポイントを適用します。

1.   **HYPER-V Manager**, の **チェックポイント** セクションで、」というタイトルの 1 つを右クリックし、 **標準** ] をクリック **適用**です。
2.  ポップアップ ダイアログ ボックスで、次のようにクリックします。 **およびチェックポイントの作成と適用**です。
    

    ![](media/apply_standard.png)
34. ときに、完了したら、チェックポイントの一覧を次のようになります。
    
    ![](media/standard_applied.png)
4. これが完了すると、右クリック] をクリックし、VM **接続** 、VM に接続します。
    
5. VM に接続するときに、メモ帳を開くと、VM を実行する必要が、実稼働のチェックポイントについて行は失われます。
    
    ![](media/standard_applied_notepad.png)
6. VMConnect の場合を終了し、実行中の VM のままです。


##実稼働のチェックポイントを適用します。

HYPER-V マネージャーに戻りましょう、実稼働のチェックポイントを適用して、仮想マシンを後で表示する方法を参照してください。 ここで、します。

1.  [チェックポイント] セクションでは、」というタイトルの 1 つを右クリックし **運用チェックポイント** ] をクリック **適用**です。
2.  ポップアップ ダイアログ ボックスで、次のように選択します。 **およびチェックポイントの作成と適用**です。
    
3. これが完了すると、右クリック] をクリックし、VM **接続** 、VM を起動します。
    
4. VM が実行されていないことがわかります。
    クリックして、 ![](media/start.png) VM を起動するには、メニュー バーで、[スタート] ボタン。
5. メモ帳で開いている test.txt を開きます。
    テストの実稼働のチェックポイントは、ファイル内の行が表示されます。
    
    ![](media/production_notepad.png)


##チェックポイントの名前を変更します。

1. ツリーで、前回のチェックポイントを右クリックし、[名前の変更] をクリックします。
2. チェックポイントの名前を付けます **削除**です。
    
    ![](media/delete_me.png)

##チェックポイントを削除します。

前の手順の次にやってみましょうについてのヒントを指定した可能性があります。
名前を変更したチェックポイントを削除しようとしています。

1. という名前のチェックポイントを右クリックして **削除** ] をクリック **Delete チェックポイント**です。
    

    ![](media/delete_checkpoint.png)
2. [警告] ダイアログ ボックスで、次のようにクリックします。 **削除**です。
    

    ![](media/delete_warn.png)
3. チェックポイントが削除されると、一覧は次のようになります。
    
    ![](media/after_delete.png)


##次の手順:

[手順 7: をエクスポートし、仮想マシンをインポートします。](walkthrough_export_import.md)





