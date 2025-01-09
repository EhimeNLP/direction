# direction
犬型ロボットとの対話を考慮した対話データセットを構築した。<br>
クラウドソーシングサービスの [lancers](https://www.lancers.jp/) にて、人間の発話文と犬型ロボットの応答文・犬型ロボットの動作の3つ組コーパスを収集した。<br>
犬型ロボットは [unitree go2](https://www.unitree.com/go2) を想定している。<br>


## データ数
| train | valid | test  |
| ----- | ----- | ----- |
| 6,000 | 1,000 | 1,000 |


## データ説明
`train/valid/test \t ユーザコード \t 発話文 \t 応答文 \t 動作` の形式で記述されている。<br>
- ユーザコード：データ構築に協力してもらった方に番号を振っており、0~60まで存在する。（0：800件、その他：120件）<br>
- 動作： [unitree go2](https://www.unitree.com/go2) の11種類の動作から8種類を設定した。<br>（「1. stretch」、「2. shake hands」、「3. jump forward」、「4. cheer」、「5. punch」、「6. sit down」、「7. standing up」、「8. dance」）<br>
- 各動作が均等に分かれるように割り振られている。（train：750件ずつ、valid, test：125件）<br>

```
train	0	公園の空気っていいね。	公園の空気は清々しくて気持ちいいよね！	1. stretch
train	0	今日は自分へのご褒美にスパに行くつもりだよ。	それはいいね！気持ちよさそう！	1. stretch
train	0	旅行がとっても楽しかったよ！異国の空気が新鮮だった！	異国の空気に触れると、心もリフレッシュするよね！	1. stretch
train	0	運動をした後は体が軽く感じるよね。	体がスッキリして気持ちがいいよね！	1. stretch
train	0	今日は早めに寝ようかな。	しっかり休息するのは大事だよね！	1. stretch
```
