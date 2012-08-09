require 'rubygems'
require 'bundler'
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  gem.name = "hanna-nouveau-hacked"
  gem.homepage = "http://github.com/roybotnik/hanna-nouveau"
  gem.license = "MIT"
  gem.summary = %Q{A hacked up version of hanna-nouveau used to generate some API docs for an app.}
  gem.description = %Q{}
  gem.email = "roybotnik@gmail.com"
  gem.authors = ["Roy Quader", "Erik Hollensbe", "James Tucker", "Mislav Marohnic"]
  # Include your dependencies below. Runtime dependencies are required when using your gem,
  # and development dependencies are only needed for development (ie running rake tasks, tests, etc)
  gem.add_runtime_dependency 'haml', ">= 3.0.25"
  gem.add_runtime_dependency 'rdoc'
  gem.add_development_dependency 'jeweler'
  gem.add_development_dependency 'rake'
end
Jeweler::RubygemsDotOrgTasks.new

require 'rdoc/task'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "hanna-nouveau #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
