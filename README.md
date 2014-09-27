JuliaTokyo #2 導入セッション
============

JuliaTokyo #2 の導入セッション用資料です。http://juliatokyo.connpass.com/event/8010/

説明には、IJulia notebookを使いました。

## Julia本体のインストール

[公式サイト](http://julialang.org/downloads/)で、安定版および開発版（Nightly builds）のバイナリが、Windows、Mac OS X、Ubuntu向けに用意されています。

Max OS XのhomebrewやDebianのaptといったパッケージ管理システムに登録されている場合もありますが、バージョンが最新安定版より古い可能性もあるので注意が必要です。

このチュートリアル実施時の最新安定版は、2014年8月に公開された **v0.3** です。以前のバージョンと一部互換性のない部分もありますので、ご注意ください。

バイナリを実行すると、標準REPLが起動します。

```
$ julia # Juliaを起動
               _
   _       _ _(_)_     |  A fresh approach to technical computing
  (_)     | (_) (_)    |  Documentation: http://docs.julialang.org
   _ _   _| |_  __ _   |  Type "help()" for help.
  | | | | | | |/ _` |  |
  | | |_| | | | (_| |  |  Version 0.3.0 (2014-08-20 20:43 UTC)
 _/ |\__'_|_|_|\__'_|  |  Official http://julialang.org/ release
|__/                   |  x86_64-apple-darwin13.3.0

julia>

```

## IJuliaのインストール
まず、iPythonをインストールする必要があります。色々なPythonのライブラリをまとめてインストールしてくれる[Anaconda](http://continuum.io/downloads)を使うと便利です。

次に、JuliaのREPLから
```
Pkg.add("IJulia")
```
とすると、IJuliaをインストールできます。


エラーの場合は
```
Pkg.update("IJulia")
```
や
```
Pkg.build("IJulia")
```
を試してみてください。


IJuliaがインストールされると、シェルから
```
$ ipython notebook --profile julia
```
と実行するか、JuliaのREPLから
```
julia> using IJulia
julia> notebook()
```
とすることでIJulia notebookを起動できます。
