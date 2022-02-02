# Herramientas para desarrollo con C++

## Instalar MinGW-w64  

### Descargue MinGW-64

[Descargue Aqui](https://drive.google.com/drive/folders/1sb-pCBB3WD7k7LCvp82lPWTPKnfclbop?usp=sharing)

En caso que no funcione el instalador anterior, utilice [este](https://github.com/msys2/msys2-installer/releases/download/2022-01-18/msys2-x86_64-20220118.exe)
Siguiendo estas [instrucciones](https://code.visualstudio.com/docs/cpp/config-mingw)



### Ejecutar el instalador
Ejecute `mingw-w64-install.exe`  
Click siguiente  
Cambie la Arquitectura de `i868` a `x86_64`  
![](https://i.imgur.com/GnRorz7.png)  
Click siguiente y mantenga la ubicación predeterminada
Click siguiente e iniciar la instalación
Click Finalizar para salir del instalador
### Despues de instalar, agregue un link a la carpeta  
Abra una ventana de comando como ADMINISTRADOR
* tecla windows -> escriba "cmd"  
* click derecho "Simbolo de sistema"  
* Ejecutar como administrador

### Win64

Copie y pegue el siguiente comando para crear el link a la carpeta MinGW en C:\  
`mklink /J C:\MinGW "C:\Program Files\mingw-w64\x86_64-8.1.0-posix-seh-rt_v6-rev0\mingw64"`  

### Win32

Copie y pegue el siguiente comando para crear el link a la carpeta MinGW en C:\  
`mklink /J C:\MinGW "C:\Program Files\mingw-w64\i686-8.1.0-posix-dwarf-rt_v6-rev0\mingw32"`


### Agregue MinGW al system PATH   
Copie y pegue los siguientes comandos
`set PATH=%PATH%;C:\MinGW\bin`  
`setx /M PATH "%PATH%"`  
Revise si la instalación es correcta
`g++ --version` debe poder ver lo siguiente:
![](https://i.imgur.com/x4LidWQ.png)  
