# RM_CurveMorph
- **RM_CurveMorph**は3DCGソフトBlenderのジオメトリーノード製のツールです。カーブオブジェクトにモディファイヤとして適用し、指定したオブジェクトをカーブに沿って変形します。
<img src="images/0095802bfab25be357368e3db10e0d3640cc97bf8505afe8b6a9a9f978e74d30.png" width=70%/>

### 動作バージョン
- Blender 4.0.0以降

### アセットライブラリへの登録方法
- **RM_CurveMorph**はBlenderのジオメトリーノード製です。そのためアセットライブラリに登録して使用するといいでしょう。

- GithubのRM_CurveMorphのページからzipファイルをダウンロードし、解凍します
<img src="images/c4b3b8e518e54b3692d4df3242e4390005a7fccb83d464b70f204c32136eaf74.png" width=70%/>

- Blenderの【プリファレンス】→【ファイルパス】→【アセットライブラリ】を開いてください。アセットライブラリとして使用できるフォルダパスが確認できます。このフォルダパスに先ほど解凍した中から「RM_TOOL」フォルダをコピーします。
<img src="images/1a12f693c34850dae32a3567cb73ea84a97095868f4e5d3949fd625dce664d06.png" width=70%/>  
<img src="images/28e52335b353a367dd9ce56334b72697c0090bafeaeb56da0e19aef7e338d9bf.png" width=70%/>  

- Blenderを再起動してアセットライブラリを表示するとRM_TOOLの項目があり、その中にRM_CurveMorphのほかサンプル用のメッシュが入っていればアセットライブラリへの登録は成功です。
<img src="images/169623afdbccaf5d1190f581229acb3325d93a2a0db3560f5def13a289b32a54.png" width=70%/>  

### 使用方法
- アセットライブラリへの登録が済んでいれば、カーブオブジェクトのモディファイアの一覧の中にRM_CurveMorphが表示されているので、モディファイアとして選択してください。
<img src="images/13799e6683d81ef150a6eb00838b7ef586240a0a1635d0cc45211c3cdffb3cc5.png" width=70%/>  



### 設定項目
- RM_CurveMorphの設定項目と効果は次になります

|項目|効果|
|---|---|
|Source Mesh|変形するメッシュオブジェクトを指定します|
|Source Mesh Rotation X・Y・Z|変形前にメッシュオブジェクトを回転します<BR>先の画像のように-Zを向くオブジェクトはX 90°, Y 0°, Z -90° にすると良いでしょう|
|Source Mesh Position LR・UD|カーブの軸に対してメッシュオブジェクトの位置を左右上下方向に移動します|
|Source Mesh Scale Width・Height| メッシュオブジェクトの幅と高さをそれぞれ変更します|
|Curve Start・End|カーブの長さを変更します|
|-x**2・Linear・1-x\*\*2|メッシュの中央が山となるように変形します|
|Material Change|マテリアルを変更するか選択します|
|Material|Material Changeにチェックを入れた場合、ここで指定したマテリアルが適用されます|
|UV Map Name|ここで名前指定したUVマップの位置を変更することができます<BR>初期値は"UVMap"です|
|UV Slide U・V|UV Map Nameで名前指定したUVマップの位置をずらします|

<img src="images/38d5f1625ae66b9aa60dd5fab30135bc93cb4a9bfa19a7c60c536684b11a5301.png" width=70%/>

### 注意事項
- メッシュの適用問題(Blender4.0で確認)
  - 問題
    - おそらくRM_CurveMorphを使う全員が直面します
    - RM_CurveMorphで作成したオブジェクトを適用する際にエラーが起こります
    - RM_CurveMorphはカーブオブジェクトからメッシュデータを作るものですが、Blender内の処理では外見上はカーブオブジェクトのままです。そのためカーブオブジェクトの中にメッシュデータがあり、通常の変換処理ができずエラーとなっていると予想されます
    - <img src="images/da53ce4210d606372f1e6d215ce55a82967626ddd88c8e2ebc18d1cc524651b9.png" width=70% />
  - 解決方法
    - メニューの「オブジェクト」→「変換」→「メッシュ」を選択するとメッシュへ変換されます
    - <img src="images/1c7111bd8a8ab010810b37a2ee3b9f7af2d26533052c88f601bca59fd550beaa.png" width=70% />

### バグ報告・機能追加要望についてのお願い
- 使用中にバグを発見した際・追加機能の要望があればぜひ作者までご連絡ください。それぞれご対応いたします。

### 更新履歴
- 2024/02/20 Source Mesh Scale機能とSouce Mesh Position機能を同時使用した場合にSouce Mesh Position機能がききづらくなるバグを修正
- 2024/02/14 Source Mesh Scale機能追加・UV Slide修正
- 2024/02/10 Githubに公開

### 免責事項
- 本ツールは、使用者の責任にて使用することを前提として提供されます。本ツールの妥当性や結果に関する判断は使用者が行うべきものであり、著作権者は使用結果に関して何らの保証をするものではなく、どのような形でも責任を負いません。著作権者は本ツールの仕様、もしくは使用不能に起因して生じた利益の損失、障害、その他の金銭的な損害を含め、いかなる特定の偶発的、間接的、もしくは派生的損害についても責任を負いません。