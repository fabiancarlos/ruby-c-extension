# -*- ruby -*-

require "rubygems"
require "hoe"
require "rake/extensiontask"

Hoe.spec "stree" do
  developer("Fabian Carlos", "fabian.pow@gmail.com")
  self.readme_file = 'README.rdoc'
  self.history_file = 'CHANGELOG.rdoc'
  self.extra_rdoc_files = FileList['*.rdoc']
  self.extra_dev_deps << ['rake-compiler', '>= 0']
  self.spec_extras = { :extensions => ["ext/stree/extconf.rb"] }

  Rake::ExtensionTask.new('stree', spec) do |ext|
    ext.lib_dir = File.join('lib', 'stree')
  end
end

Rake::Task[:test].prerequisites << :compile

# vim: syntax=ruby
