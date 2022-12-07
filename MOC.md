
```dataviewjs
const data = dv.pages();

const TotalObsidian = data.where(p => p.Lang == "Obsidian").length;
const TotalJavascript = data.where(p => p.Lang == "Javascript").length;
const TotalPHP = data.where(p => p.Lang == "PHP").length;
const TotalVSCode = data.where(p => p.Lang == "VS Code").length;


const DataArray = [TotalJavascript, TotalPHP, TotalObsidian, TotalVSCode];

const chartData = {
    type: 'bar',
    data: {
        labels: ['Javascript','PHP', 'Obsidian', 'VS Code'],
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

---
```dataview  
table Lang, Class, Source, Level, file.mtime as Last_Modified
sort file.mtime desc
limit 10
```
