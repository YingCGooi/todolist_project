require 'bundler/gem_tasks'
require 'rake/testtask'
require 'find'

desc 'Say hello' # attaches a description of 'Say hello' to the task
task :hello do
	puts "Hello there. This is the 'hello' task."
end # this is just a Ruby code.
# uses a DSL supplied by Rake.

desc 'Run tests'
task :default => :test

Rake::TestTask.new(:test) do |t|
	t.libs << "test"
	t.libs << "lib"
	t.test_files = FileList['test/**/*_test.rb']
end

desc 'Display inventory of all files'
task :inventory do
	Find.find('.') do |name|
		next if name.include?('/.')
		puts name if File.file?(name)
	end
end


