# Argparse

## import module

```python
import argparse
```

```python
parser = argparse.ArgumentParser()
parser.add_argument('-d','-dir', help='read pkl directory')
args = parser.parse_args()

pkl_dir = args.d
```

