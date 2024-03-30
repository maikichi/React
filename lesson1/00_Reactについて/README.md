## Reactとは
・Reactは、サイトの見た目を作ることができるJavaScriptのライブラリ<br>
・さらに、Reactのモバイル版であるReact Nativeを使うと、iOSとAndroid両方のスマートフォンアプリを作ることができる

### ブラウザに表示する
・App.jsというファイルのrenderメソッドのreturn内に、< h1>Hello World< /h1>と記述すると、ブラウザに「Hello World」と表示される<br>
・return以外にも色々書いてあるが、いまはApp.jsのreturnの中で記述するということだけ覚えておけばOK

```rb
[App.js]
class App.extends React.Component {
    render() {
        return (
            <h1>Hello World</h1>
        );
     }
}
```

### ① JSX（JavaScript XML）の書き方
・JSXは、HTMLとほとんど同じように記述することができる<br>
・見出しには< h1>タグや< h2>タグ、文章には< p>タグ、その他< div>タグなど、HTMLと同様のタグが使えるようになっている

```rb
[App.js]
render() {
  return {
     <div>
       <h1>h1です</h1>
       <h2>h1です</h2>
       <p>h1です</p>
     </div>
 );
}
```

### ② JSXの注意点⚠️

・JSXはほとんどHTMLと同じだが、いくつか違いがある<br>
・return内に複数の要素があるとエラーになる<br>
・複数の要素がある場合は、< div>タグで囲んで、1つの要素にまとめてあげる<br>

### ③ JSXのコメント
・JSXを {/* */} で囲むと、その部分はコメントになる<br>
・コメントにすると、そのJSXは表示されない<br>
・正しくコメントにできている場合は、囲んだ部分が灰色になる

```rb
[App.js]
render() {
  return (
    <div>
       {/*この部分はコメントです*/}
    </div>
  );
}
```

### imgタグの注意点
・imgタグは、HTMLでは、< img src='画像のURL'>のように閉じタグが必要なかったが、JSXでは閉じタグが必要<br>
・< img src='画像のURL' />のように、タグの終わりにスラッシュ「/」を記述
・ダブルフォート「”」ではなく、シングルクォート「’」

```rb
[App.js]
render() {
  return (
    <img src='https://prog-8.com/family.jp'/>
  );
}
```

### App.jsの構成
・App.jsを作成する時はいつもこのように書くので、丸暗記する必要はない

```rb
[App.js]
import React from 'react';
class App extends React.Component {
  render(){
    return (
      <h1>Hello React</h1>
    );
  }
}
export default App;
``` 
