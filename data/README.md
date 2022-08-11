# nowt36lp

## 発注するためのデータの作り方

1. (horizon プラグイン)[https://github.com/skarrmann/horizon]を KiCAD に入れる
2. `revX` (`rev0.1` や `rev0.2` など) 内の `pcb/nowt36lp.kicad_pcb` を開く
3. horizon プラグインを使って、発注するためのデータを作成する

## horizon プラグインの使い方

### もととなるKiCADのデータの作成方法

ボトムプレートとトッププレートを生成するためのデータはレイヤごとに作成されます

* `F.Adhesive` レイヤ：トッププレートの穴とEdge.Cuts
* `B.Adhesive` レイヤ：ボトムプレートの穴とEdge.Cuts


### horizon プラグインを使用して、ボトムプレートとトッププレートのデータを生成する

PCBエディタを開き、ツール > 外部プラグイン > Horizon Board Productor を実行する。

正しく実行できた場合、`data/` ディレクトリに `temp` と `gerbers` が生成される。

`temp` は KiCAD プロジェクトで、`gerbers` は JLCPCB (のみ？) に発注できるデータ。

`temp` を修正し、ガーバーファイルを生成して、発注することも可能


