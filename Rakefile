require 'rubygems'
require 'rake'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "marcusmateus-georuby"
    gem.summary = "Ruby data holder for OGC Simple Features"
    gem.description = "GeoRuby provides geometric data types from the OGC 'Simple Features' specification."
    gem.email = "georuby@simplitex.com"
    gem.homepage = "http://github.com/marcusmateus/georuby"
    gem.authors = ["Guilhem Vellut", "Marcos Piccinini", "Marcus Mateus"]
    gem.add_runtime_dependency "json_pure", ">=1.4.6"
    gem.add_development_dependency "rspec", ">= 2.0.0"
    gem.add_development_dependency "dbf", ">= 1.2.9"
  end
rescue LoadError
  puts "Jeweler not available. Install it with: sudo gem install technicalpickles-jeweler -s http://gems.github.com"
end

# require 'spec/rake/spectask'
# Spec::Rake::SpecTask.new(:spec) do |spec|
#   spec.libs << 'lib' << 'spec'
#   spec.spec_files = FileList['spec/**/*_spec.rb']
# end

# Spec::Rake::SpecTask.new(:rcov) do |spec|
#   spec.libs << 'lib' << 'spec'
#   spec.pattern = 'spec/**/*_spec.rb'
#   spec.rcov = true
# end

# task :default => :spec

require 'rake/rdoctask'
Rake::RDocTask.new do |rdoc|
  if File.exist?('VERSION.yml')
    config = YAML.load(File.read('VERSION.yml'))
    version = "#{config[:major]}.#{config[:minor]}.#{config[:patch]}"
  else
    version = ""
  end

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "geo_ruby #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end

