# kami-text-diff

[![KAMI Plugin](https://img.shields.io/badge/KAMI-plugin-8A2BE2)](https://github.com/Hypijump31/KAMI)
[![Signed](https://img.shields.io/badge/Ed25519-signed-green)](https://github.com/Hypijump31/kami-registry)

Compare two texts and return added/removed/unchanged tokens (line, word, or char level).

## Install

```bash
kami install Hypijump31/kami-text-diff@v0.1.0
```

## Usage

```bash
# Line-level diff (default)
kami exec dev.kami.text-diff '{"old": "line1\nline2\nline3", "new": "line1\nmodified\nline3"}'

# Word-level diff
kami exec dev.kami.text-diff '{"old": "the quick brown fox", "new": "the slow brown cat", "mode": "words"}'

# Char-level diff
kami exec dev.kami.text-diff '{"old": "hello", "new": "hallo", "mode": "chars"}'
```

## Arguments

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `old` | string | yes | Original text |
| `new` | string | yes | New text to compare against |
| `mode` | string | no | `lines` (default) | `words` | `chars` |

## Build from source

```bash
git clone https://github.com/Hypijump31/kami-text-diff
cd kami-text-diff
cargo build --target wasm32-wasip2 --release
```

## Security

- Filesystem: none
- Network: none
- Max memory: 32 MB
- Max execution: 3000 ms

## License

MIT
