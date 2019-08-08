2019-08-07  

Lambda School Learning Kit  
Containers and Reproducible Builds  
https://learn.lambdaschool.com/ds/module/recLjxZbBV3Jmrj2T/  

Install Docker Desktop for Windows  
https://docs.docker.com/docker-for-windows/install/  
Install Docker Toolbox on Windows (for no Hyper-V versions)  
https://docs.docker.com/toolbox/toolbox_install_windows/  

Install Hyper-V on Windows 10  
https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v  

Get started with Docker for Windows  
https://docs.docker.com/docker-for-windows/  

# Windows 8 or Windows 10

## 1. Check whether your system hardware supports Hyper-V

> -> in Start Menu Search type `cmd`    
> -> right click on `Command Prompt` and select `Run as administrator`    
> -> in the commond prompt, type `system info`  

you should be able to see the following information, 
which means your system hardware supports `Hyper-V`,
and you will be able to install `Docker Desktop for Windows` app,
or you will have to install `Docker Toolbox`

```
Hyper-V Requirements:      VM Monitor Mode Extensions: Yes
                           Virtualization Enabled In Firmware: Yes
                           Second Level Address Translation: Yes
                           Data Execution Prevention Available: Yes
```
<img src="https://github.com/Nov05/pictures/blob/master/pic001/2019-08-07%2022_03_17-Install%20Docker%20Toolbox%20on%20Windows%20_%20Docker%20Documentation.png?raw=true" width="500">  

## 2. Check whether your Windows has Hyper-V

> -> in Start Menu Search type `turn windows features on or off`  
> -> check whether there is `Hyper-V` option  

if not, it means your windows version doesn't have it, you might need to upgrade it to Pro  
you can upgrade your windows with a Pro product key  
https://blog.csdn.net/hce1478506318/article/details/80863274  
http://www.xitongzu.com/jc/6574.html  

<img src="https://github.com/Nov05/pictures/blob/master/pic001/2019-08-07%2022_24_05-Windows%20Features.png?raw=true" width="400">  

## 3. Once upgraded, tick the `Hyper-V` option   
> in the `Administrator: Command Prompt` -> `system info`       
you should be able to see the follow information

<img src="https://github.com/Nov05/pictures/blob/master/pic001/2019-08-07%2022_33_08-Editing%20Lambda-School-Data-Science_2019-08-07%20hyper-v_docker%20desktop%20app.md%20at%20m.png?raw=true" width="600">

> Start Menu Search `device manager`    
you should be able to see the Hyper-V network adapters.  

<img src="https://github.com/Nov05/pictures/blob/master/pic001/2019-08-07%2022_31_58-Device%20Manager.png?raw=true" width="300"> 
                       
## 4. Install docker for windows  


