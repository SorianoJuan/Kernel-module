# Kernel-module
Kernel Module - SO 1

Instrucciones de uso: 
-Hacer make en la carpeta del encrypter y del decrypter

-Dentro de las respectivas carpetas, insertar los modulos del kernel con sudo insmod encrypter.ko/decrypter.ko

-Dentro de la carpeta del encrypter, ejecutar <<sudo mknod -m 0666 /dev/decrypter c 1717 0>>

-Dentro de la carpeta del decrypter, ejecutar <<sudo mknod -m 0666 /dev/decrypter c 1718 0>>

-Ingresar algo al device file con pipe o demás, por ejemplo <<echo 1234 > /dev/encrypter>>

-Leer el device file, se le suma 2 a los caracteres ingresados, por lo tanto debería leerse 3456 <<cat /dev/encrypter>>

-Redireccionar lo ingresado en el encrypter al decrypter <<cat /dev/encrypter > /dev/decrypter>>

-Leer el device file del decrypter, debera salir los caracteres originales 1234 ><cat /dev/decrypter>>
