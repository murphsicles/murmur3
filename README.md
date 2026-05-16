# @crypto/murmur3

MurmurHash3 32-bit for Zeta — used in BSV P2P bloom filters.

## Why This Exists

BSV nodes use bloom filters for lightweight transaction filtering (SPV). MurmurHash3 32-bit is the hash function used in the bloom filter implementation.

This crate provides a clean, minimal implementation of MurmurHash3 for Zeta.

## Usage

```zeta
use @crypto/murmur3::{murmur3_32, Murmur3_32};

// Function interface
let hash: u32 = murmur3_32(key, seed);

// Struct interface
let hash = Murmur3_32::hash(key, seed);
let value: u32 = hash.value();
```

## API

### Functions

```zeta
pub fn murmur3_32(key: &[u8], seed: u32) -> u32
```

### Types

```zeta
pub struct Murmur3_32 {
    fn hash(data: &[u8], seed: u32) -> Self;
    fn value(self) -> u32;
}
```

## Reference

- [SMHasher](https://github.com/aappleby/smhasher) — original MurmurHash3 implementation
- BSV P2P protocol for bloom filter integration

## License

MIT

For nour. For Dark Factory. For BSV.
