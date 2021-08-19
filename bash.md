# Bash

## for

### range, sequence

```text
## n=0~101までの102個のフォルダ名nのフォルダ生成

for ITEM in `seq 0 101`
do
    mkdir "${ITEM}"
done


## 2桁ゼロ埋め

for ITEM in `seq -f %02g 0 101`
do
    mkdir "${ITEM}"
done
```

## string for

```text
task="ambitious
gentle
intellectual
rich
stylish
unique"

for i in ${task}; do
    echo ${i}
    echo "abc"
done

#### execute result
$ bash test.sh 
ambitious
abc
gentle
abc
intellectual
abc
rich
abc
stylish
abc
unique
abc
```



