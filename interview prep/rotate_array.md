k%= len(nums) ---> this is done so as to avoid repetition its same as rotating k times

nums[:]= nums[-k:]+nums[:-k]


there are other several solutions