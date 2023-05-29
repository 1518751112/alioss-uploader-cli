aliyun oss upload cli

**增加指定配置文件名称**
* 注意：配置文件名称为'.aliossrc' 取名称：alioss
* 默认配置文件名称为'.aliossrc'
```
aliossUploader alioss
```


```
npm i -g @tg1518/alioss-uploader-cli
```

make file '.aliossrc'
```
{
    "accessKeyId": "***",
    "accessKeySecret": "***",
    "region": "oss-cn-hangzhou", // eg: oss-cn-hangzhou
    "bucket": "stgame",
    "prefix": "test", // oss directory prefix; eg: auto_upload_ci/test
    "srcPath":"dist", // upload directory
    "exclude": ".*$" // Optional, default: .*$
}
```

edit 'package.json'
```
{
    ...
    "scripts": :{
        "upload": "aliossUploader"
        ...
    }
    ...
}
```

upload

```
npm run upload
```
