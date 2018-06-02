# Testing

Tests can be run with Rake:

#### Install dependencies
`bundle install`

#### Run Checkstyle & Specs
`bundle exec rake`

#### Foodcritic
`bundle exec rake test:foodcritic`

#### Cookstyle
`bundle exec rake test:cookstyle`

#### ChefSpec
`bundle exec rake test:chefspec`

#### Kitchen
`bundle exec rake test:kitchen`

#### Kitchen in Docker
`KITCHEN_YAML=.kitchen.docker.yml bundle exec rake test:kitchen`
