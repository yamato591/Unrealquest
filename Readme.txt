こちらのReadmeではサンプルプロジェクトデータについて以下の項目を記載しています。ぜひ参加前にご一読ください。

    ・サンプル内容
    ・フォルダ構成
    ・各アセットの役割
    ・軽量版の変更箇所
    ・イベント参加者の方へ

【サンプル内容】
本サンプルは「アンリアルクエスト3 ～グレイマンとつくる5つのショー～」の参加者に向けて Unreal Engine 4.27.2 で制作されたバージョンもしくは 4.27.2 で制作したプロジェクトを Unreal Engine 5.0.1 にコンバートしたサンプルです。
SideScrollerテンプレートをベースとして左クリック or ゲームパッド右トリガーによる投球が実装されています。あなただけのサイドスクローラーゲームを作っちゃいましょう！

【フォルダ構成】
ContentBrowser
    Splash：プロジェクト起動時のスプラッシュ画像が格納されています。操作等は不要です。
    UnrealQuest2
        Animations：キャラクターアニメーション、アニメーションBPを格納しています。
        Blueprints：アンリアルクエスト用のGameMode、キャラクターBP、玉BPが格納されています。
        Maps：シンプルな形状で作成されたレベルが格納されています。
        Materials：使用しているマテリアルを格納しています。
        Meshes：ステージにて使用されている各種モデルデータを格納しています。
	Textures：利用しているテクスチャを格納しています。

【各アセットの役割】
ブループリント
    BP_GameMode：処理等は追加しておらず、Default Pawn Classを設定しています。
    BP_Player：Unreal Engine 4のSideScrollerテンプレートに付属しているBPに玉の投球処理、被ダメージ処理を追加しています。
    BP_Ball：プレイヤーの投球処理によって実際に投げられる玉です。ヒットした物に対してダメージ処理を行なうようになっています。
　　　ABP_ThirdPerson:SideScrollerテンプレートに含まれるアニメーション ブループリントをベースに投球用のアニメーションロジックを追加しています。

レベル(マップ)
    SideScrollerExampleMap：SideScrollerテンプレートに付属するマップです。

【軽量版の変更箇所】
今回ダウンロードされたプロジェクトが「UnrealQuest3_UE(エンジンバージョン)_Light」だった場合。通常のプロジェクトデータと違い開発にてPCへかかる負荷を落とすため設定の変更を行っています。
以下に変更を行っている設定を列挙しています。

プロジェクト設定 > ターゲットハードウェア
    ・Target Hardware：モバイル/タブレット、スケーラブルな3D・2D

Viewport > 左上のメニュー
    ・リアルタイム：オフ

ツールバー > 設定
    ・エンジンの拡張機能設定：中
     [projectpath]/config/DefaultEngine.ini の [ConsoleVariables] セクションに設定している9項目が該当設定です。
     エディター上にて設定を変更する場合は.iniファイルの設定が優先されるため、ファイル上から [ConsoleVariables] セクションの9項目を削除した上で変更してください。

    ・マテリアルの品質レベル：低
     [projectpath]/config/DefaultEngine.ini の [ConsoleVariables] セクションに設定しています。

    もし軽量版を利用しても動作が重い場合は以下をお試しください。
    ・エンジンの拡張機能設定：低
    ・描画レベルをプレビュー：Android ES3.1(※シェーダーコンパイルが多く走ります。)

コンテンツブラウザ > 表示オプション
    ・リアルタイムサムネイル：オフ

FPS上限を60FPSに設定
    ・[projectpath]/config/DefaultEngine.ini の [/Script/UnrealEd.EditorEngine] セクションに設定しています。
    もしもFPS上限を固定したくない場合は該当セクションをまるごと削除してください。

プラグイン
    VR系などデフォルトで不要なプラグインのいくつかを無効化しています。具体的なリストはプロジェクトフォルダ上の「UnrealQuest3.uproject」をテキストエディターで開くことで確認できます。

UE5版のみ
    プロジェクト設定
        Rendering -> Dynamic Global Illumination Method：None
        Rendering -> Reflection Method:None
        Rendering -> Shadow Map Method:Shadow Maps

▼参考資料
    ・UE4 Editor軽量化 改訂版 | PaperSloth’s diary
    https://papersloth.hatenablog.com/entry/UEAC_2020

    ・[UE4] Editorのイテレーションを早くするTips (Editor起動/LevelOpen/PIE) | Qiita
    https://qiita.com/donbutsu17/items/be66551c48360d7b0864

　　　・[UE4]ConsoleVariables.iniの特殊性
　　　https://qiita.com/EGJ-Takashi_Suzuki/items/07ef02bf6eb08cdc1664

    ・拡張性のリファレンス
    https://docs.unrealengine.com/4.26/ja/TestingAndOptimization/PerformanceAndProfiling/Scalability/ScalabilityReference/

【イベント参加者の方へ】
クエストの取り組み方などで躓いたり、わからないことがあればぜひDiscordサーバーの #質問部屋01、#質問部屋02 チャンネルにてご質問ください！皆さんの仲間が助けてくれるかもしれません！
その他、レギュレーションなど本イベントについてわからないことがあれば #ご質問 チャンネルよりご質問ください。

「アンリアルクエスト3 ～グレイマンとつくる5つのショー～」イベントページはこちら
https://www.unrealengine.com/ja/events/how-to-join-unrealquest3