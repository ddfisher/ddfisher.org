require 'rubygems'
require 'rake'

#
# Compile
#

desc "Compile everything"
task :compile do
  sh "jekyll"
end

#
# Watch & continuously compile
#

desc "Watch-compile jekyll site"
task :jekyll do
  sh "jekyll --auto --server"
end

#
# Deploy
#

desc "Deploy site"
task :publish do
  sh "jekyll"
  sh "rsync -r -a -v --delete nginx.conf _site ddfisher.org:/home/david/www/ddfisher.org/"
end
