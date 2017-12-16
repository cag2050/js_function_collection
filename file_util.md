```
    dataURItoBlob (dataURI) {
        let arr = dataURI.split(',')
        let mime = arr[0].match(/:(.*?);/)[1]
        let bstr = atob(arr[1])
        let n = bstr.length
        let u8arr = new Uint8Array(n)
        while (n--) {
            u8arr[n] = bstr.charCodeAt(n)
        }
        return new Blob([u8arr], {type: mime})
    }
    // Blob 对象转为 File 对象
    blobToFile (theBlob, fileName) {
        theBlob.lastModifiedDate = new Date()
        theBlob.name = fileName
        return theBlob
    }
```