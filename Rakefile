require 'rubygems'
require 'bundler'
require 'bundler/gem_tasks'

Bundler.setup :default, :development

require 'rspec/core'
require 'rspec/core/rake_task'

RSpec::Core::RakeTask.new(:spec) do |spec|
  spec.pattern = FileList['spec/**/*_spec.rb']
end

require 'rubocop/rake_task'
RuboCop::RakeTask.new

task default: [:rubocop, :spec]

load 'slack/web/api/tasks/generate.rake'
