Vagrant.configure(2) do |config|

  config.vm.provider :aws do |aws, override|
    aws.access_key_id = ENV["AWS_ACCESS_KEY_ID"]
    aws.secret_access_key = ENV["AWS_SECRET_ACCESS_KEY"]
    aws.keypair_name = ENV["AWS_KEYPAIR_NAME"]

    aws.ami = "ami-26cc934e"
    aws.instance_type = "t1.micro"

    override.ssh.username = "ec2-user"
    override.ssh.private_key_path = ENV["AWS_PRIVATE_KEY_PATH"]
  end

  config.vm.box = "dummy"

  # config.vm.provision "shell", inline: <<-SHELL
    # yum -y update
    # wget http://dl.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm
    # wget http://rpms.famillecollet.com/enterprise/remi-release-6.rpm
    # sudo rpm -Uvh remi-release-6*.rpm epel-release-6*.rpm
    # yum install -y erlang
    # wget http://www.rabbitmq.com/releases/rabbitmq-server/v3.2.2/rabbitmq-server-3.2.2-1.noarch.rpm
    # rpm --import http://www.rabbitmq.com/rabbitmq-signing-key-public.asc
    # yum install rabbitmq-server-3.2.2-1.noarch.rpm
    # sudo rabbitmq-plugins enable rabbitmq_management
  # SHELL

end
