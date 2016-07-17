# COSON简介

<https://github.com/bevry/cson#what-is-cson>

## 安装

-   安装：`npm install --save cson`
-   使用：`require('coson')`

## 什么是CSON

CoffeeScript的JSON。易读易写，不需大括号和换行转义，支持注释和多行字符串，不用担心忘掉写逗号。

以下面的JSON数据为例：

```javascript
{
  "greatDocumentaries": [
    "earthlings.com",
    "forksoverknives.com",
    "cowspiracy.com"
  ],
  "importantFacts": {
    "emissions": "Livestock and their byproducts account for at least 32,000 million tons of carbon dioxide (CO2) per year, or 51% of all worldwide greenhouse gas emissions.\nGoodland, R Anhang, J. “Livestock and Climate Change: What if the key actors in climate change were pigs, chickens and cows?”\nWorldWatch, November/December 2009. Worldwatch Institute, Washington, DC, USA. Pp. 10–19.\nhttp://www.worldwatch.org/node/6294"
  }
}
```

等价的COSON如下：

```coffee
# 允许注释！！

# 数组项目不需逗号隔开
greatDocumentaries: [
    'earthlings.com'
    'forksoverknives.com'
    'cowspiracy.com'
]
# 对象上不需要大括号
importantFacts:
	# 多行字符串不需要换行转义
	emissions: '''
		Livestock and their byproducts account for at least 32,000 million tons of carbon dioxide (CO2) per year, or 51% of all worldwide greenhouse gas emissions.
		Goodland, R Anhang, J. “Livestock and Climate Change: What if the key actors in climate change were pigs, chickens and cows?”
		WorldWatch, November/December 2009. Worldwatch Institute, Washington, DC, USA. Pp. 10–19.
		http://www.worldwatch.org/node/6294
		'''
```
