 # <p align= "center"> :books: RVfpga SoC THE IMAGINATION UNIVERSITY PROGRAMME :books: </p>

Para la realización de los siguientes laboratorios incialmente nos registramos en la pagina web de imagination university program y solicitamos el envio del mataerial correspondiente, posteriormente se incio la lectura de la guia para iniciar la instalación y desarrollo de los laboratorios.

### LABORATORIO 1 - INTRODUCCIÓN A RVfpga-Soc
Para inciar el desarrollo de este laboratorio iniciamos con la lectura incial en la guia de forma que se fuera entendiendo como funciona RVfpga-SoC, además de ir conociendo sus caracteristicas principales, posteriormente se fueron conociendo los requerimientos necesarios para el correcto desarrollo del laboratorio y se inicio con la instalación de los siguientes programas:


 * :black_nib: Vivado 
 * :black_nib: Cable Drivers
 * :black_nib: Digilent Board Files

Ahora se iniciara con el desarrollo de la guia por lo tanto se creara un proyecto en vivado: 

<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/073427536581c14a7dcc519191a407ddf5a3ae89/Im%C3%A1genes/Screenshot%20from%202022-03-06%2015-27-54.png"/>
</p>

Luego se definen diferentes caracteristicas en el proyecto creado como las que se pueden observar a continuación:

<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/10ceab68894be5e6ab13573844f50aaf18fbfe8e/Im%C3%A1genes/Screenshot%20from%202022-03-06%2018-22-41.png"/>
</p>
<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/10ceab68894be5e6ab13573844f50aaf18fbfe8e/Im%C3%A1genes/Screenshot%20from%202022-03-06%2018-32-28.png"/>
</p>
 
e iniciamos a añadir algunos bloques en el espacio de diseño, uno de ellos es el swerv_wrapper_verilog0:

<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/18b41a04b81fd2621903e8d3899d51664c39f2ea/Im%C3%A1genes/Screenshot%20from%202022-03-06%2018-36-53.png"/>
</p>

Luego de realizar cada una de las conexiones requeridas obtenemos un diseño como el que se puede observar en la siguiente imagen: 


<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/ff9088e116703afc03ac4f4b44b5fb3902b39b47/Im%C3%A1genes/Screenshot%20from%202022-03-06%2020-32-55.png"/>
</p>


Ahora se va a generar el bit stream: 

<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/c7ee3ebc16cc1986ad42da0d897b7c13d6281938/Im%C3%A1genes/Screenshot%20from%202022-03-06%2021-26-42.png"/>
</p>

Finalmente se puede observar que se obtuvo el bit stream y la sintesis correctamente: 

<p align="center"> 
 <img src="https://github.com/Vlasevi/riscvlabs/blob/c7ee3ebc16cc1986ad42da0d897b7c13d6281938/Im%C3%A1genes/Screenshot%20from%202022-03-06%2022-44-06.png"/>
</p>



### LABORATORIO 2 - CORRIENDO EL SOFTWARE EN RVfpga-Soc


### CONCLUSIONES :heavy_check_mark:
* 
* 
* 

### REFERENCIAS :paperclip:
* The imagination university program (2021), RVfpga-SoC INSTALLATION GUIDE
* paperclip: The imagination university program (2021), RVfpga-SoC LAB 1 INTRODUCTION TO RVfpga-SoC
* paperclip: The imagination university program (2021), RVfpga-SoC LAB 2 RUNNING SOFTWARE ON RVfpga-SoC

#### UNIVERSIDAD INDUSTRIAL DE SANTANDER :mortar_board:
* :woman: Angela Yulieth Rivera Gómez - 2162467
* :man: Vladimir Sebastian Villamizar Anaya - 2171522
