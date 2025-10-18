nums1[m:] = nums2
nums1.sort()

we can two pointers here as well
        midx= m-1
        nidx = n-1
        right = m+n-1
        while nidx>=0:
            if midx>=0 and nums1[midx]> nums2[nidx]:
                nums1[right] = nums1[midx]
                midx-=1
            else:
                nums1[right] = nums2[nidx]
                nidx -=1
            right-=1
