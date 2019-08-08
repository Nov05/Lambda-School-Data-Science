2019-08-07  

Lambda School Learning Kit  
Containers and Reproducible Builds  
https://learn.lambdaschool.com/ds/module/recLjxZbBV3Jmrj2T/  

Install Docker Desktop for Windows  
https://docs.docker.com/docker-for-windows/install/  
Install Docker Toolbox on Windows (for no Hyper-V versions)  
https://docs.docker.com/toolbox/toolbox_install_windows/  

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

## 2. Check whether your Windows has Hyper-V

> -> in Start Menu Search type `turn windows features on or off`
> -> check whether there is `Hyper-V` option

if not, it means your windows version doesn't have it, you might need to upgrade it to Pro  
you can upgrade your windows with a Pro product key  
https://blog.csdn.net/hce1478506318/article/details/80863274  
http://www.xitongzu.com/jc/6574.html  

## 3. Once upgraded, check the `Hyper-V` option, 
then in the `Administrator: Command Prompt` -> `system info`, 
you should be able to see the follow information

## 4. install docker for windows


