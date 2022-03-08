 # <p align= "center"> :books: _RVfpga SoC THE IMAGINATION UNIVERSITY PROGRAMME_ :books: </p>
 
_Imagiation technologies_ es una empresa Britanica dedicada al diseño de software y semiconductores, esta empresa cuenta con un programa universitarios que brinda al estudiante materiales de apoyo, guias de referencia y ejercios de laboratorio, además las herramientas para desarrollo de software son gratuitas y cuentan cn una plataforma de hardware a un precio razonable, todo con el fin de que halla una enseñanza genuina para el estudiante.
 
Para iniciar el curso de RVfpga SoC se desarrollan un conjuto de laboratorios con el fin obtener buenos conocimientos.
En este informe se va a realizar el desarrollo del lab1 y lab2 respectivamente.

El primero paso a seguir es registrarse en la pagina web de imagination university program y solicitar el envio del mataerial correspondiente, posteriormente se incio la lectura de la guia para iniciar la instalación y desarrollo de los laboratorios.

Ahoase va a instalar el software necesario para el desarrollo de los laboratorios es el siguiente:

 * :black_nib: Vivado 
 * :black_nib: _Cable Drivers_
 * :black_nib: _Digilent Board Files_
 * :black_nib: _VS code_
 * :black_nib: _PlatformIO on top of VSCode_
 * :black_nib: GTKVWave
 * :black_nib: Verilator
  

### :large_orange_diamond: LABORATORIO 1 - INTRODUCCIÓN A RVfpga-Soc
Para inciar el desarrollo de este laboratorio iniciamos con la lectura incial en la guia de forma que se fuera entendiendo como funciona _RVfpga-SoC_, además de ir conociendo sus caracteristicas principales, posteriormente se fueron conociendo los requerimientos necesarios para el correcto desarrollo del laboratorio.
 
Primero se iniciara con el desarrollo de la guia por lo tanto se creara un proyecto en vivado: 

<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/073427536581c14a7dcc519191a407ddf5a3ae89/Im%C3%A1genes/Screenshot%20from%202022-03-06%2015-27-54.png" alt="modulo" width="500"/>
</p>

Luego se definen diferentes caracteristicas en el proyecto creado como las que se pueden observar a continuación:

<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/10ceab68894be5e6ab13573844f50aaf18fbfe8e/Im%C3%A1genes/Screenshot%20from%202022-03-06%2018-22-41.png" alt="modulo" width="400"/>
</p>
<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/10ceab68894be5e6ab13573844f50aaf18fbfe8e/Im%C3%A1genes/Screenshot%20from%202022-03-06%2018-32-28.png" alt="modulo" width="400"/>
</p>
 
Iniciamos añadiendo algunos bloques en el espacio de diseño, uno de ellos es el _swerv_wrapper_verilog0_:

<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/18b41a04b81fd2621903e8d3899d51664c39f2ea/Im%C3%A1genes/Screenshot%20from%202022-03-06%2018-36-53.png"/>
</p>

Luego de realizar cada una de las conexiones requeridas obtenemos un diseño como el que se puede observar en la siguiente imagen: 

<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/ff9088e116703afc03ac4f4b44b5fb3902b39b47/Im%C3%A1genes/Screenshot%20from%202022-03-06%2020-32-55.png"/>
</p>

Ahora se va a generar el _bit stream_: 

<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/c7ee3ebc16cc1986ad42da0d897b7c13d6281938/Im%C3%A1genes/Screenshot%20from%202022-03-06%2021-26-42.png"/>
</p>

Finalmente se puede observar que se obtuvo el _bit stream_ y la sintesis correctamente: 

<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/c7ee3ebc16cc1986ad42da0d897b7c13d6281938/Im%C3%A1genes/Screenshot%20from%202022-03-06%2022-44-06.png"/>
</p>

### :large_orange_diamond: LABORATORIO 2 - CORRIENDO EL SOFTWARE EN _RVfpga-Soc_
Para inciar el desarrollo del segundo laboratorio se realizo la respectiva lectura de la guia de manera que se conocieran y entendieran los requerimientos necesarios para la implementación.

* Se debe obtener el archivo verilog BD.v del laboratorio anterior y llevarlo a la ubicación  
#### [RVfpgaSoCPath]/RVfpgaSoC/Labs/LabResources/Lab2/src/SweRVolfSoC/.

 En esta ubicación se debe corroborrar que los modulos dentro del archivo verilog, terminen en 0_0, como se observa en las siguientes figuras:

<p align="center"> 
 <img src="https://github.com/Computer-Architecture-I-UIS/project-rivera-villamizar/blob/5fb83562aa8dccc5db3205ccfa065064efe62e14/Im%C3%A1genes/Screenshot%20from%202022-03-07%2010-40-13.png"/>
</p>

<p align="center"> 
 <img src="https://github.com/Computer-Architecture-I-UIS/project-rivera-villamizar/blob/5fb83562aa8dccc5db3205ccfa065064efe62e14/Im%C3%A1genes/Screenshot%20from%202022-03-07%2010-40-23.png"/>
</p>

<p align="center"> 
 <img src="https://github.com/Computer-Architecture-I-UIS/project-rivera-villamizar/blob/5fb83562aa8dccc5db3205ccfa065064efe62e14/Im%C3%A1genes/Screenshot%20from%202022-03-07%2010-40-30.png"/>
</p>

<p align="center"> 
 <img src="https://github.com/Computer-Architecture-I-UIS/project-rivera-villamizar/blob/5fb83562aa8dccc5db3205ccfa065064efe62e14/Im%C3%A1genes/Screenshot%20from%202022-03-07%2010-40-41.png"/>
</p>

Ya con esta comprobación realizada, se realiza la creación del archivo _Vrvfpgasim_, mediante los siguientes códigos:

* ´cdcd´ [RVfpgaSoCPath]/RVfpgaSoC/Labs/LabResources/Lab2/verilatorSIM
* ´make clean´
* ´make´

Con esto se obtiene el resultado en la terminal que se observa en la figura y ya el archivo está creado.

<p align="center"> 
 <img src="https://github.com/Computer-Architecture-I-UIS/project-rivera-villamizar/blob/1b90377250b4951d5dbc3e386ae80e207a531ac5/Im%C3%A1genes/Screenshot%20from%202022-03-07%2011-11-52.png"/>
</p>

Posteriormente se abre el visual basic code en la carpeta que cuenta con la siguiente direccion:
##### [RVfpgaSoCPath]/RVfpgaSoC/Labs/LabResources/Lab2/examples/ 
Luego se abre el archico PlatformIO.ini y se modifica la linea 21 colocando la siguiente redireccion:
##### home/user/RVfpgaSoC/Labs/LabResources/Lab2/verilatorSIM/Vrvfpgasim

Las direcciones de las varibles que se van a observar en el _GTKWave_ son las siguientes: 
* TOP rvfpgasim swervolf swerv_wrapper_verilog_0 swerv_eh1_2 swerv ifu(clk,ifu_i0_instr[31:0],ifu_i1_instr[31:0])
* TOP rvfpgasim swervolf swerv_wrapper_verilog_0 swerv_eh1_2 swerv dec arf gpr_banks(0) gpr(28) gprff (dout[31:0])

Las variables a mostrar son las que se encuentran en parentesis.


:heavy_check_mark: Finalmente se pueden observar los resultados en GTKWave donde las variables nos muestran los resultados esperados:

<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/c3741e68eb663f32c510e4e9023f44afb101304f/Im%C3%A1genes/o.png"/>
</p>


### CONCLUSIONES :heavy_check_mark:

* Se pudo ejecutar el programa de prueba AL_Operations en el procesador y observar su comportamiento mediante GtkWave.
* Mediante el uso de vivado se pudo sintetizar el diseño para generar el archivo verilog del procesador para realizar la simulación.
* Se debió abrir el Visual Code como super usario para poder realizar la traza.
* El archivo trace.vcd debió moverse a una ubicación sin restricciones para poder ser corrido en Gtkwave.

### REFERENCIAS :paperclip:
* The imagination university program (2021), RVfpga-SoC INSTALLATION GUIDE
* The imagination university program (2021), RVfpga-SoC LAB 1 INTRODUCTION TO RVfpga-SoC
* The imagination university program (2021), RVfpga-SoC LAB 2 RUNNING SOFTWARE ON RVfpga-SoC

#### UNIVERSIDAD INDUSTRIAL DE SANTANDER :mortar_board:
* :woman: Angela Yulieth Rivera Gómez - 2162467
* :man: Vladimir Sebastian Villamizar Anaya - 2171522



