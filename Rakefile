require 'rubygems'
require 'rubygems/package_task'

NAME = 'ruby-netcdf'
VER = '0.7.2'

PKG_FILES = FileList[
  '**',
  'lib/**/*',
  'demo/**/*',
  'doc/**/*',
  'test/**/*'
]

spec = Gem::Specification.new do |s|
  s.name             = NAME
  s.version          = VER
  s.authors           = ["Takeshi Horinouchi", "Tsuyoshi Koshiro",\
    "Shigenori Otsuka", "Seiya Nishizawa", "T Sakakima"]
  s.email            = ['eriko@gfd-dennou.org']
  s.homepage         = 'http://www.gfd-dennou.org/arch/ruby/products/ruby-netcdf/'
  s.licenses         = ["GFD Dennou Club"]
  s.platform         = Gem::Platform::RUBY
  s.summary          = %q{Ruby interface to NetCDF}
  s.description      = %q{RubyNetCDF is the Ruby interface to the NetCDF library built on the NArray library, which is an efficient multi-dimensional numeric array class for Ruby.}

  s.files            = PKG_FILES.to_a
  s.require_paths    = ['lib']
  s.test_files = Dir.glob("test/*")
  s.required_ruby_version = Gem::Requirement.new(">= 3.0")
  s.add_runtime_dependency(%q<narray>, [">= 0"])
  s.add_runtime_dependency(%q<narray_miss>, [">= 0"])
  #s.extra_rdoc_files = ['README']

  s.extensions << "extconf.rb"
end

Gem::PackageTask.new(spec) do |pkg|
  pkg.need_tar = true
end
