```
// 将cookie转化成json对象
var ToJsonObj = function () {
	var json_hash = {};
	var cookie = document.cookie;
	var trans_one = cookie.split("; ");
	for(var i=0,len=trans_one.length;i<len;i++){
		json_hash[trans_one[i].split('=')[0]] = trans_one[i].split('=')[1];
	}
	return json_hash;
}
```