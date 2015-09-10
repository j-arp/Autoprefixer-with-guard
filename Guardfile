require "autoprefixer-rails"
# A sample Guardfile
# More info at https://github.com/guard/guard#readme
# directories %w(site)
#watch(/.*/){ | f |  puts "gonna do funky shit to #{f}" }

# guard 'sass', :output => 'styles', :output => 'css', :shallow => false, :syntax => :scss, :cache => false do
#   watch %r{^sites^site\/(.+)\/src\/(.+\.s[ac]ss)$^site\/(.+)\/src\/(.+\.s[ac]ss)$\/(.+)\/src\/(.+\.s[ac]ss)$}
# end


watch(%r{^sites\/(.+)\/src\/(.+\.css)$}) do | f |  
  # puts AutoprefixerRails.methods
  puts "gonna do funky shit to #{f}" 
  css = File.read(f.first)
  puts "process #{f.last} and then write it to #{f.first.gsub('src', 'css')}"
  prefixed = AutoprefixerRails.process(css, from: f.first).css
  puts prefixed
  File.open(f.first.gsub('src', 'css'), 'w') { |file| file.write(prefixed) }
end
