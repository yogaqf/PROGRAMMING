```dataviewjs
const data = dv.pages('"Javascript"');

const TotalJavascript = data.where(p => p.Lang == "Javascript").length;


const DataArray = [TotalJavascript];

const chartData = {
    type: 'bar',
    data: {
        labels: ['Javascript'],
        datasets: [{
            label: 'Total',
            data: DataArray,
            backgroundColor: [
                'rgba(255, 99, 132, 0.2)'
            ],
            borderColor: [
                'rgba(255, 99, 132, 1)'
            ],
            borderWidth: 1
            
        }]
    }
}

window.renderChart(chartData, this.container);
```

```dataview  
table Lang, Class, Source, Level, file.mtime as Last_Modified
sort file.mtime desc
```
