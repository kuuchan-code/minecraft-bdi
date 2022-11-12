0. 初期化
/scoreboard players set @p bdi 0
/title @p times 0 220 0
1. 設問と選択肢の表示
/titleraw @p subtitle {"rawtext":[{"text":"a: 憂うつではない\nb: 憂うつである\nc: いつも憂うつから逃れることができない\nd: 耐えがたいほど、憂うつで不幸である"}]}
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
2. 看板もしくはランプの形 (0-3や◎○△×など) に従った選択肢を選択し (0-3) の点を変数へ加算していく。 
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 5 title @p actionbar aを選択しました。
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 1 title @p actionbar bを選択しました。
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 1 scoreboard players add @p bdi 1
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 8 title @p actionbar cを選択しました。
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 8 scoreboard players add @p bdi 2
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 14 title @p actionbar dを選択しました。
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 14 scoreboard players add @p bdi 3
3. 1. から2. までのループを設問数分だけ行い合計点を得る。
4. 合計点を元に6段階でうつの程度を分類して結果に応じて色の違うブロックをコマンドブロック実行者に渡す。
/give @p[scores={bdi=0..10}] wool 1 13 (緑)
/give @p[scores={bdi=11..16}] wool 1 5 (黄緑)
/give @p[scores={bdi=17..20}] wool 1 4 (黄色)
/give @p[scores={bdi=21..30}] wool 1 1 (オレンジ)
/give @p[scores={bdi=31..40}] wool 1 14 (赤)
/give @p[scores={bdi=41..}] wool 1 14 (赤)










/titleraw @p subtitle {"rawtext":[{"text":"a: 将来について悲観してはいない\nb: 将来について悲観している\nc: 将来に希望がない\nd: 将来に何の希望もなく、良くなる可能性もない"}]}
/title @p title 2.
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
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 5 title @p actionbar aを選択しました。
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 1 title @p actionbar bを選択しました。
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 1 scoreboard players add @p bdi 1
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 8 title @p actionbar cを選択しました。
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 8 scoreboard players add @p bdi 2
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 14 title @p actionbar dを選択しました。
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 14 scoreboard players add @p bdi 3

/titleraw @p subtitle {"rawtext":[{"text":"a: それほど失敗するようには感じない\nb: 普通より、よく失敗するように思う\nc: 過去のことをふりかえれば、失敗のことばかり思い出す\nd: 人間として全く失敗だと思う"}]}
/title @p title 3.
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
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 5 title @p actionbar aを選択しました。
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 1 title @p actionbar bを選択しました。
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 1 scoreboard players add @p bdi 1
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 8 title @p actionbar cを選択しました。
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 8 scoreboard players add @p bdi 2
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 14 title @p actionbar dを選択しました。
/execute @p ~ ~ ~ detect ~ ~-1 ~ wool 14 scoreboard players add @p bdi 3
