## ES 基础

### 查询

1、search：

es通过search查询数据时，默认size为10，可通过设置进行

指定数据查询。size最大值为10000，不能进行大数据查询

2、helpers.scan

```
from elasticsearch import Elasticsearch
from elasticsearch import helpers
data=helpers.scan(client=self.es,query=EsInfo.body,scroll='20m',index=EsInfo.index)
此时data的数据类型为generator,需要转换成list
data=list(data)
```

