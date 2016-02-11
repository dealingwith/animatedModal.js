task :default => [:minify]

desc "Minify"
task :minify do
  begin
    require 'rubygems'
    require 'uglifier'
  rescue LoadError => e
    if verbose
      puts "\nYou'll need the 'uglifier' gem for minification. Just run:\n\n"
      puts "  $ gem install uglifier"
      puts "\nand you should be all set.\n\n"
      exit
    end
    return false
  end
  puts "Minifying animatedModal.js with UglifyJS..."
  File.open("animatedModal.min.js", "w"){|f| f.puts Uglifier.new.compile(File.read("animatedModal.js"))}

end