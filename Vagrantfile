# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.hostname = "apachebuddy-vagrant"
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"

  config.vm.provision :shell, :inline => "apt-get install -y apache2;\
    wget http://apachebuddy.pl -O /tmp/apachebuddy.pl;\
    service apache2 start;\
    perl /tmp/apachebuddy.pl;\
    echo Hack from /vagrant and run 'perl /tmp/apachebuddy.pl' to compare to the live http://apachebuddy.pl";
end
