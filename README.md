# DeviceConnect-Spec
This file defines the Device Connect API specification ([Swagger 2.0](http://swagger.io/specification/) format).<br>
The API standardized here is realized in Device Connect.

For Device Connect System, refer to here: (https://github.com/DeviceConnect/DeviceConnect-Docs).<br>
For Device Connect API developer guidline, refer to here (https://github.com/DeviceConnect/DeviceConnect-Docs/wiki/Specification-Api-Guidelines).


# Output of Document
The Document assumes that the following commands are installed.

* Java
* cURL

[DeviceConnect-Experiments](https://github.com/DeviceConnect/DeviceConnect-Experiments) から DeviceConnect Codegen をダウンロードします。

```
$ curl -LkO https://github.com/DeviceConnect/DeviceConnect-Experiments/releases/download/codegen-v1.0.0/deviceconnect-codegen-project-1.0.0.dist.zip
$ unzip deviceconnect-codegen-project-1.0.0.dist.zip
```

DeviceConnect-Spec から最新の定義ファイルをダウンロードします。

```
$ curl -o DeviceConnect-Spec.zip -LkO https://github.com/DeviceConnect/DeviceConnect-Spec/archive/master.zip
$ unzip DeviceConnect-Spec.zip
```

ダウンロードした定義ファイルからドキュメントを作成します。

```
$ java -Dfile.encoding=UTF-8 -jar ./deviceconnect-codegen-project-1.0.0/bin/deviceconnect-codegen.jar \
        --lang deviceConnectHtmlDocs \
        --display-name Device_Connect_RESTful_API_Specification \
        --input-spec-dir ./DeviceConnect-Spec-master/api \
        --output ./docs
```

実行すると`--output`で指定したフォルダにDevice Connect APIのドキュメントが作成されます。

#### 各オプションの説明

> `--input-spec-dir`
> > 定義ファイルが置いてあるフォルダを指定します。
>
> `--output`
> > ドキュメントを出力する先のフォルダ名を指定します。<br>
> > 指定されたフォルダが存在しない場合には作成します。
> 
> `--lang`
> > ドキュメントを出力するので、*deviceConnectHtmlDocs*を指定します。
> 
> `--display-name`
> > ドキュメントのタイトルを指定します。

上記に記載したオプションが知りたい場合には[こちら](https://github.com/DeviceConnect/DeviceConnect-Experiments/tree/master/DeviceConnectCodegen)を参照してください。

