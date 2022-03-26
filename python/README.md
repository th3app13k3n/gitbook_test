# Python

## リスト内包表記

実行速度が普通のfor文より早い.  普通のfor文は以下が発生するため遅い.\
1\. リストからappend属性の取り出し．\
2\. python関数としてappendを実行．

```
# img_size_txt
07 322 18 779 990
13 1283 78 1815 1050
12 101 51 547 1023
...
```

```python
with open(img_size_txt, 'r') as size_txt:
    imgsize_list = size_txt.readlines()



# imgsize_list(=s)の行の内，s.split()[0]がstmimg_numに一致する行を取り出す．

# 1.リスト内包表記でないループ
line = []
for s in imgsize_list:
    if s.split()[0] == stmimg_num:
        line.append(s)

# 2.リスト内包表記
line = [ s for s in imgsize_list if s.split()[0] == stmimg_num ]
```

## アノテーション

numsの型はList\[int]で、targetの型はint、twoSum()の返り値はList\[int]であることを示す注釈.

```python
def twoSum(self, nums: List[int], target: int) -> List[int]:
```
