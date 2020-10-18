## 今日は missing scripts: start と闘いました…負けました…

最初はgithubのrepoに追加したREADME.mdがlocal領域にないってとこからエラーになりました
検索したらcloneをダウンロードしてターミナルでpull(?) merge(?)してもう一回pushすればいいって書いてました
その通りにやってみました
まささんにも連絡したりして何とかpushまでは終わりました

その後の段階のpackage.jsonの修正 （"homepage", "predeploy", "deploy"の追加）でまた問題になりました
package.jsonがpackage-lock.jsonになって修正できなくなちゃったんです T-T
しかもサイトによって "predeploy"と　"deploy"の設定が違って
私みたいに何もわからずコピペしてる人には意味がもるげそよでした






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
  
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

なかなか治らなくて検索していろいろやってみる！を何度も繰り返してたら
知らない間にreactのprojectが入ってるfileが勝手にcopyされ2つになってたり
project folderの中身がバラバラになって上位のfolderに飛んでたり
node modulesが消えたりbranchの名前を間違えて中身が混ざったり………T-T　ぐちゃぐちゃになっちゃいました　（ここまで4時間ぐらいかかりました…自分がバカすぎてホントに悲しい気持ちになりました）

ぐちゃぐちゃすぎて全部最初からやり直そう！と思い…どじょんどじょんしてた途中…
npm start をうったら　missing scripts: start　というエラーが発生しました…
検索したらこれは package.jsonの中の "sripts"の"start"部分が抜けてるか

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/MinjiKinn/blog/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
