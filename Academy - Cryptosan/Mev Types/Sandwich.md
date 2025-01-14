Sandwich MEV

Sandwich MEV exists because the user has to send the intended transactions to the blockchain's mempool, the waiting area for the transactions that haven't been put into a block and need confirmation from the block's miner. 

If the user sets a too-high slippage for the transaction, the searcher could exploit the opportunity by:

Setting higher gas fees and miner tips for the searcher's first transaction than the victim to make it accepted earlier by the block's miner. 

Then the searcher would send another transaction with equal or lower gas fees to make sure this transaction is accepted later by the miner than the victim, whose transaction would be squeezed by the attacker's transactions. 

How exactly does the attacker gain revenues during the process? Here is an example. 

In a UNISWAP liquidity pool, Bob is a retail investor who wants to trade 1000 $WETH for $USDC. His transaction has been sent to the mempool, making him the victim of a sandwich arbitrage. The transaction is marked as ①  in the figure below. 

Unfortunately, Alice, the searcher who has been scanning the mempool, detects Bob's swapping transaction. 

Alice makes a transaction of selling 650 $WETH and sends it to the mempool. In the end, she receives 1,842,200 $USDC at the exchange rate of 1 $WETH for 2,834 $USDC. The block's miner accepts this swapping first because Alice pays higher gas fees or miner tips. The swapping causes the exchange rate to change to 1 $WETH for 2,821 $USDC. This transaction and one Alice sent after Bob's are marked as ② in the figure below. 

Bob's transaction goes through the mempool and to the block selling 1000 $WETH for 2,821,000 $USDC, which he should have been able to get 2,834,000 $USDC. 

Alice's selling of 1,842,200 $USDC passes the mempool and gets recorded by the miner in the block. She receives 652.9 $WETH.  

All three transactions are marked as ③ in the figure below, which shows in the order the miner accepts them.