If the current string does not start with the prefix, shorten the prefix. --> while (strs[i].indexOf(common) !== 0) { common.slice(0,-1)}

 
    if(strs.length===0) return "";
    let common=strs[0]
    for (let i = 1; i < strs.length; i++) {
        while (strs[i].indexOf(common) !== 0) {
            common=common.slice(0,-1);
            if (common === "") return ""
        }
    }
    return common