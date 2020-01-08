# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
# http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#

def bundle_exec(command)
  sh "bundle exec #{command}"
end

task :vendor do
  sh 'test -d cookbooks && rm -r cookbooks || exit 0'
  bundle_exec 'berks vendor cookbooks'
end

namespace :test do
  desc 'Tests suites runner'

  task :checkstyle do
    Rake::Task['test:foodcritic'].invoke
    Rake::Task['test:cookstyle'].invoke
  end

  task :specs do
    Rake::Task['test:chefspec'].invoke
  end

  task :foodcritic do
    bundle_exec 'foodcritic -f any .'
  end

  task :cookstyle do
    bundle_exec :cookstyle
  end

  task :chefspec do
    bundle_exec :rspec
  end

  task :kitchen do
    bundle_exec 'kitchen test'
  end
end

task default: ['test:checkstyle', 'test:specs']
