---
title: 计算标准差
tags: [计算公式, JavaScript]
---

### js 计算 标准差

- 总数求和,平均数

```javascript
data = [];
sum = data.reduce((prev, curr) => prev + curr);
ave = sum / data.length;
```

- 各项之差,差值平方和

```javascript
devi = data.map((item) => item - ave);
deviPow = devi.map((item) => item * item);
deviPowSum = deviPow.reduce((prev, curr) => prev + curr);
```

- 差值平方平均 (非总体数据除数为 N-1)

```javascript
deviPowAve = deviPowSum / data.length;
```

- 平方平均开方

```javascript
standardDeviation = Math.sqrt(deviPowAve);
```
