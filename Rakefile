require 'rubygems'
require 'echoe'

# get the version directly from the .h file
version_file = File.join File.dirname(__FILE__), "ext", "serialport.h"
version = File.read(version_file).match(/RUBY_SERIAL_PORT_VERSION.*"(.*)"/)[1]

# try "rake -T" so see the wunderfull tasks generated by the little code below ;-)
e = Echoe.new('ruby-serialport', version) do |s|
   # set only a platform when building binary gems.
   # in this case the Manifest has also to be changed to include the compiled extension
   #s.platform = Gem::Platform::CURRENT
   s.summary = "Ruby/SerialPort is a Ruby library that provides a class for using RS-232 serial ports."

   s.rdoc_pattern = [ "README", "CHANGELOG", "ext/serialport.c", "lib/serialport.rb" ]
   s.ignore_pattern = Dir.glob("{tmp}/**/*")

   s.author = ["Guillaume Pierronnet", "Alan Stern", "Daniel E. Shipton", "Jonas Bähr"]
   s.email = "daniel.shipton.oss@gmail.com"
   s.project = 'ruby-serialport'
   s.url = "http://ruby-serialport.rubyforge.org"

   s.rubygems_version = nil
end
