## 今日は missing scripts: start と闘いました…負けました…

最初はgithubのrepoに追加したREADME.mdがlocal領域にないってとこからエラーになりました<br />
検索したらcloneをダウンロードしてターミナルでpull(?) merge(?)してもう一回pushすればいいって書いてました<br />
その通りにやってみました<br />
まささんにも連絡したりして何とかpushまでは終わりました<br />

その後の段階のpackage.jsonの修正 （"homepage", "predeploy", "deploy"の追加）でまた問題になりました<br />
package.jsonがpackage-lock.jsonになって修正できなくなちゃったんです T-T<br />
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

頑張ってもなかなか治らなくて検索して何かやってみるのを何度も繰り返してたら
知らない間にreactのprojectが入ってるfileが勝手にcopyされ2つになってたり
project folderの中身がバラバラになって下位のfolderに飛んでたり
node modulesが消えたりbranchの名前が被っちゃって中身が混ざってたり………T-T　ぐちゃぐちゃになっちゃいました　（ここまで５時間ぐらいかかりました…自分がバカすぎてホントに悲しい気持ちになりました）

もう
ぐちゃぐちゃすぎて全部最初からやり直そう！と思い…どじょんどじょんしてた途中…
npm start をうったら　missing scripts: start　というエラーが発生しました…
検索したらこれは package.jsonの中の "sripts"の"start"の部分が抜けてるか何かおかしいか…が原因だとみんな言ってました
でももういろいろやってる中package.jsonもnode modulesも(多分他に大事なものも何個か)消され…
startできなくてnpm installのやり直しもできず……(これが正解だったのかはわかりませんT-T)
結局検索しても手を出せない状況になってしまいました　（もう夜…悲しすぎて泣きました…マジ首にしてください…）

npm startできないとreactを立ち上げるのもできなくて…
しかたなくてまた最初からやり直しました
今回は最初の宿題と今回の宿題が入ってるdirectoryじゃなくて
全然無関係な遠いfolderにdirectoryを作ってcreate reactを最初からやり直したら
！！！何かうまくいきました！

そっから
新しいとこに宿題をうつしてもう一度githubにpushしました
今回はスムーズにできました！
package.jsonの修正も何とかできました！
最後のnpm run deployでちょっと



### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/MinjiKinn/blog/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
