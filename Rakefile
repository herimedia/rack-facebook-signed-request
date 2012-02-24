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
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "rack-facebook-signed-request"
  gem.homepage = "http://github.com/gamesthatgive/rack-facebook-signed-request"
  gem.license = "MIT"
  gem.summary = %Q{Simple Rack middle for parsing and validation Facebook signed_request param.}
  gem.description = %Q{See http://developers.facebook.com/docs/authentication/canvas}
  gem.email = "goss@gamesthatgive.net"
  gem.authors = ["Kristofer Goss"]

  gem.add_runtime_dependency 'rack'
  gem.add_runtime_dependency 'yajl-ruby'

  gem.add_development_dependency 'shoulda', '>= 0'
  gem.add_development_dependency 'bundler', '~> 1.0.0'
  gem.add_development_dependency 'jeweler', '~> 1.5.1'
end
Jeweler::RubygemsDotOrgTasks.new

require 'rake/rdoctask'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "rack-facebook-signed-request #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
