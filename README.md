# libskk用の設定
## sticky shiftのための設定
libskkのソースコードに含まれるtest-stickyを改変したもの

sticky shiftのデフォルトプレフィックスキーは「変換」に変更している。
これは`keymap/hiragana.json` の中で変更可能

### 参考URL
- https://uwabami.junkhub.org/log/20141025.html

## ローマ字かな変換テーブルの改造

かな入力時の挙動の変更
- 「!」を押した時に全角の「！」が出るようにした
- 「z8」あるいは「z9」で全角の「（」「）」が出るようにした
  - 本来は「z(」「z)」で出るはずなのだが、
    不具合があるためか半角の「(」「)」が出てしまう
- `rom-kana/default.json`に追記することでカスタマイズ可能

参考URL
- https://typeinf-memo.blogspot.com/2017/08/fcitx-skk_10.html

## インストール
```bash
cd $HOME/.config/libskk/rules

git clone git@github.com:toshi-ara/test-sticky.git
 or
git clone https://github.com/toshi-ara/test-sticky.git
```

