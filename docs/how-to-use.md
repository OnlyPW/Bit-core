# How to Use BIT Core

This page covers common wallet and nickname workflows.

## Send and Receive

Create a receive address:

```bash
bit-cli getnewaddress
```

Send to an address:

```bash
bit-cli sendtoaddress "<address>" 10
```

## Nickname Workflow

Check nickname availability and pricing:

```bash
bit-cli checknickname "bit_user"
```

Resolve active nickname:

```bash
bit-cli resolvenickname "bit_user"
```

List your wallet-controlled nicknames:

```bash
bit-cli listwalletnicknames
```

## Register a Nickname

1. Get owner key (pubkey from an address you control).
2. Choose payout address.
3. Broadcast registration.

```bash
# Example values shown for format only:
bit-cli registernickname "bit_user" "<33-byte-compressed-owner-pubkey-hex>" "<payout-address>"
```

## Update / Transfer / Renew / Release / Claim Bond

Update payout address:

```bash
bit-cli updatenickname "bit_user" "<new-payout-address>"
```

Transfer ownership:

```bash
bit-cli transfernickname "bit_user" "<new-owner-compressed-pubkey-hex>"
```

Renew:

```bash
bit-cli renewnickname "bit_user"
```

Release:

```bash
bit-cli releasenickname "bit_user"
```

Claim bond:

```bash
bit-cli claimnicknamebond "bit_user"
```

## Send to Nickname

```bash
bit-cli sendtonickname "bit_user" 5
```

Send to nickname with memo tag:

```bash
bit-cli sendtonickname "bit_user" 5 "" "" false "123456" "numeric"
```

## Useful RPC Help

```bash
bit-cli help checknickname
bit-cli help registernickname
bit-cli help sendtonickname
```
