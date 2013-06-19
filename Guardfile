# A sample Guardfile
# More info at https://github.com/guard/guard#readme

#guard 'livereload' do
#  watch(%r{app/views/.+\.(erb|haml|slim)$})
#  watch(%r{app/helpers/.+\.rb})
#  watch(%r{public/.+\.(css|js|html)})
#  watch(%r{config/locales/.+\.yml})
#  # Rails Assets Pipeline
#  watch(%r{(app|vendor)(/assets/\w+/(.+\.(css|js|html))).*}) { |m| "/assets/#{m[3]}" }
#end

guard 'livereload' do
  watch(%r{content/pages(/.+)\.(mdown|textile|haml)}) { |match| match[1] }
  watch(%r{public(/.+\.(jpe?g|js|png))}) { |match| match[1] }
  watch(%r{views/.+\.haml})
  watch(%r{config/.+\.yml})
  watch(%r{views/(.+)\.s[ac]ss}) do |match|
    if match[1] =~ /(mixins|variables)/
      ["/css/master.css", "/css/layout.css"]
    else
      "/css/#{match[1]}.css"
    end
  end
end
