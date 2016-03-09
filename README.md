# textlint-isssue78

This repository reproduce textlint/issues/78 

- https://github.com/textlint/textlint/issues/78

## Problem

Duplicated error messages caused by file order.

## Installation

  npm install

## Usage

`npm run textlint` reproduce the bug.

```
$ npm run textlint
DEBUG=textlint* npm run textlint

> textlint-isssue78@1.0.0 textlint /Users/azu/.ghq/github.com/azu/textlint-isssue78
> textlint --plugin textlint-plugin-jtf-style index.md README.md

  textlint:cli Running on files +0ms
  textlint:cli-engine config %O +167ms Config {
  configFile: undefined,
  rulesBaseDirectory: undefined,
  rules: [],
  plugins: [ 'textlint-plugin-jtf-style' ],
  rulesConfig:
   { 'textlint-plugin-jtf-style/2.1.9.アルファベット': true,
     'textlint-plugin-jtf-style/4.2.8.セミコロン(;)': true,
     'textlint-plugin-jtf-style/1.2.1.句点(。)と読点(、)': true,
     'textlint-plugin-jtf-style/4.2.4.中黒(・)': true,
     'textlint-plugin-jtf-style/1.1.1.本文': true,
     'textlint-plugin-jtf-style/4.1.3.ピリオド(.)、カンマ(,)': true,
     'textlint-plugin-jtf-style/2.1.10.算用数字の位取りの表記': true,
     'textlint-plugin-jtf-style/4.2.9.ダッシュ(-)': true,
     'textlint-plugin-jtf-style/4.3.1.丸かっこ（）': true,
     'textlint-plugin-jtf-style/2.1.2.漢字': true,
     'textlint-plugin-jtf-style/2.2.1.ひらがなと漢字の使い分け': true,
     'textlint-plugin-jtf-style/3.3.かっこ類と隣接する文字の間のスペースの有無': true,
     'textlint-plugin-jtf-style/3.2.カタカナ語間のスペースの有無': true,
     'textlint-plugin-jtf-style/4.3.8.一重引用符': true,
     'textlint-plugin-jtf-style/4.3.6.中かっこ{ }': true,
     'textlint-plugin-jtf-style/2.1.8.算用数字': true,
     'textlint-plugin-jtf-style/1.1.2.見出し': true,
     'textlint-plugin-jtf-style/4.2.2.疑問符(？)': true,
     'textlint-plugin-jtf-style/2.2.3.一部の助数詞の表記': true,
     'textlint-plugin-jtf-style/3.1.1.全角文字と半角文字の間': true,
     'textlint-plugin-jtf-style/2.2.2.算用数字と漢数字の使い分け': true,
     'textlint-plugin-jtf-style/1.2.2.ピリオド(.)とカンマ(,)': true,
     'textlint-plugin-jtf-style/4.2.7.コロン(：)': true,
     'textlint-plugin-jtf-style/4.3.7.山かっこ<>': true,
     'textlint-plugin-jtf-style/2.1.5.カタカナ': true,
     'textlint-plugin-jtf-style/2.1.6.カタカナの長音': true,
     'textlint-plugin-jtf-style/1.1.3.箇条書き': true,
     'textlint-plugin-jtf-style/4.3.3.かぎかっこ「」': true,
     'textlint-plugin-jtf-style/1.1.5.図表のキャプション': true,
     'textlint-plugin-jtf-style/3.1.2.全角文字どうし': true,
     'textlint-plugin-jtf-style/4.2.1.感嘆符(！)': true,
     'textlint-plugin-jtf-style/4.1.1.句点(。)': true,
     'textlint-plugin-jtf-style/4.3.2.大かっこ［］': true,
     'textlint-plugin-jtf-style/4.3.5.二重引用符': true,
     'textlint-plugin-jtf-style/4.3.4.二重かぎかっこ『』': true,
     'textlint-plugin-jtf-style/4.2.5.波線(〜)': true,
     'textlint-plugin-jtf-style/4.2.6.ハイフン(-)': true },
  extensions: [],
  rulePaths: [],
  formatterName: 'stylish' }
  textlint:cli-engine Loading rules from plugin: /Users/azu/.ghq/github.com/azu/textlint-isssue78/node_modules/textlint-plugin-jtf-style/lib/index.js +7ms
  textlint:core use "jtf-style/1.1.1.本文" rule +2ms
  textlint:core use "jtf-style/1.1.2.見出し" rule +2ms
  textlint:core use "jtf-style/1.1.3.箇条書き" rule +0ms
  textlint:core use "jtf-style/1.1.5.図表のキャプション" rule +1ms
  textlint:core use "jtf-style/1.2.1.句点(。)と読点(、)" rule +0ms
  textlint:core use "jtf-style/1.2.2.ピリオド(.)とカンマ(,)" rule +1ms
  textlint:core use "jtf-style/2.1.2.漢字" rule +0ms
  textlint:core use "jtf-style/2.1.5.カタカナ" rule +0ms
  textlint:core use "jtf-style/2.1.6.カタカナの長音" rule +19ms
  textlint:core use "jtf-style/2.1.8.算用数字" rule +5ms
  textlint:core use "jtf-style/2.1.9.アルファベット" rule +1ms
  textlint:core use "jtf-style/2.1.10.算用数字の位取りの表記" rule +0ms
  textlint:core use "jtf-style/2.2.1.ひらがなと漢字の使い分け" rule +0ms
  textlint:core use "jtf-style/2.2.2.算用数字と漢数字の使い分け" rule +9ms
  textlint:core use "jtf-style/2.2.3.一部の助数詞の表記" rule +0ms
  textlint:core use "jtf-style/3.1.1.全角文字と半角文字の間" rule +1ms
  textlint:core use "jtf-style/3.1.2.全角文字どうし" rule +0ms
  textlint:core use "jtf-style/3.2.カタカナ語間のスペースの有無" rule +0ms
  textlint:core use "jtf-style/3.3.かっこ類と隣接する文字の間のスペースの有無" rule +1ms
  textlint:core use "jtf-style/4.1.1.句点(。)" rule +0ms
  textlint:core use "jtf-style/4.1.3.ピリオド(.)、カンマ(,)" rule +0ms
  textlint:core use "jtf-style/4.2.1.感嘆符(！)" rule +0ms
  textlint:core use "jtf-style/4.2.2.疑問符(？)" rule +1ms
  textlint:core use "jtf-style/4.2.4.中黒(・)" rule +0ms
  textlint:core use "jtf-style/4.2.5.波線(〜)" rule +0ms
  textlint:core use "jtf-style/4.2.6.ハイフン(-)" rule +28ms
  textlint:core use "jtf-style/4.2.7.コロン(：)" rule +0ms
  textlint:core use "jtf-style/4.2.8.セミコロン(;)" rule +1ms
  textlint:core use "jtf-style/4.2.9.ダッシュ(-)" rule +0ms
  textlint:core use "jtf-style/4.3.1.丸かっこ（）" rule +0ms
  textlint:core use "jtf-style/4.3.2.大かっこ［］" rule +0ms
  textlint:core use "jtf-style/4.3.3.かぎかっこ「」" rule +0ms
  textlint:core use "jtf-style/4.3.4.二重かぎかっこ『』" rule +1ms
  textlint:core use "jtf-style/4.3.5.二重引用符" rule +0ms
  textlint:core use "jtf-style/4.3.6.中かっこ{ }" rule +0ms
  textlint:core use "jtf-style/4.3.7.山かっこ<>" rule +0ms
  textlint:core use "jtf-style/4.3.8.一重引用符" rule +0ms
  textlint:find-util Processing index.md +1ms
  textlint:find-util Processing README.md +0ms
  textlint:core
Processor : MarkdownProcessor
text:
もっとです。
もっとする。もっとだ。
ext : .md
filePath: /Users/azu/.ghq/github.com/azu/textlint-isssue78/index.md
 +1ms
  textlint:rule-context-agent pushReport 9:1:<RuleError>本文を敬体(ですます調)に統一して下さい。
本文の文体は、敬体(ですます調)あるいは常体(である調)のどちらかで統一します。
"だ。"が常体(である調)です。 @:1:9: +55ms
  textlint:core
Processor : MarkdownProcessor
text:
ext : .md
filePath: /Users/azu/.ghq/github.com/azu/textlint-isssue78/README.md
 +1ms
  textlint:rule-context-agent pushReport 9:1:<RuleError>本文を敬体(ですます調)に統一して下さい。
本文の文体は、敬体(ですます調)あるいは常体(である調)のどちらかで統一します。
"だ。"が常体(である調)です。 @:1:9: +3ms

/Users/azu/.ghq/github.com/azu/textlint-isssue78/index.md
  3:10  error  本文を敬体(ですます調)に統一して下さい。
本文の文体は、敬体(ですます調)あるいは常体(である調)のどちらかで統一します。
"だ。"が常体(である調)です。  jtf-style/1.1.1.本文

/Users/azu/.ghq/github.com/azu/textlint-isssue78/README.md
  3:10  error  本文を敬体(ですます調)に統一して下さい。
本文の文体は、敬体(ですます調)あるいは常体(である調)のどちらかで統一します。
"だ。"が常体(である調)です。  jtf-style/1.1.1.本文

✖ 2 problems (2 errors, 0 warnings)
```

## License

MIT
