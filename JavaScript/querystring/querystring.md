```js
import { querystring } from 'querystring'

querystring.parse('a=b&c=d') // {a:'b',c:'d'}, 默认参数为 location.search

querystring.stringify({a:'b',c:'d'}) // 'a=b&c=d'，注意不支持复杂嵌套的结构
```