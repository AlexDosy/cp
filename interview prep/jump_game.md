goal = len(nums)-1
        for i in range(len(nums)-2, -1,-1):
            if i + nums[i] >= goal:
                goal = i

        return True if goal==0 else False


        we will loop from second last element to the first element
        logic if current element + index >= goal, goal can be updated to that index
        at last if goal is becoming 0, return True