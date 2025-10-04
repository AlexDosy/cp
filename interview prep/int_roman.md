function intToRoman(num: number): string {
      const val: number[] = [
        1000, 900, 500, 400,
        100, 90, 50, 40,
        10, 9, 5, 4, 1
    ];
     const syms: string[] = [
        "M", "CM", "D", "CD",
        "C", "XC", "L", "XL",
        "X", "IX", "V", "IV", "I"
    ];

    let roman=""
    let i=0;

    while(num>0){
        while(num>=val[i]){
            roman+=syms[i]
            num-=val[i]
        }
        i++
    }
    return roman
};


