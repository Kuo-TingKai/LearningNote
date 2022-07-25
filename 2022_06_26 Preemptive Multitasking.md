# 2022/06/26 Preemptive Multitasking

### Concurrency used in CV application

- [Mastering concurrency in python, ch8: example 5 and 6](https://github.com/PacktPublishing/Mastering-Concurrency-in-Python/tree/master/Chapter08)

### Implementation

- [asyncio(python)](https://ajing-notebook.blogspot.com/2021/11/python-asycio-intro.html)
    -  cooperative
    -  coroutine
        -  generator and **yield**
    -  event loop

- [linux kernel: **yield**](https://www.coolcou.com/linux-kernel/linux-process-scheduling-kernel-api/the-linux-kernel-yield.html)

- [**cocurrency in python: cooperative vs preemptive**](https://medium.com/fullstackai/concurrency-in-python-cooperative-vs-preemptive-scheduling-5feaed7f6e53)
    - bholley(Bobby Holley): [must to be this tall to write multi-threaded code](https://bholley.net/blog/2015/must-be-this-tall-to-write-multi-threaded-code.html)
        - [David Baron](https://dbaron.org/)

- [**Trio**(python)](https://trio.readthedocs.io/en/stable/)
- [cyrui(python)](https://curio.readthedocs.io/en/latest/)
- [greenlet(python)](https://greenlet.readthedocs.io/en/latest/)

---

### WIKI Reference

- [**preemptive multitasking** wiki](https://zh.m.wikipedia.org/w/index.php?title=%E6%8A%A2%E5%8D%A0%E5%BC%8F%E5%A4%9A%E4%BB%BB%E5%8A%A1%E5%A4%84%E7%90%86&oldformat=true&variant=zh-mo)
    - [time slicing](https://zh.m.wikipedia.org/zh-mo/%E6%97%B6%E9%97%B4%E7%89%87)
        - [**nice value**](https://zh.m.wikipedia.org/zh-tw/Nice%E5%80%BC)
    - [process](https://zh.m.wikipedia.org/zh-mo/%E8%A1%8C%E7%A8%8B)
        - [time-sharing](https://zh.m.wikipedia.org/zh-mo/%E5%88%86%E6%99%82%E7%B3%BB%E7%B5%B1)
            - [port](https://zh.m.wikipedia.org/zh-mo/%E4%BB%8B%E9%9D%A2_(%E8%B3%87%E8%A8%8A%E7%A7%91%E6%8A%80)#%E7%A1%AC%E9%AB%94%E4%BB%8B%E9%9D%A2)
                - [bus](https://zh.m.wikipedia.org/zh-mo/%E6%80%BB%E7%BA%BF)
                    - [address bus](https://zh.m.wikipedia.org/zh-mo/%E4%BD%8D%E5%9D%80%E5%8C%AF%E6%B5%81%E6%8E%92)
                    - [control bus](https://zh.m.wikipedia.org/zh-mo/%E6%8E%A7%E5%88%B6%E5%8C%AF%E6%B5%81%E6%8E%92)
                        - [direct memory access](**https://zh.m.wikipedia.org/zh-mo/%E7%9B%B4%E6%8E%A5%E8%A8%98%E6%86%B6%E9%AB%94%E5%AD%98%E5%8F%96**)
                            - [interupt](https://zh.m.wikipedia.org/zh-mo/%E4%B8%AD%E6%96%B7)
                                - [**context switch**](https://zh.m.wikipedia.org/zh-mo/%E4%B8%8A%E4%B8%8B%E6%96%87%E4%BA%A4%E6%8F%9B)
                                    - [address space](https://zh.m.wikipedia.org/zh-mo/%E5%AE%9A%E5%9D%80%E7%A9%BA%E9%96%93)
                                        - [**NUMA(non-uniform memory access**)](https://zh.m.wikipedia.org/zh-mo/%E9%9D%9E%E5%9D%87%E5%8C%80%E8%AE%BF%E5%AD%98%E6%A8%A1%E5%9E%8B)
                                            - [SMP(symmetric multiprocessing)](https://zh.m.wikipedia.org/zh-mo/%E5%AF%B9%E7%A7%B0%E5%A4%9A%E5%A4%84%E7%90%86)
                                - [**fiber**](https://zh.m.wikipedia.org/zh-mo/%E7%BA%96%E7%A8%8B) 
                            - [**ISA(instruction set architecture)**](https://zh.m.wikipedia.org/zh-mo/%E6%8C%87%E4%BB%A4%E9%9B%86%E6%9E%B6%E6%A7%8B)
                            - [register](https://zh.m.wikipedia.org/zh-mo/%E5%AF%84%E5%AD%98%E5%99%A8)
                                - [**memory hierarchy**](https://zh.m.wikipedia.org/zh-mo/%E8%A8%98%E6%86%B6%E9%AB%94%E9%9A%8E%E5%B1%A4)
                                    - [cache](https://zh.m.wikipedia.org/zh-mo/%E7%BC%93%E5%AD%98)
                        - [**bus contention**](https://zh.m.wikipedia.org/zh-mo/%E6%80%BB%E7%BA%BF%E7%AB%9E%E4%BA%89) 
            - [computer multitasking](https://zh.m.wikipedia.org/zh-mo/%E5%A4%9A%E4%BB%BB%E5%8A%A1%E5%A4%84%E7%90%86#%E5%A4%9A%E9%81%93%E7%A8%8B%E5%BA%8F)

- [cooperative multitasking](https://zh.m.wikipedia.org/zh-tw/%E5%8D%8F%E4%BD%9C%E5%BC%8F%E5%A4%9A%E4%BB%BB%E5%8A%A1)
- [processor affinity](https://zh.wikipedia.org/zh-tw/%E5%A4%84%E7%90%86%E5%99%A8%E4%BA%B2%E5%92%8C%E6%80%A7)

---

[Virtual memory(linux study group hackmd)](https://hackmd.io/@combo-tw/Linux-%E8%AE%80%E6%9B%B8%E6%9C%83/%2F%40combo-tw%2FBJlTwJUABB)