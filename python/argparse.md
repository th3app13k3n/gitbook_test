# Argparse

## import module

```python
import argparse
```

### example0

```python
parser = argparse.ArgumentParser()
parser.add_argument('-d','-dir', help='read pkl directory')
args = parser.parse_args()

pkl_dir = args.d
```

### example1

```python
def create_argument_parser() -> argparse.ArgumentParser:
    parser = argparse.ArgumentParser()

    parser.add_argument(
        '--r_xyzcp',
        metavar="<read_xyzcp_npy>",
        action='store',
        default=None,
        required=True
    )
    parser.add_argument(
        '--d_split_npy',
        metavar="<save dir tmp split npy>",
        action='store',
        default=None,
        required=True
    )
    parser.add_argument(
        '-s', '--s_min_list',
        metavar="<save_min_list>",
        action='store',
        default=None,
        # required=True
    )
    parser.add_argument(
        '--s_nearest_xyzc',
        metavar="<save_nearest_xyzc>",
        action='store',
        default=None,
        required=False
    )

    return parser

def main():
    parser = create_argument_parser()
    args = parser.parse_args()

    r_table_xyzcp = args.r_xyzcp
```

