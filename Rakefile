require 'rake'
require 'rake/testtask'
require 'rake/rdoctask'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gemspec|
    gemspec.name = "uploadcolumn"
    gemspec.summary = "Enables easy uploading of files, especially images."
    gemspec.description = "UploadColumn is a gem/plugin for the Ruby on Rails framework that enables easy uploading of files, especially images."
    gemspec.email = "dave.hrycyszyn@headlondon.com"
    gemspec.homepage = "http://github.com/futurechimp/uploadcolumn"
    gemspec.authors = ["Dave Hrycyszyn", "Jonas Nicklas", "Sebastian Kanthak"]
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler not available. Install it with: gem install jeweler"
end

file_list = FileList['spec/*_spec.rb']

desc 'Default: run unit tests.'
task :default => 'spec:rcov'

namespace "doc" do

  desc 'Generate documentation for the UploadColumn plugin.'
  Rake::RDocTask.new(:normal) do |rdoc|
    rdoc.rdoc_dir = 'doc/rdoc'
    rdoc.title    = 'UploadColumn'
    rdoc.options << '--line-numbers' << '--inline-source'
    rdoc.rdoc_files.include('README')
    rdoc.rdoc_files.include('lib/**/*.rb')
  end

  desc 'Generate documentation for the UploadColumn plugin using the allison template.'
  Rake::RDocTask.new(:allison) do |rdoc|
    rdoc.rdoc_dir = 'doc/rdoc'
    rdoc.title    = 'UploadColumn'
    rdoc.options << '--line-numbers' << '--inline-source'
    rdoc.rdoc_files.include('README')
    rdoc.rdoc_files.include('lib/**/*.rb')
    rdoc.main = "README" # page to start on
    rdoc.template = "~/Projects/allison2/allison/allison.rb"
  end
end

