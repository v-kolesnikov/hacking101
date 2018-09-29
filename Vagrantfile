Vagrant.configure('2') do |config|
  config.vm.define 'x86' do |x86|
    x86.vm.box = 'ubuntu/xenial32'
  end

  config.vm.define 'x64' do |x64|
    x64.vm.box = 'ubuntu/xenial64'
  end

  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y \
      build-essential \
      gdb \
      lldb \
      clang \
      cmake
  SHELL
end
