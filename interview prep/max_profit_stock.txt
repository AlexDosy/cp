    bruteforce::____
        profit=[]
        for i in range(len(prices)):
            for j in range(i,len(prices)):
                if prices[i]<prices[j]:
                    profit.append(prices[j]-prices[i])
        if profit==[]:
            return 0
        else:
            return max(profit)

kadanes algorithm?
buy = prices[0]
        profit = 0
        for i in range(1, len(prices)):
            if prices[i] < buy:
                buy = prices[i]
            elif prices[i] - buy > profit:
                profit = prices[i] - buy
        return profit