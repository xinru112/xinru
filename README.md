# evm-batch-tools

Small, dependency-free Python tools for everyday EVM list and unit work.
纯 Python 小工具，无第三方依赖，处理 EVM 地址、单位换算和名单分批。

## Tools

### 1. checksum_addresses.py — EIP-55 checksum 地址

Validate addresses and convert them to checksum form. Duplicates are removed.

```bash
python3 tools/checksum_addresses.py examples/addresses.txt
python3 tools/checksum_addresses.py --check examples/addresses.txt
```

### 2. convert_units.py — unit conversion 单位换算

Supports `wei`, `gwei`, `ether`, and any token via `--decimals`.

```bash
python3 tools/convert_units.py 1.5 ether wei
# 1500000000000000000

python3 tools/convert_units.py 123.45 token --decimals 6 wei
# 123450000
```

### 3. split_batches.py — split a list into batches 名单分批

```bash
python3 tools/split_batches.py examples/list.txt --size 3 --out batches/
# 7 entries -> 3 batch file(s) in batches/
```

## Requirements

Python 3.8+. No pip installs needed.

## License

MIT
