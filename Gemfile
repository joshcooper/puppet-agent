source ENV['GEM_SOURCE'] || "https://rubygems.org"

def vanagon_location_for(place)
  if place =~ /^(git[:@][^#]*)#(.*)/
    [{ :git => $1, :branch => $2, :require => false }]
  elsif place =~ /^file:\/\/(.*)/
    ['>= 0', { :path => File.expand_path($1), :require => false }]
  else
    [place, { :require => false }]
  end
end

gem 'vanagon', *vanagon_location_for(ENV['VANAGON_LOCATION'] || '0.7.1')
gem 'packaging', '~> 0.4', :github => 'puppetlabs/packaging'
gem "beaker-hostgenerator", :github => 'joshcooper/beaker-hostgenerator', :branch => 'cinext' # *location_for(ENV['BEAKER_HOSTGENERATOR_VERSION'] || "~> 0.3")

gem 'rake'
gem 'json'
gem 'rubocop', "~> 0.34.2"
