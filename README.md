###压缩解压文件

文件以二进制读取，压缩并解压
本库里有d.ts文件，可用于typeScript语言的项目，例如 egret 白鹭引擎

###解压

    let plain = new Uint8Array(data);  //data is a ArrayBuffer
    let inflate = new Zlib.Inflate(plain);
	let deplain = inflate.decompress();
	let lastbytes = deplain.buffer;
	//egret 将二进制解析成object
	let bytes: egret.ByteArray = new egret.ByteArray(lastbytes);
	let obj = JSON.parse(bytes.readUTFBytes(lastbytes.byteLength));









