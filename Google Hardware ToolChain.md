#  Google Hardware ToolChain 

###### tags: `IC design`
> [name=<img src = "https://i.imgur.com/FiXNhGv.png" width ="25">] [time=2022 07 20] [color=#907bf7]



- <img src="https://i.imgur.com/IcD6vvU.png" alt="drawing" width="20"/> [skywater pdk](https://github.com/google/skywater-pdk/)
    - [micromamba](https://mamba.readthedocs.io/en/latest/user_guide/micromamba.html)

- git clone --depth 1 : accelerate download speed

- [review tcl wiki](https://zh.wikipedia.org/zh-tw/Tcl)
    - [RAD(rapid application development)](https://zh.wikipedia.org/zh-tw/%E5%BF%AB%E9%80%9F%E6%87%89%E7%94%A8%E7%A8%8B%E5%BC%8F%E9%96%8B%E7%99%BC)
    - [*review* Polish notation](https://zh.wikipedia.org/zh-tw/%E6%B3%A2%E5%85%B0%E8%A1%A8%E7%A4%BA%E6%B3%95a)
    - [*review* mixin](https://zh.wikipedia.org/zh-tw/Mixin)
> Mixin是物件導向程式設計語言中的類，提供了方法的實現。其他類可以存取mixin類的方法而不必成為其子類。[1]Mixin有時被稱作"included"而不是"inherited"。mixin為使用它的class提供額外的功能，但自身卻不單獨使用（不能單獨生成實例物件，屬於抽象類）。因為有以上限制，Mixin類通常作為功能模組使用，在需要該功能時「混入」，而且不會使類的關係變得複雜。使用者與Mixin不是「is-a」的關係，而是「-able」關係
Mixin有利於代碼復用[2]又避免了多繼承的複雜。[3][4]使用Mixin享有單一繼承的單純性和多重繼承的共有性。介面與mixin相同的地方是都可以多繼承，不同的地方在於mixin是帶實現的。Mixin也可以看作是帶實現的interface。這種設計模式實現了依賴反轉原則。[5]
- [tcl gitbook](http://tw.gitbook.net/tcl/tcl_special_variables.html)

- review CVC(code validity checker) and Klayout(support GDB and Oasis)



## <img src="https://i.imgur.com/CuLAW0m.png" alt="drawing" width="30"/> Trouble Shooting 
- Issue was [reported](https://github.com/chipsalliance/silicon-notebooks/issues/7)

```cmd=
Extracting         0%error    libmamba Failed to download package from https://conda.anaconda.org/main/linux-64/_libgcc_mutex-0.1-main.tar.bz2 (status 403)
_libgcc_mutex                                      366.0 B @   1.2kB/s  0.3s
critical libmamba Multi-download failed. Reason: Transfer finalized, status: 403 [https://conda.anaconda.org/main/linux-64/_libgcc_mutex-0.1-main.tar.bz2] 366 bytes

                                           __
          __  ______ ___  ____ _____ ___  / /_  ____ _
         / / / / __ `__ \/ __ `/ __ `__ \/ __ \/ __ `/
        / /_/ / / / / / / /_/ / / / / / / /_/ / /_/ /
       / .___/_/ /_/ /_/\__,_/_/ /_/ /_/_.___/\__,_/
      /_/
```

```cmd=
couldn't read file "/content/conda-env/share/pdk/sky130A/libs.tech/openlane/config.tcl": no such file or directory
    while executing
"source $pdk_config"
    (procedure "prep" line 165)
    invoked from within
"prep {*}$args"
    (procedure "run_non_interactive_mode" line 12)
    invoked from within
"run_non_interactive_mode {*}$argv"
    invoked from within
"if { [info exists flags_map(-interactive)] || [info exists flags_map(-it)] } {
    if { [info exists arg_values(-file)] } {
        run_file [file nor..."
    (file "/content/OpenLane/flow.tcl" line 384) 
```
> [time=2022 07 21][color=#907bf7]更新
- Intel Math Kernel Library (MKL)
- **Trouble Shooting**❌: In vscode, cannot import entire functions of devsim but in cmd can. 
- tip: ```python xxx.py>log.txt ``` :+1: 
- ```inkscape --export-pdf=output.pdf input.eps```


```bash=
add_1d_mesh_line(...)
    devsim.add_1d_mesh_line (mesh, tag, pos, ns, ps)

    Add a mesh line to a 1D mesh

    Parameters
    ----------
    mesh : str
       Mesh to add the line to
    tag : str, optional
       Text label for the position
    pos : str
       Position for the mesh point
    ns : Float, optional
       Spacing from this point in the negative direction (default ps value)
    ps : Float
       Spacing from this point in the positive direction
```


```bash= 
SetParameters(device, region)
    Set parameters for 300 K
```

```bash=
set_parameter(...)
    devsim.set_parameter (device, region, name, value)

    Set a parameter on region, device, or globally

    Parameters
    ----------
    device : str, optional
       The selected device
    region : str, optional
       The selected region
    name : str
       Name of the parameter name being retrieved
    value : any
       value to set for the parameter

    Notes
    -----

    Note that the device and region options are optional.  If the region is not spec
```

🎥 Youtube: [skywater 130 pdk install](https://www.youtube.com/watch?v=KgBLByOkJxA) 