 # <p align= "center"> :books: _RVfpga SoC THE IMAGINATION UNIVERSITY PROGRAMME_ :books: </p>
 
:pushpin: _Imagiation technologies_ es una empresa Britanica dedicada al diseño de software y semiconductores, esta empresa cuenta con un programa universitarios que brinda al estudiante materiales de apoyo, guias de referencia y ejercios de laboratorio, además las herramientas para desarrollo de software son gratuitas y cuentan cn una plataforma de hardware a un precio razonable, todo con el fin de que halla una enseñanza genuina para el estudiante.
 
Para iniciar el curso de _RVfpga SoC_ se desarrollan un conjuto de laboratorios con el fin de adquirir conocimientos.
En este informe se va a realizar el desarrollo del lab1 y lab2 respectivamente.

El primero paso a seguir es registrarse en la pagina web de _imagination university program_ y solicitar el envio del material correspondiente, posteriormente se incio la lectura de la guia para iniciar la instalación y desarrollo de los laboratorios.

El software que se debe instalar para el desarrollo de los laboratorios es el siguiente:

 * :black_nib: _Vivado_ 
 * :black_nib: _Cable Drivers_
 * :black_nib: _Digilent Board Files_
 * :black_nib: _VS code_
 * :black_nib: _PlatformIO on top of VSCode_
 * :black_nib: _GTKVWave_
 * :black_nib: _Verilator_
  

### :large_orange_diamond: LABORATORIO 1 - INTRODUCCIÓN A _RVfpga-Soc_
* Para inciar el desarrollo de este laboratorio primero se hizo la lectura incial en la guia de forma que se fuera entendiendo como funciona _RVfpga-SoC_, además de ir conociendo sus caracteristicas principales, posteriormente se fueron conociendo los requerimientos necesarios para el correcto desarrollo del laboratorio.
 
 Primero se iniciara con el desarrollo de la guia por lo tanto se creara un proyecto en vivado: 

<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/073427536581c14a7dcc519191a407ddf5a3ae89/Im%C3%A1genes/Screenshot%20from%202022-03-06%2015-27-54.png" alt="modulo" width="500"/>
</p>

Ahora se deben incluir los directorios, los archivos y así dejar creado el proyecto.

* Luego se definen algunos archivos de manera global, como se puede observar en la figura. También se debe asignar el archivo _rvfpga.sv_ como _"top"_.
<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/10ceab68894be5e6ab13573844f50aaf18fbfe8e/Im%C3%A1genes/Screenshot%20from%202022-03-06%2018-22-41.png" alt="modulo" width="400"/>
</p>
<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/10ceab68894be5e6ab13573844f50aaf18fbfe8e/Im%C3%A1genes/Screenshot%20from%202022-03-06%2018-32-28.png" alt="modulo" width="400"/>
</p>

Se deben definir de esta manera, es decir, globales los siguientes archivos:

 * common_defines.vh
 * assign.svh
 * registers.svh
 * typedef.svh
 
Mediante la herramiento de Diseño de Bloques llamado BD, se crea un espacio de trabajo en blanco donde se pueden agregar bloques como el de la figura:
<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/18b41a04b81fd2621903e8d3899d51664c39f2ea/Im%C3%A1genes/Screenshot%20from%202022-03-06%2018-36-53.png"/>
</p>

Esto se debe realizar para los siguientes bloques:


 * _swerv_wrapper_verilog_
 * _intcon_wrapper_bd_
 * _bootrom_wrapper_
 * _syscon_wrapper_
 * _bidirec_ (En 32 ocaciones) 

Se procede a realizar las respectivas conexiones tanto internas (corresponde a conexiones entre los bloques), como externas (señales que provienen de manera externa). Luego de realizar cada una de las conexiones requeridas se plantea un diseño de esquemático como el que se puede observar en la siguiente figura: 

<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/ff9088e116703afc03ac4f4b44b5fb3902b39b47/Im%C3%A1genes/Screenshot%20from%202022-03-06%2020-32-55.png"/>
</p>

Finalizado este paso, a partir del archibo _BD.bd_, se crea el archivo verilog el cual contiene las conexiones de todos los bloques.

* Con los resultados anteriores, se va a generar el _bitstream_, para ellos incialmente se tienen que realizar las siguientes modificaciones sobres las configuraciones en vivado, como se puede observar en la figura.

<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/c7ee3ebc16cc1986ad42da0d897b7c13d6281938/Im%C3%A1genes/Screenshot%20from%202022-03-06%2021-26-42.png"/>
</p>

 :heavy_check_mark: Finalmente, después de haber realizado el _bitstream_, se puede observar que este y la sintesis se realizaron de manera correcta, como lo muestra la figura.
<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/c7ee3ebc16cc1986ad42da0d897b7c13d6281938/Im%C3%A1genes/Screenshot%20from%202022-03-06%2022-44-06.png"/>
</p>

### :large_orange_diamond: LABORATORIO 2 - CORRIENDO UN PROGRAMA DE PRUEBA EN _RVfpga-Soc_
Para inciar el desarrollo del segundo laboratorio se realizo la respectiva lectura de la guia correspondiente al laboratorio 2 de manera que se fueran entendiendo los conceptos y el paso a paso para realizar este laboratorio.

* Se debe obtener el archivo _verilog BD.v_ del laboratorio anterior y llevarlo a la siguiente ubicación:  
#### <p align="center"> [RVfpgaSoCPath]/RVfpgaSoC/Labs/LabResources/Lab2/src/SweRVolfSoC/. </p>

 En esta ubicación se debe corroborrar que los modulos dentro del archivo _verilog_, terminen en 0_0, como se observa en las siguientes figuras:

<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/ba23f66f7315943cc86921ef832bdf7d636be216/Im%C3%A1genes/Screenshot%20from%202022-03-07%2010-40-13.png"/>
</p>

<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/62d9690599bd853af054f6fd9fdbd91ed2572553/Im%C3%A1genes/Screenshot%20from%202022-03-07%2010-40-23%20(1).png"/>
</p>

<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/ba23f66f7315943cc86921ef832bdf7d636be216/Im%C3%A1genes/Screenshot%20from%202022-03-07%2010-40-30.png"/>
</p>

<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/a0c7591137a16262592e7c75499dd809da946fd7/Im%C3%A1genes/Screenshot%20from%202022-03-07%2010-40-41.png"/>
</p>

Con esta comprobación realizada, se procede a la creación del archivo _Vrvfpgasim_, mediante los siguientes códigos:

* `cdcd [RVfpgaSoCPath]/RVfpgaSoC/Labs/LabResources/Lab2/verilatorSIM`
* `make clean`
* `make`

Así se obtiene el resultado en la terminal que se observa en la siguiente figura yse observa que ya el archivo está creado.

<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/ba23f66f7315943cc86921ef832bdf7d636be216/Im%C3%A1genes/Screenshot%20from%202022-03-07%2011-11-52.png"/>
</p>

* Posteriormente se abre el _visual basic code_ en la carpeta que cuenta con la siguiente direccion:

##### <p align="center"> [RVfpgaSoCPath]/RVfpgaSoC/Labs/LabResources/Lab2/examples/ </p>

Luego se abre el archivo _PlatformIO.ini_ y se modifica redireccionando la linea 21:

##### <p align="center"> home/user/RVfpgaSoC/Labs/LabResources/Lab2/verilatorSIM/Vrvfpgasim </p>

Las direcciones de las varibles que se van a observar en el _GTKWave_ son las siguientes: 

* _TOP rvfpgasim swervolf swerv_wrapper_verilog_0 swerv_eh1_2 swerv ifu(clk,ifu_i0_instr[31:0],ifu_i1_instr[31:0])_
* _TOP rvfpgasim swervolf swerv_wrapper_verilog_0 swerv_eh1_2 swerv dec arf gpr_banks(0) gpr(28) gprff (dout[31:0])_

Las variables a mostrar son las que se encuentran en parentesis.


:heavy_check_mark: Finalmente se pueden observar los resultados en _GTKWave_ donde las variables nos muestran los resultados esperados en la siguiente figura:

<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/c3741e68eb663f32c510e4e9023f44afb101304f/Im%C3%A1genes/o.png"/>
</p>


### CONCLUSIONES :heavy_check_mark:

* Se entendió el procedimiento desde la asignación de los archivos globales, como archivos principales del proyecto, hasta la generación de la traza.
* Se logró obtener la salida de la instrucción esperada en el procesador en el tiempo entre los 10 [fs] y 100 [fs].
* La señal de salida observada se puede observar en los tiempos de 10 [fs] y 100 [fs] y 10 [ns] y 100 [ns] (tiempo sugerido en la guia).
* El archivo trace.vcd debió moverse a una ubicación sin restricciones para poder ser corrido en Gtkwave.
* El software Visal Code debe ser abierto como superusuario para poder correr el IDE PlatformIO.


### REFERENCIAS :dart:
* [Imagination university program](https://university.imgtec.com/)
* [Vivado](https://www.xilinx.com/support/download.html)
* [Visual Basic Code](https://code.visualstudio.com/)
* [Verilator](https://www.veripool.org/verilator/)

#### UNIVERSIDAD INDUSTRIAL DE SANTANDER :mortar_board:
* :woman: Angela Yulieth Rivera Gómez - 2162467
* :man: Vladimir Sebastian Villamizar Anaya - 2171522




