---
id: withdraw-exit-faster
title: withdrawExitFaster
keywords:
- 'plasma client, erc721, withdrawExitFaster, polygon, sdk'
description: '引き出すプロセスを終了します。'
---

`withdrawExitFaster`メソッドは、すべてのトークンを承認するために使用できます。

バックエンドでプルーフを生成するため高速です。バックエンドは、専用のプライベートのリモートプロシージャコール（RPC）を用いて設定できます。

**注記**- 引き出しを終了するには、withdrawStartトランザクションにチェックポイントを設定する必要があります。

```
const erc721RootToken = plasmaClient.erc721(<root token address>, true);

const approveResult = await erc721RootToken.withdrawExitFaster(<burn tx hash>);

const txHash = await approveResult.getTransactionHash();

const txReceipt = await approveResult.getReceipt();

```
