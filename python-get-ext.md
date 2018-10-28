title=pythonで拡張子を取得する
slug=python-get-extn
tags=[python]
ファイルの拡張子を取得する方法をいつも忘れるのでメモ

```python
import os
file_path = "hoge/test.md"
root, ext = os.path.splitext(file_path)
print(root, ext)
```

出力

```
hoge/test .md
```
