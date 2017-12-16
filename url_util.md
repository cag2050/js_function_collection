```
// 获取url中的参数值，举例：var id = getUrlParam('id') !== null && getUrlParam('id').toString().length > 1 ? getUrlParam('id') : ''
    function getUrlParma(name) {
        var reg = new RegExp("(^|&)" + name + "=([^&]*)(&|$)");
        var r = window.location.search.substr(1).match(reg);
        if (r != null) {
            return decodeURIComponent(r[2]);
        }
        return null;
    }
```