1. 初期化
```
(/scoreboard objectives add bdi dummy BDI)
/scoreboard players set @p bdi 0
/title @p times 0 220 0
```
2. 設問と選択肢の表示
/titleraw @p subtitle {"rawtext":[{"text":"a: 憂うつではない\nb: 憂うつである\nc: いつも憂うつから逃れることができない\nd: 耐えがたいほど、憂うつで不幸である"}]}
```
/title @p title 1.
/title @p actionbar 10 (delay 20)
/title @p actionbar 9 (delay 20)
/title @p actionbar 8 (delay 20)
/title @p actionbar 7 (delay 20)
/title @p actionbar 6 (delay 20)
/title @p actionbar 5 (delay 20)
/title @p actionbar 4 (delay 20)
/title @p actionbar 3 (delay 20)
/title @p actionbar 2 (delay 20)
/title @p actionbar 1 (delay 20)
/title @p actionbar 0 (delay 20)
```
3. 看板もしくはランプの形 (0-3や◎○△×など) に従った選択肢を選択し (0-3) の点を変数へ加算していく。 
```
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 5 title @p actionbar aを選択しました。
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 1 title @p actionbar bを選択しました。
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 1 scoreboard players add @p bdi 1
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 8 title @p actionbar cを選択しました。
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 8 scoreboard players add @p bdi 2
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 14 title @p actionbar dを選択しました。
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 14 scoreboard players add @p bdi 3
```
4. 2と3のループを設問数分だけ行い合計点を得る。
5. 合計点を元に6段階でうつの程度を分類して結果に応じて色の違うブロックをコマンドブロック実行者に渡す。
```
/give @p[scores={bdi=0..10}] wool 1 13 (緑)
/give @p[scores={bdi=11..16}] wool 1 5 (黄緑)
/give @p[scores={bdi=17..20}] wool 1 4 (黄色)
/give @p[scores={bdi=21..30}] wool 1 1 (オレンジ)
/give @p[scores={bdi=31..40}] wool 1 14 (赤)
/give @p[scores={bdi=41..}] wool 1 14 (赤)
```