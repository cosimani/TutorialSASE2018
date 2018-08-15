Tutorial SASE 2018
==================

**Visión artificial y reconocimiento de patrones para la movilidad de un robot**

:Docentes: Ing. César Osimani  - Ing. Martín Salamero
:Contacto: cosimani@ubp.edu.ar - martin.salamero@gmail.com
:Código fuente: https://github.com/cosimani/RA-CVBot

Acondicionar la Raspberry Pi 
----------------------------

- Descargar imagen de `Raspbian Stretch with desktop <https://downloads.raspberrypi.org/raspbian_latest>`_

- Es una imagen que deberá ser copiada en la memoria SD ( se pueden usar los aplicativos Win32 Disk Imager (Windows) o Disk Image Writer (Ubuntu) )

- Utilizar la consola para realizar las siguientes instalaciones y configuraciones:

.. code-block::

	

	sudo apt-get update

	sudo apt-get upgrade

	sudo apt-get install build-essential cmake pkg-config

	- Crear una carpeta para compilar OpenCV, por ejemplo usar /home/pi/opencv y allí ejecutar lo siguiente:

	sudo wget http://liquidtelecom.dl.sourceforge.net/project/opencvlibrary/opencv-unix/3.1.0/opencv-3.1.0.zip

	sudo unzip opencv-3.1.0.zip

	cd opencv-3.1.0

	sudo mkdir build

	cd build

	sudo cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local -D WITH_V4L=ON -D WITH_TBB=ON ..

	sudo make

	sudo make install

	sudo nano /etc/ld.so.conf.d/opencv.conf

	/usr/local/lib









sudo apt-get install build-essential cmake pkg-config

sudo apt-get install default-jdk ant

sudo apt-get install libgtkglext1-dev

sudo apt-get install bison

sudo apt-get install qt4-dev-tools libqt4-dev libqt4-core libqt4-gui

sudo apt-get install v4l-utils

sudo apt-get install qtcreator

sudo wget http://liquidtelecom.dl.sourceforge.net ... -3.1.0.zip

sudo unzip opencv-3.1.0.zip

cd opencv-3.1.0

sudo mkdir build

cd build

sudo cmake -D CMAKE_BUILD_TYPE=RELEASE -D INSTALL_C_EXAMPLES=ON –D INSTALL_PYTHON_EXAMPLES=ON -D BUILD_EXAMPLES=ON -D WITH_QT=ON -D CMAKE_INSTALL_PREFIX=/usr/local -D WITH_OPENGL=ON -D WITH_V4L=ON –D BUILD_NEW_PYTHON_SUPPORT=ON -D WITH_TBB=ON ..

sudo make

sudo make install

sudo nano /etc/ld.so.conf.d/opencv.conf

/usr/local/lib

Press Control + X to save

sudo ldconfig

sudo nano /etc/bash.bashrc

PKG_CONFIG PATH=$PKG_CONFIG_PATH:/usr/local/lib/pkgconfig

export PKG_CONFIG_PATH

cd /home/pi/opencv-3.1.0/samples/cpp

g++ -o facedetect facedetect.cpp `pkg-config opencv --cflags --libs`

./facedetect





* `Aplicativos para desarrollo con Qt/C++ <http://www.qt.io/download-open-source/>`_
* `Instaladores offline de Qt <http://download.qt.io/archive/qt/>`_
* `Tutoriales y ejemplos con la biblioteca Qt <http://doc.qt.io/qt-5/qtexamplesandtutorials.html>`_
* `Foro de Qt en Español  <https://forum.qt.io/category/31/spanish>`_
* `Libro: El lenguaje de programación C++ de Bjarne Stroustrup (disponible en biblioteca de UBP) <http://www.amazon.es/El-lenguaje-programaci%C3%B3n-Bjarne-Stroustrup/dp/847829046X>`_
* `Videos tutoriales de C <https://www.youtube.com/playlist?list=PL54fdmMKYUJszGt6xq6QGSoaTzAVO-8jX>`_
* `Videos tutoriales de C++ <https://www.youtube.com/playlist?list=PL54fdmMKYUJvS32aLptKVC0AH9bwsavzi>`_
* `Videos tutoriales de Qt <https://www.youtube.com/playlist?list=PL54fdmMKYUJvn4dAvziRopztp47tBRNum>`_
* `App SoloLearn <https://play.google.com/store/apps/details?id=com.sololearn&hl=es_419>`_
