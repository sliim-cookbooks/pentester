# -*- coding: utf-8 -*-
source 'https://rubygems.org'

gem 'chef', '~> 12'
gem 'berkshelf'
gem 'rake'

group :lint do
  gem 'rubocop'
  gem 'foodcritic'
end

group :unit do
  gem 'chefspec'
end

group :kitchen do
  gem 'test-kitchen'
  gem 'kitchen-vagrant'
  gem 'kitchen-openstack'
  gem 'kitchen-docker', '=2.1.0'
end

group :development do
  gem 'guard'
  gem 'guard-foodcritic'
  gem 'guard-rubocop'
  gem 'guard-rspec'
end
