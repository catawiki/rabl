source 'https://rubygems.org'

# Specify your gem's dependencies in rabl.gemspec
gemspec

gem 'i18n', '~> 0.6'

platforms :mri_18 do
  gem 'SystemTimer'
  gem 'json'
end

group :test do
  # RABL TEST
  gem 'builder'

  # FIXTURES
  gem 'rack-test', :require => 'rack/test'
  gem 'activerecord', :require => 'active_record'
  gem 'sqlite3'
  gem 'sinatra', '>= 1.2.0'
  gem 'hashie', '~> 3.5.5'
end

group :development, :test do
  platforms :mri_18 do
    gem 'ruby-debug'
  end

  platforms :mri_19 do
    gem 'debugger'
  end

  platforms :mri_20, :mri_21, :mri_22 do
    gem 'byebug'
  end if RUBY_VERSION > '2.0'
end
