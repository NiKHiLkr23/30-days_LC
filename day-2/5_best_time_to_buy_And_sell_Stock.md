
https://leetcode.com/problems/best-time-to-buy-and-sell-stock/

```python
class Solution:
    def maxProfit(self, prices: List[int]) -> int:
        l,r=0,1
        m=0
        while r<len(prices):
            if prices[l] < prices[r]:
                profit=prices[r]-prices[l]
                m=max(m,profit)
            else:
                l=r
            r += 1
        return m