# A sample Guardfile
# More info at https://github.com/guard/guard#readme
if File.exists?("./config.rb")
# Compile on start.
  puts `compass compile --time --quiet `
  guard :compass do
    watch(%r{(.*)\.s[ac]ss$})
  end
end

guard 'livereload' do
  watch(%r{html/.+\.(css|js|html|png|jpg|php)})
  watch(%r{sass/(.+).scss}) { |m| "html/assets/css/#{m[1]}.css" }
end
