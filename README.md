# Phase-3!

# Results
![Results](images/results.png)

# Steps

* **Copy all the files(.sh, .java and 9091, 9293) to Vagrant box(itmd-521/data)**
	* exit vagrant
	* download the files or clone it itmd-521/data folder
	* vagrant plugin install vagrant-scp
	* vagrant scp "./data/9091" default:/home/vagrant/
	* vagrant scp "./data/9293" default:/home/vagrant/
	* vagrant scp "./data/9293" default:/home/vagrant/
	* vagrant scp "./data/mySql-setup.sh" default:/home/vagrant/
	* vagrant scp "./data/dbCreation.sh" default:/home/vagrant/
	* vagrant scp "./data/tblCreation.sh" default:/home/vagrant/
	* vagrant scp "./data/insertDataTbleOne.java" default:/home/vagrant/
	* vagrant scp "./data/insertDataTbleTwo.java" default:/home/vagrant/
	* vagrant scp "./data/maxTemperatureTblOne.java" default:/home/vagrant/
	* vagrant scp "./data/maxTemperatureTblTwo" default:/home/vagrant/
	* vagrant up then do vagrant ssh

* **Install MYSQL**
	* Run mySql-setup.sh
		* Enter password when prompted as **root**
		* sudo chmod +x mySql-setup.sh
		* sudo ./mySql-setup.sh
		
* **Database Creation**
	* Create Database
		* sudo chmod +x dbCreation.sh
		* sudo ./dbCreation.sh
		
	* Create Table
		* sudo chmod +x tblCreation.sh
		* sudo bash tblCreation.sh

* **Inserting Records in MYSQL table**
	* Add MYSQL Driver
		* sudo apt-get install mysql-client
		* sudo apt-get install libmysql-java
		* Add Classpath in **.bashrc**
		* **export CLASPATH=$CLASSPATH:/usr/share/java/mysql.jar**

	* Create a class file
		* hadoop com.sun.tools.javac.Main insertDataTbleOne.java
		* hadoop com.sun.tools.javac.Main insertDataTbleTwo.java
		
	* Compile java file
		* javac insertDataTbleOne.java
		* javac insertDataTbleTwo.java
		
	* Run java file
		* java insertDataTbleOne
		* java insertDataTbleTwo
		
*  **Retrieve the highest temperature on record per year**
	* Create a class file
		* hadoop com.sun.tools.javac.Main maxTemperatureTblOne.java
		* hadoop com.sun.tools.javac.Main maxTemperatureTblTwo.java
		
		
	* Compile java file
		* javac maxTemperatureTblOne.java
		* javac maxTemperatureTblTwo.java
		
	* Run java file
		* java maxTemperatureTblOne
		* java maxTemperatureTblTwo
		
		