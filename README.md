## 原理

先`prettier`格式化，再用`正则替换`匹配到的字符，但在代码中注视掉的模块，我们无法格式化，这会导致一些匹配上出现的错误，和冗余的资源下载，但是基于正则的模式下，这很难避免。所以即使提供了全量一次性替换，仍然建议少量多次,具体请查看`i2l -h`

## 可转换的格式

### .js | .jsx

```jsx
  src = {'xxx'} 
  src = 'xxx'
  backgroundImage=`url(xxx)`
```

### .less

```less
url('xxx')
```