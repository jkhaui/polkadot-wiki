---
id: maintain-guides-how-to-stop-validating
title: How to Stop Validating
sidebar_label: How to Stop Validating
---

To ensure a smooth stop to validation, make sure you should do the following actions:

1. Chill your validator tokens
2. Purge validator session keys
3. Unbond your tokens

These can all be done with [PolkadotJS Apps](https://polkadot.js.org/apps) interface or with
extrinsics.

## Chill tokens

To chill your tokens, see the [How to Chill](maintain-guides-how-to-chill) page. You can also
[claim your rewards](learn-simple-payouts#claiming-rewards) at this time.

## Purge validator session keys

Purging the validator's session keys removes the key reference to your stash. This can be done
through the `session.purgeKeys()` extrinsic with the controller account.

> NOTE: **If you skip this step, you will not be able to reap your stash account**, and you will
> need to rebond, purge the session keys, unbond, and wait the unbonding period again before being
> able to transfer your tokens. See [Unbonding and Rebonding](maintain-guides-how-to-unbond) for
> more details.

## Unbond your tokens

Unbonding your tokens can be done through the `Network > Staking > Account actions` page in
PolkadotJS Apps by clicking the corrosponding stash account dropdown and selecting "Unbond funds".
This can also be done through the `staking.unbond()` extrinsic with the controller account.
