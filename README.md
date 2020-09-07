amcharts圖表使用總結
其他 · 發表 2019-01-23


Amcharts JS 版屬性/方法詳細說明書

1、     座標軸（Y軸）  
序號     屬性名/方法名     作用     物件獲取方法/常用屬性值     示例;
1     valueAxis物件     圖表的Y軸，一個圖表中可以有多個Y軸     Var valueAxis = new AmCharts.ValueAxis();    
2     axisColor      軸的顏色            valueAxis.axisColor = "#FF6600";
3     axisThickness     軸的寬度          valueAxis.axisThickness = 1;
4     gridAlpha     軸的透明度，值介於0-1之間，0全透明          valueAxis1.gridAlpha = 0.2;
5     tickLength     軸從下到上像左或右伸出來的延長線          valueAxis1.tickLength =0;
6     minimum     軸的最小值，如果不設定那麼最小值根據資料動態變化          valueAxis1.minimum = -100;
7     maximum     軸的最大值，如果不設定那麼最大值根據資料動態變化          valueAxis1.maximum = 100;
8     title     軸的名稱          valueAxis1.title="哈哈";
9     logarithmic     是否為對數函式分佈，一般軸的刻度是均勻劃分的，當該屬性設定為true的時候，刻度分佈呈對數形式分佈          valueAxis1.logarithmic = false;
10     integersOnly     是否只顯示整數，如果為true軸的刻度只顯示整數形式          valueAxis1.integersOnly = true;
11     gridCount     最大刻度個數          valueAxis1.gridCount = 10;
12     unit     單位          valueAxis1.unit = "%";
13     labelsEnabled     是否顯示軸標籤，預設值為true          valueAxis1.labelsEnabled = true;
14     inside     軸的刻度值顯示在表裡面還是外面          valueAxis1.inside = true;
15     position     軸的位置，預設在左側          valueAxis1.position = "left";
16     stackType               valueAxis.stackType = "0%";

2、     categoryAxis（圖表線，相當於X軸）
序號     屬性名/方法名     作用     物件獲取方法/常用屬性值     示例
1     valueAxis物件     圖表的線，一個圖表中可以有多個，每個對應一個Y軸或者共同擁有一個Y軸     var categoryAxis = chart.categoryAxis;    
2     parseDates     是否以日期為x軸的值     True、false       categoryAxis.parseDates = false;
3     minPeriod     當以日期為x軸的時候x軸顯示的最小範圍     SS：分鐘 DD：天      categoryAxis.minPeriod = "SS"
4     dashLength     破折線長度，預設為0是實心線          categoryAxis.dashLength = 1;
5     gridAlpha     網格的透明度，垂直x軸的刻度線形成網格          categoryAxis.gridAlpha = 0.15;
6     axisColor     軸的顏色          categoryAxis.axisColor = "#DADADA";
7     position     軸的位置，預設在最下方     top：顯示在上方 left:左側right：右側     categoryAxis.position = "top";
8     gridPosition     網格位置          categoryAxis.gridPosition = "start";
9     startOnAxis     是否從軸上開始繪製，預設為false，即第一個點繪製是從中間開始的，當設定為true的時候，第一個點開始總是從Y軸上開始，結束總是在最後一個跟Y軸平行的軸上結束     true、false     categoryAxis.startOnAxis = true;
10     gridColor     網格顏色          categoryAxis.gridColor = "#FFFFFF";
11     dateFormats     日期格式，將資料格式化成對應的日期格式          categoryAxis.dateFormats = [{                          period:'DD',            format: 'DD'},
{period:'WW',           format: 'MMM DD'},
{period: 'MM',format:'MMM'},    period: 'YYYY',
format: 'YYYY'
}];
12                   
3、     Legend（圖例）
序號     屬性名/方法名     作用     物件獲取方法/常用屬性值     示例
1     legend物件     在圖表的上方或者下方顯示圖例，圖例的顏色就是對應線條的顏色     var legend = new AmCharts.AmLegend();    
2     align     排列樣式     center        legend.align = "center";
3     marginLeft     左邊緣          legend.marginLeft = 0;
4     title     標題          legend.title="測試";
5     horizontalGap     水平間隔，一個圖表可以有多個圖例，圖例之間的間隔用此屬性          legend.horizontalGap = 10;
6     equalWidths     是否等寬          legend.equalWidths = false;
7     valueWidth     值的寬度，在圖例的右側會顯示該線或者圖表的當前選中的值，設定為0時則不顯示值          legend.valueWidth = 120;
8     switchType     暫時沒明白什麼意思          legend.switchType = "v";

4、     Guide（嚮導線）
序號     屬性名/方法名     作用     物件獲取方法/常用屬性值     示例
1     guide物件     嚮導線可以是一條根Y軸平行的線，也可以是一個矩形區域       var guide = new AmCharts.Guide();    
2     fillAlpha     區域透明度            guide.fillAlpha = 0.1;
3     lineAlpha     線透明度          guide.lineAlpha = 0;
4     value     其實值，其實指對應Y座標的值          guide.value = 50;
5     toValue     到達值，其實指對應Y座標的值，跟上面屬性共同確定了一個從value到toValue的區域，寬度為圖表的寬度，高度為（toValue-value）的絕對值          guide.toValue = 0;
6     lineColor     相導線的顏色          guide.lineColor = "#CC0000";
7     dashLength     破折長度，預設為0為實心線條，設定值後為破折線          guide.dashLength = 4;
8     label     標籤，就是給嚮導線顯示一個名字          guide.label = "平均值";
9     inside     是否讓嚮導線顯示在圖形裡面，預設為true     True，false     guide.inside = true;

5、     Scrollbar（滾動條）
序號     屬性名/方法名     作用     物件獲取方法/常用屬性值     示例
1     scrollbar物件     滾動條可以選擇圖表顯示的區域     var chartScrollbar = new AmCharts.ChartScrollbar();    
3     backgroundAlpha     滾動條背景透明度          chartScrollbar.backgroundAlpha = 0.1;
4     backgroundColor     滾動條背景顏色          chartScrollbar.backgroundColor = "#000000";
5     graphLineAlpha     影象線條的透明度          chartScrollbar.graphLineAlpha = 0.1;
6     graphFillAlpha     影象的填充透明度          chartScrollbar.graphFillAlpha = 0;
7     selectedGraphFillAlpha     選中影象的填充色的透明度          chartScrollbar.selectedGraphFillAlpha = 0;
8     selectedGraphLineAlpha     選中區域的影象線條透明度          chartScrollbar.selectedGraphLineAlpha = 0.25;
9     scrollbarHeight     滾動條高度          chartScrollbar.scrollbarHeight = 30;
10     selectedBackgroundColor     選中區域的背景顏色          chartScrollbar.selectedBackgroundColor = "#FFFFFF";

6、     Graph (圖表)
序號     屬性名/方法名     作用     物件獲取方法/常用屬性值     示例
1     graph物件     影象物件，必須有該屬性       var graph1 = new AmCharts.AmGraph();    
2     valueAxis     影象的Y軸，一個chart可以新增多個graph，一個graph只能有一個valueAxis            graph1.valueAxis = valueAxis1;
3     valueField     指定一個欄位作為Y座標值          graph1.valueField = "visits";
4     bullet     影象的節點型別          graph1.bullet = "round";
5     dashLength     繪製圖像時延時，預設為0秒，設定為正整數時可以看到動態生成效果          graph1.dashLength = 0;
6     hideBulletsCount     一個影象中當節點大於一定數值後隱藏節點形狀          graph1.hideBulletsCount = 10;
7     balloonText     節點顯示的文字內容          graph1.balloonText = "[[date]] ([[visits]])";
8     lineColor     影象線顏色          graph1.lineColor = "#d1655d";
9     connect     是否連線起來，是指如果資料有x軸值，但是y軸值丟失的時候，如果設定為true則忽略該點，設定為false則線條在此點處斷開          graph1.connect = false;
10     bulletBorderColor     節點邊框顏色          graph1.bulletBorderColor = "#FFFFFF";
11     bulletBorderThickness     節點邊框寬度          graph1.bulletBorderThickness = 2;
12     customBulletField     使用者自定義節點欄位          graph.customBulletField = "bullet";
13     bulletOffset     節點偏移量          graph.bulletOffset = 16;
14     cornerRadiusTop               graph.cornerRadiusTop = 8;
15     bulletSize     節點大小          graph.bulletSize = 14;
16     colorField     顏色欄位，顏色可以從資料中讀取          graph1.colorField = "color";
17     type     影象型別，有line、column、smoothedLine型別，第一種為線形圖，第二種為柱狀圖     line /column/smoothedLine     graph1.type = "line";
18     fillAlphas     填充區透明度，預設為0，最大值為1，當設定值時，線上條跟x軸之間的區域會填充顏色          graph1.fillAlphas = 0.3;
19     negativeLineColor     當數值為負數時線條的顏色          graph1.negativeLineColor = "#efcc26";


7、     Chart （amcharts 物件）
序號     屬性名/方法名     作用     物件獲取方法/常用屬性值     示例
1     chart物件     Amcharts 的核心物件     var chart = new AmCharts.AmSerialChart();    
2     pathToImages     指定chart圖片的引用地址            chart.pathToImages = "amcharts/images/";
3     zoomOutButton     設定放大/縮小按鈕的背景色和透明度          chart.zoomOutButton = {
                              backgroundColor: '#000000',
                              backgroundAlpha: 0.15
                          };
4     dataProvider     指定資料來源，一般指向一個數組物件          chart.dataProvider = chartData;
5     categoryField     指定X軸由哪個欄位決定          chart.categoryField = "date";
6     autoMargins     自動調整邊距，如果設定為true則邊距設定不起效          chart.autoMargins = true;
7     fontSize     字型大小          chart.fontSize = 14;
8     color      圖示顏色          chart.color = "#FFFFFF";
9     marginTop      上邊距          chart.marginTop = 100;
10     marginLeft      左邊距          chart.marginLeft = 50;
11     marginRight      右邊距          chart.marginRight = 30;
12     addGraph(graph)     新增一個圖形，可以新增多個，想要繪製圖形，必須有此方法          chart.addGraph(graph1);
13     validateNow（div）     當資料改變時或者屬性改變時，想要重新繪圖，可以呼叫該方法          chart.validateNow('chartdiv');
14     chart.write('chartdiv');     將amcharts物件寫到一個div中，最常用方法          chart.chart.write('chartdiv');;
15     addListener('dataUpdated', zoomChart)     新增一個監聽函式，第一個引數是指定事件，第二個是呼叫的函式名     chart.addListener('zoomed', handleZoom);     chart.addListener('dataUpdated', zoomChart);
16     rotate      影象是否xy軸互換，預設為false，如果想讓影象順時針旋轉90°，則設定為true     False，true     chart.rotate = false;
17     depth3D     設定為3d影象的厚度值          chart.depth3D = 50
18     angle     角度，當設定影象為3d圖時使用該屬性，預設為0          chart.angle = 40
19     startDuration               chart.startDuration = 2
20     plotAreaBorderColor     繪圖區域邊框顏色          chart.plotAreaBorderColor = "#000000";
21     plotAreaBorderAlpha     繪圖區域邊框透明度          chart.plotAreaBorderAlpha = 5;
22     backgroundImage     設定背景圖片的地址          chart.backgroundImage = "amcharts/images/bg.jpg";
23     addChartScrollbar(chartScrollbar)     新增滾動條，只能新增一個          chart.addChartScrollbar(chartScrollbar);
24     addLegend(legend)     新增圖例，可以新增多個          chart.addLegend(legend);
25     addValueAxis(valueAxis1)     新增Y軸。可以新增多個          chart.addValueAxis(valueAxis1);
26     addChartCursor(chartCursor)     新增滑鼠形狀          chart.addChartCursor(chartCursor);
27                   
28                   
29                   
30                   
31                   
32                   
8、     ChartCursor（游標）
序號     屬性名/方法名     作用     物件獲取方法/常用屬性值     示例
1     chartCursor 物件     設定游標的形狀和樣式     var chartCursor = new AmCharts.ChartCursor();    
2     zoomable      是否可以縮放，設為true的時候，按住滑鼠左鍵劃線可以方法影象     True/false       chartCursor.zoomable = false;
3     cursorAlpha      游標透明度          chartCursor.cursorAlpha = 0;
4     cursorPosition      游標位置          chartCursor.cursorPosition = "mouse";
5     pan      預設為false，設定為true時，游標變為四個向外的箭頭形狀，按住左鍵滑動滑鼠可以將影象向左移動向右移動          chartCursor.pan = true;
6     categoryBalloonDateFormat      設定游標節點顯示的日期格式          chartCursor.categoryBalloonDateFormat = "JJ:NN, DD MMMM";

9、     動態圖表示例
1、需要在html頁面增加一個div，同時設定div的id和樣式，amcharts將圖表顯示在指定的id的div中
<div id="chartdiv" style="width: 50%; height: 300px"></div>
2、引用amcharts js 庫和css樣式
<script src="amcharts/amcharts.js" type="text/javascript"></script>       
<link rel="stylesheet" href="style.css" type="text/css">
3、設定一個定時器，迴圈呼叫函式
window.setInterval(show,2000);//每隔2秒呼叫一次show（）方法，show方法完成繪圖功能
function show(){
                         var chart = new AmCharts.AmSerialChart();
                         var valueAxis1 = new AmCharts.ValueAxis();
                         var graph1 = new AmCharts.AmGraph();
                         var categoryAxis = chart.categoryAxis;
                         var guide = new AmCharts.Guide();
                         var legend = new AmCharts.AmLegend();
                           var chartCursor = new AmCharts.ChartCursor();
                         //設定最大顯示數值個數
                     generateChartData();
                      chart.pathToImages = "amcharts/images/";
                          chart.zoomOutButton = {
                              backgroundColor: '#000000',
                              backgroundAlpha: 0.15
                          };
                          chart.dataProvider = chartData;
                          chart.categoryField = "date";
                          categoryAxis.parseDates = false; // as our data is date-based, we set parseDates to true
                            categoryAxis.dashLength = 1;
                           categoryAxis.gridAlpha = 0.15;
                           categoryAxis.axisColor = "#DADADA";
                          // categoryAxis.position = "top";
                           categoryAxis.gridPosition = "start";
                           categoryAxis.startOnAxis = true;
                           categoryAxis.gridColor = "#FFFFFF";               
                        // CURSOR

                           chartCursor.zoomable = false; // as the chart displayes not too many values, we disabled zooming
                           chartCursor.cursorAlpha = 0;
                           chartCursor.cursorPosition = "mouse";
                           chartCursor.pan = true; // set it to fals if you want the cursor to work in "select" mode
                           chart.addChartCursor(chartCursor);

                           valueAxis1.axisColor = "#FF6600";
                           valueAxis1.axisThickness = 1;
                           valueAxis1.gridAlpha = 0;
                           valueAxis1.tickLength =0;
                           valueAxis1.minimum = -100;
                           valueAxis1.maximum = 100;
                           valueAxis1.title="哈哈";
                           valueAxis1.logarithmic = false; // this line makes axis logarithmic
                           valueAxis1.integersOnly = true;
                           valueAxis1.gridCount = 10;
                           valueAxis1.unit = "%";
                           valueAxis1.labelsEnabled = true;
                           valueAxis1.inside = true;
                           valueAxis1.position = "left";

                           chart.addValueAxis(valueAxis1);

                        // LEGEND
                           legend.align = "center";
                           legend.marginLeft = 0;
                           legend.title="測試";
                           legend.horizontalGap = 10;
                           legend.equalWidths = false;
                           legend.valueWidth = 120;
                           chart.addLegend(legend);

                           guide.fillAlpha = 0.1;
                           guide.lineAlpha = 0;
                           guide.value = 50;
                           guide.toValue = 0;
                           guide.lineColor = "#CC0000";
                           guide.dashLength = 4;
                           guide.label = "平均值";
                           guide.inside = true;
                           guide.lineAlpha = 1;

                           var guide1 = new AmCharts.Guide();
                           guide1.lineColor = "#CC0000";
                           guide1.lineAlpha = 1;
                           guide1.dashLength = 2;
                           guide1.inside = true;
