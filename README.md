# DeviceConnect-Spec
This file defines the Device Connect API specification ([Swagger 2.0](http://swagger.io/specification/) format).<br>
The API standardized here is realized in Device Connect.

For Device Connect System, refer to here: (https://github.com/DeviceConnect/DeviceConnect-Docs).<br>
For Device Connect API developer guidline, refer to here (https://github.com/DeviceConnect/DeviceConnect-Docs/wiki/Specification-Api-Guidelines).


# Output of Document
The Document assumes that the following commands are installed.

* Java
* cURL

Download DeviceConnect Codegen from [DeviceConnect-Experiments](https://github.com/DeviceConnect/DeviceConnect-Experiments).

```
$ curl -LkO https://github.com/DeviceConnect/DeviceConnect-Experiments/releases/download/codegen-v1.0.0/deviceconnect-codegen-project-1.0.0.dist.zip
$ unzip deviceconnect-codegen-project-1.0.0.dist.zip
```

Download newest definitions file from DeviceConnect-Spec.

```
$ curl -o DeviceConnect-Spec.zip -LkO https://github.com/DeviceConnect/DeviceConnect-Spec/archive/master.zip
$ unzip DeviceConnect-Spec.zip
```

Create documentation from downloaded definitions file.

```
$ java -Dfile.encoding=UTF-8 -jar ./deviceconnect-codegen-project-1.0.0/bin/deviceconnect-codegen.jar \
        --lang deviceConnectHtmlDocs \
        --display-name Device_Connect_RESTful_API_Specification \
        --input-spec-dir ./DeviceConnect-Spec-master/api \
        --output ./docs
```

にDevice Connect API document is folder specified by `--output` at time of execution.

#### Explanation of Options

> `--input-spec-dir`
> > Set the folder with definition file
>
> `--output`
> > Set the folder where document is output<br>
> > Create folder if it does not exist
> 
> `--lang`
> > Document is output, so specify*deviceConnectHtmlDocs*
> 
> `--display-name`
> > Set document name

Please refer to the following to learn more about the options listed above[Here](https://github.com/DeviceConnect/DeviceConnect-Experiments/tree/master/DeviceConnectCodegen).

