require "autoprefixer-rails"

# directories %w(site)


watch(%r{^sites\/(.+)\/src\/(.+\.css)$}) do | f |  
  css = File.read(f.first)
  # "process #{f.last} and then write it to #{f.first.gsub('src', 'css')}"
  prefixed = AutoprefixerRails.process(css, from: f.first).css
  File.open(f.first.gsub('src', 'css'), 'w') { |file| file.write(prefixed) }
end
