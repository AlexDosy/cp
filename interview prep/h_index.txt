The h-index is defined as the maximum value of h such that the given researcher has published at least h papers that have each been cited at least h times.

    const n = citations.length;
    citations.sort((a,b)=>a-b)
    for ( let i = 0; i<n;i++){
        if(citations[i]>=n-i){
            return n-i
        }
    }
    return 0;

    the condition citation >= n - i holds is the maximum h-index. This is because it indicates that the paper has been cited more times than the number of papers that follow, and it’s impossible to satisfy this condition for larger indexes.