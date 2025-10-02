We can solve this efficiently using a two-pass greedy algorithm:

Left to Right pass:

Start by giving each child 1 candy.

Traverse from left to right.

If the current child's rating is greater than the previous child's, give one more candy than the previous child.

Right to Left pass:

Traverse from right to left.

If the current child's rating is greater than the next child's, update the current child's candy count to max(current, next + 1).

Finally, sum all the candies.



function candy(ratings: number[]): number {
    const n=ratings.length
    const candy= new Array(n).fill(1)

    for (let i =0;i<n;i++){
        if (ratings[i]>ratings[i-1]){
            candy[i]=candy[i-1]+1
        }

    }
    for (let i=n-2;i>=0;i--){
        if (ratings[i]>ratings[i+1]){
            candy[i]=Math.max(candy[i],candy[i+1]+1)
        }
    }

    return candy.reduce((a,b)=>a+b,0)
};