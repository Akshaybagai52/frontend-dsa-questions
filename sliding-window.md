## 239. Sliding Window Maximum

### // brute force 
var maxSlidingWindow = function(nums, k) {
    let startInd = 0;
    let endInd = startInd + k;
    let outputArr = [];
    while(endInd <= nums.length) {
        let arr = nums.slice(startInd, endInd).sort((a, b) => b - a)
        outputArr.push(arr[0]);
        startInd++;
        endInd++;
    }
    return outputArr;    
};
