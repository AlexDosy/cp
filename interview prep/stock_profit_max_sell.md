we can sell stock in a day multiple time but can hold only one stock at a time
        profit =0
        n= len(prices)
        for i in range(1,n):
            if prices[i]>prices[i-1]:
                profit+=prices[i]-prices[i-1]
        return profit


        profit checking at each step(if prices[i]>prices[i-1]:) eventually builds a cumulative profit which is greater or equal to previous problem--