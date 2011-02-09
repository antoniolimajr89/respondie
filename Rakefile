require 'rubygems'
require 'rake'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "respondie"
    gem.summary = %Q{A helper to avoid class multiplicity in inheriting responders.}
    gem.description = %Q{A helper to avoid class multiplicity in inheriting responders.}
    gem.email = "guilherme.silveira@caelum.com.br"
    gem.homepage = "http://github.com/caelum/respondie"
    gem.authors = ["guilherme silveira"]
    gem.add_development_dependency "rspec", ">= 1.2.9"
    gem.version = "0.9.0"
    # gem is a Gem::Specification... see http://www.rubygems.org/read/chapter/20 for additional settings
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: gem install jeweler"
end

require 'rspec'
require 'rspec/core'
require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new(:spec) do |t|
  # t.spec_files = FileList['spec_*.rb']
  t.rspec_opts = ['--colour', '--format progress']
end

task :default => :spec

require 'rake/rdoctask'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "respondie #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
