# AE/ exposure stabalization

- (2022/06/16 Update) 如果要用最優控制的話，我犯了一個低級錯誤:應該要加的是控制輸入的隨時間累積項而不是瞬時項...這個跟力學控制不太一樣，因為我們不是直接施力在機構上面，而是調整感測器參數以控制畫面像素值分布，但沒辦法直接控制環境照度，可以的話我就是上帝了。而且exposure也要有記憶性。


[gekko](https://gekko.readthedocs.io/en/latest/examples.html)

[optimal control wiki](https://zh.wikipedia.org/wiki/%E6%9C%80%E4%BC%98%E6%8E%A7%E5%88%B6)

[Kalman filter](https://zh.wikipedia.org/wiki/%E5%8D%A1%E5%B0%94%E6%9B%BC%E6%BB%A4%E6%B3%A2)

[LQR](https://zh.wikipedia.org/wiki/LQR%E6%8E%A7%E5%88%B6%E5%99%A8#%E6%9C%89%E9%99%90%E6%99%82%E9%96%93%E9%95%B7%E5%BA%A6%EF%BC%8C%E9%9B%A2%E6%95%A3%E6%99%82%E9%96%93%E7%9A%84LQR)

build up (intg,lux,brightness)的landscape
[python-control(princeton)](https://web.math.princeton.edu/~cwrowley/python-control/index.html)

[**ml dp**](https://ml-adp.readthedocs.io/en/latest/guide.html)
[**OT**](https://github.com/dfdazac/wassdistance/blob/master/sinkhorn.ipynb)
對於完全靜態景物似乎沒用...
[**POT**](https://pythonot.github.io/auto_examples/index.html)
[**python stabalization analysis**](https://www.halvorsen.blog/documents/programming/python/resources/powerpoints/Stability%20Analysis%20of%20Control%20Systems%20with%20Python.pdf)

[pathfollowing](https://github.com/Karthikeyanc2/Pure-Pursuit-Geometric-controller-for-Lateral-Control/blob/master/pathfollowing.py)

[pygame](https://stackoverflow.com/questions/51050257/distributed-1-21-8-requires-msgpack-which-is-not-installed)
[pygame2](https://github.com/microsoft/pylance-release/blob/main/DIAGNOSTIC_SEVERITY_RULES.md#diagnostic-severity-rules)
[pygame3](https://stackoverflow.com/questions/18317521/importerror-no-module-named-pygame)

[pythonlinearnonlinearcontrol](https://github.com/Shunichi09/PythonLinearNonlinearControl)

[control](https://python-control.readthedocs.io/en/latest/optimal.html)

[py matlab control](https://blog.csdn.net/jiyotin/article/details/114110001)

[py control zhihu](https://www.zhihu.com/column/c_1385910766168555520)

[py stochastic control](https://www.796t.com/post/N2Vrd20=.html)

[scipy control](https://www.pythonheidong.com/blog/article/534448/2fe3b731c31f0c53bc8d/)

