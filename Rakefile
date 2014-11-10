#https://github.com/swipely/docker-api
require 'rake'
require 'docker'
require 'rake/packagetask'

task :pack do
   sh "cd images/psql; tar --exclude=upload.tar -cf upload.tar *"
end

task :run do
  puts "Uploading image"
  image=Docker::Image.build_from_tar(File.open('images/psql/upload.tar', 'r'))
  puts "Creating container"
  container = Docker::Container.create('Image' => image.json['Config']['Image'])
  puts "Starting container"
  container.start
end

 task :prepare => [:pack, :run] do
   puts "preparing"
 end
