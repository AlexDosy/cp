function lengthOfLastWord(s: string): number {
    let end = s.length -1
    while(end>=0 && s[end]===' '){
        end--
    }
    let start= end
    while (start>=0 &&s[start]!==' '){
        start--
    }
    return end-start
};

we will subtract end if there are traling space to get to the last word
start corresponds to end, start will be subtract by the required length times
return end-start