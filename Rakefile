require 'html-proofer'

desc "build and test website"
task :test do
  sh "bundle exec jekyll build"
  HTMLProofer.check_directory("./_site", {
    :typhoeus => {
      :ssl_verifypeer => false,
      :ssl_verifyhost => 0},
    verbose => true}).run
end