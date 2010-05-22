require 'rubygems'
require 'rake'
require 'spec/rake/spectask'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "remarkable_mongo_ign"
    gem.summary = %Q{Remarkable Matchers for MongoDB ORMs}
    gem.email = "nicolas.merouze@gmail.com, rubyorchard@gmail.com"
    gem.homepage = "http://github.com/rubyorchard/remarkable_mongo"
    gem.authors = ["Nicolas Mérouze", "Chandra Patni"]
    
    gem.add_dependency('remarkable',  '~> 3.1.13')
    gem.add_dependency('mongo_mapper_ign', '>= 0.7.6')
  end
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: sudo gem install jeweler"
end

desc 'Default: run specs.'
task :default => :spec

desc 'Run all the specs for the machinist plugin.'
Spec::Rake::SpecTask.new do |t|
  t.spec_files = FileList['spec/**/*_spec.rb']
  t.rcov = false
end