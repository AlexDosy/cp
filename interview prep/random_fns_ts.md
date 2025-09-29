class RandomizedSet {
    map:Map<number,number>
    arr:number[]
    constructor() {
       this.map = new Map;
       this.arr= [];
    }

    insert(val: number): boolean {
        if(this.map.has(val)) return false
        this.map.set(val,this.arr.length)
        this.arr.push(val)
        return true
    }

    remove(val: number): boolean {
        if(!this.map.has(val)) return false
        const last = this.arr[this.arr.length-1]
        const index = this.map.get(val)
        this.map.set(last, index)

        this.arr[index]=last
        this.arr.pop()
        this.map.delete(val)
        return true
    }

    getRandom(): number {
       return this.arr[Math.floor(Math.random() * this.arr.length)]
    }
}

/**
 * Your RandomizedSet object will be instantiated and called as such:
 * var obj = new RandomizedSet()
 * var param_1 = obj.insert(val)
 * var param_2 = obj.remove(val)
 * var param_3 = obj.getRandom()
 */