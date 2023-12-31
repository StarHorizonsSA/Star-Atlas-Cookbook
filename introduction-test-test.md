---
description: TEST TEST TEST TEST
---

# Introduction (TEST TEST)

### [Example's Setup](https://ttdonovan.github.io/staratlas-cookbook/intro.html#examples-setup) <a href="#examples-setup" id="examples-setup"></a>

Most if not all examples will follow this setup:

```typescript
import { AnchorProvider, Program, Wallet } from '@project-serum/anchor';
import { Connection, Keypair, PublicKey } from '@solana/web3.js';
import bs58 from 'bs58';

const rpc_url = Bun.env.SOLANA_RPC_URL || 'http://localhost:8899';
const connection = new Connection(rpc_url, 'confirmed');

const payer = Keypair.generate();

// const payer = Keypair.fromSecretKey(
//   bs58.decode(Bun.env.SOLANA_PAYER_SECRET_KEY || '')
// );

const provider = new AnchorProvider(
    connection,
    new Wallet(payer),
    AnchorProvider.defaultOptions(),
);
```

The wallet address used in examples [2yodqKtkdNJXxJv21s5YMVG8bjscaezLVFRfnWra5D77](https://solscan.io/account/2yodqKtkdNJXxJv21s5YMVG8bjscaezLVFRfnWra5D77).

### [Full Source Code Examples](https://ttdonovan.github.io/staratlas-cookbook/intro.html#full-source-code-examples) <a href="#full-source-code-examples" id="full-source-code-examples"></a>

Full source code examples can be found under `/scripts`.

Example of usage:

```
# make changes to `.env` file
$ cp .env.example .env

$ bun install
$ bun run scripts/01-player-profiles.ts
```
