SwapExactTokensForTokens ( amounIn, amountOutMin, address[] path, to)
-swaps all input for max output. 
calls a UniswapV2Library function called "getAmountsOut(it calculates an uint array called amounts-which stores the amount of tokens exchanged during swap process)"


amountOutMin- the min amount of tokens user wants from the swap
to-receiver of final output token
amounts[0] - input token amount
account[length -1] - output token amount
intermediary elements correspond to amounts exchanged during multi-hop process.

SETFT() transfers input tokens to pair contract=>inside the swap function, the func loops(for loops from i=0 to i=path.length -2) through the path array, iterating from index 0 to path.length -1. each iteration calculates pair contract address and executes swap on the pair contract.
automated => send token to pair contract => call internal function _swap.
pair contracts are created using function called create2 based on the input and output token addresses provided in the path array(contains addresses pf token involved)