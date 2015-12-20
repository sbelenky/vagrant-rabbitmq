Vagrant.configure(2) do |config|

  config.vm.provider :aws do |aws, override|
    aws.access_key_id = ENV["AWS_ACCESS_KEY_ID"]
    aws.secret_access_key = ENV["AWS_SECRET_ACCESS_KEY"]
    aws.keypair_name = ENV["AWS_KEYPAIR_NAME"]

    aws.ami = "ami-3d7b2c57"
    aws.instance_type = "t1.micro"

    override.ssh.username = "root"
    override.ssh.private_key_path = ENV["AWS_PRIVATE_KEY_PATH"]
  end

  config.vm.box = "dummy"

end
