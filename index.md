## 今日は missing scripts: start と闘いました…負けました…

最初はgithubのrepoに追加したREADME.mdがlocal領域にないってとこからエラーになりました<br />
検索したらcloneをダウンロードしてターミナルでpull(?) merge(?)してもう一回pushすればいいって書いてありました<br />
その通りにやってみました<br />
まささんにも連絡したりして何とかpushまでは終わりました<br />

その後の段階のpackage.jsonの修正 （"homepage", "predeploy", "deploy"の追加）で、また問題になりました<br />
package.jsonがpackage-lock.jsonにかわって修正できなくなちゃったんです T-T<br />
しかもサイトによって "predeploy"と　"deploy"の設定が違って<br />
私みたいに何もわからずコピペしてる人には意味がもるげそよでした<br />


### T-T

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown


# まささんが教えてくれたサイト

...
  "scripts": {
    ...
    "predeploy" : "yarn run build",
    "deploy": "gh-pages -d build"
    ...
  },
  ...
  "homepage": "https://{githubユーザー名}/{リポジトリ名}",
  ...
  
## 他のサイト

"scripts":{ 
  "predeploy": "react-scripts build", 
  "deploy": "gh-pages -d build", 
}

### また他のサイト

"scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "deploy": "gh-pages -b master -d build",
    "predeploy": "npm run build" (혹은 yarn build)
  }
  
```

頑張ってもなかなか治らなくて検索して何かうつのを何度も繰り返してたら<br />
知らない間にreactのprojectが入ってるfileが勝手にcopyされ2つになってたり<br />
project folderの中身がバラバラになって下位のfolderに飛んでたり<br />
node modulesが消えたりbranchの名前が被っちゃって中身が混ざってたり………T-T　ぐちゃぐちゃになっちゃいました　（ここまで５時間ぐらいかかりました…自分がバカすぎてホントに悲しい気持ちになりました）<br />

もう
ぐちゃぐちゃすぎて全部最初からやり直そう！と思い…どじょんどじょんしてた途中…<br />
npm start をうったら　missing scripts: start　というエラーが発生しました…<br />
検索したらこれは package.jsonの中の "sripts":"start"の部分が抜けてるか何かおかしいか…が原因だとみんな言ってました<br />
でももういろいろやってる中package.jsonもnode modulesも(多分他に大事なものも何個か)消され…<br />
startできなくてnpm installのやり直しもできず……(これが正解だったのかはわかりませんT-T)<br />
結局検索しても何も手を出せない状況になってしまいました　（もう夜…悲しすぎて泣きました…マジ首にしてください…）<br />

npm startできないとreactを立ち上げるのもできなくて…<br />
しかたなくまた最初からやり直しました<br />
今回は最初の宿題と今回の宿題が入ってるdirectoryじゃなくて<br />
全然無関係な遠いfolderにdirectoryを作ってcreate reactを最初からやり直したら<br />
！！！何かうまくいきました！<br />

そっから<br />
新しいとこに宿題をうつしてもう一度githubにpushしました<br />
今回はスムーズにできました！<br />
package.jsonの修正も何とかできました！<br />
最後のnpm run deployでちょっと迷ったんですけど（上で言ったdeployなんちゃらがサイトによって違ってT-T)<br />
最後の段階までやってやっと何かいい感じの赤くない文字が出てきました（ターミナルに…）<br />

あとは住所とか設定して<br />
https://minjikinn.github.io/homework2/<br />
これになりました…<br />
でもまたなんかエラー404が出たり…react appって表示されてるのに中身は何も映らなかったり<br />
homework2っていうrepoの名前だけ出てきたりしてます………<br />



### 1日無駄にしてほんとにすみません…


読んでてあきれましたよね………<br />
本当にこんな人間に給料やるのもったいないんで<br />
いつでも首にしてください………<br />
html css bootstrap…他にやることいっぱいなのにT-T<br />
先週の宿題のやつも…mobileのサイズで作っててまだPCのサイズに反応するように作る方法とかわからないし…早くやらなきゃいけないのに…<br />
バカでごめんなさい…頑張ります…………<br />



### 宿題早く提出したいんですけど今hosting pageが…

宿題はもう土曜の夕方に終わってるんですけど
terminalとgithubとの戦いが終わらなくて……
https://minjikinn.github.io/homework2/<br />
の後ろにApp.jsとかつけてもcodeしか見えないです T-T<br />
どうすればいいですかㅠㅠㅠㅠㅠㅠㅠㅠㅠㅠㅠㅠㅠㅠㅠㅠㅠㅠ<br />


