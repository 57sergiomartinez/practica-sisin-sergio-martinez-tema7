Vagrant.configure("2") do |config|
  
  # Introduce aquí la configuración del servidor virtual
  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network" , ip:"192.168.50.55"
  config.vm.synced_folder ".", "/practica-sisin-sergio-martinez"


  config.vm.provision "shell", inline: <<-SHELL

      # Instalación de los binarios de PHP, el driver mysqli y la extensión FPM para realizar peticiones de tipo RESTful
      sudo apt-get install -y php php-mysqli

      # Generar archivo SQL con los registros de los diferentes Módulos Profesionales
      echo "-- Insertar datos en la lista 'profesores'" > /home/vagrant/datos_profesores.sql
      echo "INSERT INTO empleados_tunivers.profesores (nombre, apellido, edad, salario, departamento) VALUES" >> /home/vagrant/datos_profesores.sql
      echo "('Diego','Alonso', 20, 3000.00, 'SISIN')," >> /home/vagrant/datos_profesores.sql
      echo "('Diego','Mateos', 25, 2500.00, 'PROG')," >> /home/vagrant/datos_profesores.sql
      echo "('Thomas','Huerta', 30, 2000.00, 'BADAT')," >> /home/vagrant/datos_profesores.sql
      echo "('Guillermo','Roman', 35, 1500.00, 'ENDES')," >> /home/vagrant/datos_profesores.sql
      echo "('Lorena','Franco', 40, 1000.00, 'LEUP')" >> /home/vagrant/datos_profesores.sql

  SHELL

end
