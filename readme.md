# React講座のメモ

## 目標
- Reactの基礎知識を得る
- Hooksを用いた記法で開発をすることができる
- Reactで簡単なチャットアプリを作ることができる

## 基礎知識
ReactはFacebook社が開発したUiライブラリで現在はOSS. UIを作るためのコンポーネント(見た目+機能)という概念が特徴的で, コンポーネントを組み合わせてwebの画面を作っていく.  
従来のHTMLでは, HTML(ツリー構造のドキュメント)を画面に描画する. ツリー構造を変更するときはDocument Object Model(DOM)からアクセスを行う. ただしDOMを直接変更してHTMLを再描画する処理はコストが高いという問題点がある. Reactでは仮想DOMと呼ばれる仕組みを用いてこの問題点を解決している. 仮想DOMでは, ブラウザのDOMツリーはJavaScriptのオブジェクトとして扱うことでブラウザに負荷をかけずにJavaScriptエンジンのメモリを使うことができ, 効率の良い再描画(レンダリング)を行うことがこのような仕組みの目標である. またDOMの状態をJavaScriptで管理することができる(=コンポーネント). レンダリングには差分描画という仕組みが用いられている. 従来のHTMLの場合, ツリー構造の1箇所が更新されると全体をレンダリングしていたが, 仮想DOMを用いると更新された箇所に関係する箇所のみを書き換えることでレンダリングの処理を軽量化している. 