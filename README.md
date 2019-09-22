# Array

//连接数组
var arr1 = [1,2,3];
var arr2 = [4,5,6];
var arr3 = arr1.concat(arr2);
console.log(arr3);  //[ 1, 2, 3, 4, 5, 6 ]


//用分隔符连接数组元素，形成字符串
var strArr = ['aa','bb','cc'];
console.log(strArr.join());  //aa,bb,cc
console.log(strArr.join('-'));  //aa-bb-cc


//删除数组最后一个元素
var stackArr = [1,2,3,4];
stackArr.pop();
console.log(stackArr);  //[ 1, 2, 3 ]


//数组末尾添加一个或多个元素
var arr = [1,2,3];
arr.push(4);
console.log(arr);  //[ 1, 2, 3, 4 ]
arr.push(5,6);
console.log(arr);  //[ 1, 2, 3, 4, 5, 6 ]


//反转数组
var initArr = [1,2,3];
initArr.reverse();
console.log(initArr);  //[ 3, 2, 1 ]


//删除数组第一个元素
var arr4 = [1,2,3,4];
arr4.shift();
console.log(arr4);  //[ 2, 3, 4 ]


//向数组开头添加一个或多个元素
var arr5 = [4,5];
arr5.unshift(3);
console.log(arr5);  //[ 3, 4, 5 ]
arr5.unshift(1,2);
console.log(arr5);  //[ 1, 2, 3, 4, 5 ]


//数组排序
var arrs = [1,3,5,2,4];
arrs.sort();
console.log(arrs);  //[ 1, 2, 3, 4, 5 ]
arrs.sort(function (a,b){
return a - b;
});
console.log(arrs);  //[ 1, 2, 3, 4, 5 ]
arrs.sort(function (a,b){
return b - a; 
});
console.log(arrs);  //[ 5, 4, 3, 2, 1 ]


//截取数组 arrs.slice(start,end);
//start参数必需，从何处开始选取，包括start。如果为负数，会从尾部选取，比如-1代表最后一个元素。
//end参数可选，从何处结束选取，不包括end。如果没有指定该参数，数组会包含从start开始到数组结束的所有元素。
//如果该参数是负数的话，表示从数组尾部开始算起的元素。
var arr6 = [1,2,3,4,5];
console.log(arr6.slice(1));  //[ 2, 3, 4, 5 ]
console.log(arr6.slice(1,3));  //[ 2, 3 ]
console.log(arr6.slice(1,-1));  //[ 2, 3, 4 ]


//插入、删除和替换数组的元素
//Array.splice(index,howmany,element1,.....elementX);
//index必需，从何处添加、删除元素，开始插入或删除数组元素的下标
//howmany必需，应该删除多少个元素，可以为0，如果未设定该参数，则删除从index开始到数组结尾的所有元素
//element1可选，添加到数组中的新元素，从index下标开始插入
//elementX可选，可向数组中添加若干个元素
var arr7 = [1,2,3,4,5,6];
arr7.splice(1,0,8);
console.log(arr7);  //[ 1, 8, 2, 3, 4, 5, 6 ]
arr7.splice(2,1);
console.log(arr7);  //[ 1, 8, 3, 4, 5, 6 ]
arr7.splice(1,1,10);
console.log(arr7);  //[ 1, 10, 3, 4, 5, 6 ]
————————————————
版权声明：本文为CSDN博主「lihaomuye」的原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/lihaomuye/article/details/79758314
