#
# $Id: Rakefile 1164 2011-04-21 17:25:07Z davidm $
#

require 'rubygems'
#require 'rake/gempackagetask'
require 'rubygems/package_task'
#require 'rubygems/packagetask'

spec = Gem::Specification.new do |s|
  # Basics
  s.name = 'tle'
  s.version = '0.0.0'
  s.summary = 'Provides Ruby bindings to sgp4 TLE library'
  s.description = <<-EOD
    TLE prediction code for Ruby based on C++ sgp4 code included in
    http://celestrak.com/publications/AIAA/2006-6753/AIAA-2006-6753.zip
    EOD
  #s.platform = Gem::Platform::Ruby
  s.required_ruby_version = '>= 1.8.1'
  #s.add_dependency('narray', '>= 0.5.9')

  # About
  s.authors = 'David MacMahon (gemification)'
  s.email = 'davidm@astro.berkeley.edu'
  s.homepage = 'http://tle.rubyforge.org/'
  s.rubyforge_project = 'tle' 

  # Files, Libraries, and Extensions
  s.files = FileList[
    'README.rdoc',
    'Rakefile',
    'lib/tle.rb',
    'ext/debug1.i',
    'ext/debug2.i',
    'ext/debug3.i',
    'ext/debug4.i',
    'ext/debug5.i',
    'ext/debug6.i',
    'ext/debug7.i',
    'ext/extconf.rb',
    'ext/rb_tle.cpp',
    'ext/sgp4ext.cpp',
    'ext/sgp4ext.h',
    'ext/sgp4io.cpp',
    'ext/sgp4io.h',
    'ext/sgp4unit.cpp',
    'ext/sgp4unit.h',
    'test/tcppver.out',
    'test/test.rb'
  ]
  #s.require_paths = ['lib', 'ext']
  #s.autorequire = nil
  #s.bindir = 'bin'
  #s.executables = []
  #s.default_executable = nil

  # C compilation
  s.extensions = %w[ ext/extconf.rb ]

  # Documentation
  s.has_rdoc = true
  #s.rdoc_options = %w[-m README.rdoc -E c=cpp]
  s.rdoc_options = %w[-m README.rdoc]
  s.extra_rdoc_files = %w[README.rdoc ext/rb_tle.cpp]

  # Testing TODO
  #s.test_files = []
end

Gem::PackageTask.new(spec) do |pkg|
  pkg.need_zip = true
  pkg.need_tar = true
end
