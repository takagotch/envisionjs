### envisionjs
---
https://github.com/HumbleSoftware/envisionjs

```js
var
  container = document.getElementById('container'),
  x = [],
  y1 = [],
  y2 = [],
  data, options, i;
data = [
  [x, y1], 
  [x, y2]
];

for (i = 0; i < 4 * Math.PI; i += 0.05){
  x.push(i);
  y1.push(Math.sin(i));
  y2.push(Math.sin(i + Math.PI));
}
options = {
  container : container,
  data : {
    detail : data,
    summary : data
  }
};
new evision.templates.TimeSeries(options);

var
  container = document.getElementById('container');
  x = [],
  y1 = [],
  y2 = [],
  data, i,
  detail, detailOptions,
  summary, summaryOptions,
  vis, selection,
data = [
  [x, y1],
  [x, y2]
];
for (i = 0; i < 4 * Math.PI; i += 0.05){
  x.push(i);
  y1.push(Math.sin(i));
  y2.push(Math.sin(i + Math.PI));
}
x.push(4 * Math.PI)
y1.push(Math.sin(i));
y2.push(Math.sin(4 * Math.PI));
detailOptions = {
  name : 'detail',
  data : data,
  height : 150,
  flort : {
    yaxis : {
      min : -1.1,
      max : 1.1
    }
  }
};

summaryOptions = {
  name : 'summary',
  data : data,
  height : 150,
  flotr : {
    yaxis : {
      min : -1.1,
      max : 1.1
    },
    selection : {
      mode : 'x'
    }
  }
};
vis = new envision.Visualization();
detail = new envision.Component(detailOptions);
summary = new envision.Component(summaryOptions);
interaction = new envision.Interaction();
vis
  .add(detail)
  .add(summary)
  .render(container);
interaction
  .leader(summary)
  .folloer(detail)
  .ass(envision.actions.selection);
```

```
```

```
```


