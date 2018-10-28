title=Hugoの記事にdescriptionを追加する
slug=hugo-add-site-description
tags=[Hugo]

Hugoで書いた記事が検索で引っかからないなと思っていたら、descriptionタグが設定されていませんでした。
なので、descriptionタグをつけていきます。

次のようにすると、markdownに書いたdescriptionが参照できます。

```
{{ .Description }}
```


これまで書いた記事全てに、descriptionをつけていくのは面倒ですね。
次のようにサイトサマリーを参照することも可能です

```
{{ .Summary }}
```

結局、header.htmlなどに次のように書いておけばおkです。

```html
{{ if .Description }}
<meta name="description" content="{{ .Description }}">
{{ else }}
<meta name="description" content="{{ .Summary }}">
{{ end }}
```
