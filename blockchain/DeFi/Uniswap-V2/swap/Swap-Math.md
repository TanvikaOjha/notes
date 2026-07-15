**Swap Math**

X0 -initial X tokens
Y0-initial Y tokens

X0 + dx -final amount of X tokens
Y0 - dy -final amount of Y tokes

$x0 * y0 = (x0 + dx)(y0 - dy)$

$dy = (y0 * dx) / (x0 + dx)$ => considering no swap fee

Swap fee - charged to the token that is inputed into the liquidity pool.
swap fee rate = f( 0 < f < 1)
swap fee = f * dx


$dy = (y0 * dx(1-f))/(x0 + dx(1-f))$


1.Single-Hop Swaps- uses one pair contract to swap between two tokens
user calls swapExactTokensForTokens(amount of token1, adress of token 2) on router contract => router transfers token1 to pair contract and calls the swap func on it => router transfer token2 => router gives back to user.

for swapping ETH for other tokens: swapExactEthForTokens().


2.Multi-Hop Swaps- uses two or more pair contracts, in a series, to swap two tokens.
For WETH/MKR :
router transfers WETH to DAI/WETH pair => swaps and gets DAI => calls DAI/MKR => swaps and get MKR.
