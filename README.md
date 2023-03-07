# UiTest
function longestConsec(strarr, k) {
  let n=strarr.length
  if (n==0 || k>n || k<=0){
    return "";
  }else{
      let list =[];
    
    //Joining two consecutive values of array
    
      for (var i=0;i<n-k+1;i++)
        {
          list[i]=strarr.slice(i,k+i).join('');
          
         }
    
  //finding the first longest value
    
      let longest = list.reduce((a, b)=> a.length >= b.length ? a : b);
      return longest;
}
}
let strarr = ["tree", "foling", "trashy", "blue", "abcdef", "uvwxyz"]
let strarr2= ["zone", "abigail", "theta", "form", "libe", "zas", "theta", "abigail"]
let k = 2
console.log(longestConsec(strarr,k))
console.log(longestConsec(strarr2,k))
