It finds the first station from where you can complete the full circle.

You don't need to explicitly wrap the loop, because the return value tells where to start, and from there you’ll naturally wrap around in the real journey.


if (gas.reduce((a,b) => a+b, 0)<cost.reduce((a,b)=>a+b,0)){
        return -1
    }

    let currentGas =0;
    let start = 0;

    for (let i =0; i<gas.length; i++){
        currentGas +=gas[i] - cost[i];
        if(currentGas < 0){
            currentGas = 0;
            start =i+1
        }
    }
    return start