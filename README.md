# busSystem
a system of bus

### 那些年，走过的坑
一开始的解决方法是想办法去判断什么时候公交的线路该拐，所以我想画图来解决，开始的图入下：
```
  1····2····3····4····5
                      ·
                      ·
                      ·
                      ·
 10····9····8····7····6
 ·
 ·
 ·
 ·
 11····12····13····14····15
                          ·
                          ·
                          ·
                          ……
                          
 ```
                          

但是这样并不能解决线到底从哪开始画，从哪开始拐到哪里结束的问题。所以我想了一下，根据canvas画图的原理，只要把所有的点先按照顺序求出坐标放到数组里面，然后遍历数组绘图就可以了，canvas不用关系到哪里拐，只要根据数组里面的点画出相应的路线就可以，所以我就又修改了一下路线图
```

[mire ,mire ]  ····  [2mire ,mire ]  ····  [3mire ,mire ]  ····  [4mire ,mire ]  ····  [5mire ,mire ]
                                                                                              ·
                                                                                              ·
                                                                                              ·
                                                                                              ·
[mire ,2mire ] ····   [2mire ,2mire ] ···· [3mire ,2mire ] ····  [4mire ,2mire ] ····  [5mire ,2mire ]
      ·
      ·
      ·
      ·
[mire ,3mire ] ····   [2mire ,3mire ] ···· [3mire ,3mire ] ····  [4mire ,3mire ] ····  [5mire ,3mire ]
                                                                                              ·
                                                                                              ·
                                                                                              ·
                                                                                              ·
                                                                                              ……
                                                                                              
```                                                                                              
所以，我只要根据一定的mire求出所有点的坐标，先moveto第一个点，然后按照顺序一直lineto下一个点就好了                                                                                              
                                                                                            


