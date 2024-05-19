Vagrant.configure("2") do |config|
  
  # Introduce aquí la configuración del servidor virtual
  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network" , ip:"192.168.50.55"
  config.vm.synced_folder ".", "/practica-sisin-sergio-martinez"


  config.vm.provision "shell", inline: <<-SHELL

      # Instalación de los binarios de PHP, el driver mysqli y la extensión FPM para realizar peticiones de tipo RESTful


      # Generar archivo SQL con los registros de los diferentes Módulos Profesionales
      

  SHELL

end
