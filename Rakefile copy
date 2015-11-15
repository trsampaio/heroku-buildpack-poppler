require "fileutils"
require "tmpdir"

FONTCONFIG_PACKAGE_TGZ = ENV['FONTCONFIG_PACKAGE_TGZ']

desc "download Fontconfig"
task "fontconfig:download", :version do |t, args|
  version = args[:version]
  echo version
  sh "curl http://www.freedesktop.org/software/fontconfig/release/fontconfig-#{version}.tar.gz -s -o - | tar vzxf -"
end

desc "install Fontconfig"
task "fontconfig:build", :version do |t, args|
  version = args[:version]
  name    = "fontconfig"
  prefix  = "/app/vendor/#{name}"

  build_command = [
    "./configure --disable-static --disable-docs --prefix=#{prefix}",
    "make",
  ].join(" && ")
  sh build_command
end

desc "download Poppler"
task "poppler:download", :version do |t, args|
  version = args[:version]

  sh "curl http://poppler.freedesktop.org/poppler-#{version}.tar.gz -s -o - | tar vxf -"
end

desc "install Poppler"
task "poppler:build", :version do |t, args|
  version = args[:version]
  name    = "poppler"
  prefix  = "/app/vendor/#{name}"
  echo version
  build_command = [
    "./configure --disable-static --enable-zlib --prefix=#{prefix}",
    "make",
  ].join(" && ")

  sh build_command
end
