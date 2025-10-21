removing given val and return the no remaining elements in an array

1 aproach:
    to loop through a for loop and count no of times ith element is not equal to value

2nd aproach:
    using two pointer swap the elements equal to val occuring from left to right end -- return r +1
        l = 0
        r = len(nums) - 1

        while l <= r:
            if nums[l] == val:
                nums[l] = nums[r]
                r -= 1
            else:
                l += 1

        return r + 1 