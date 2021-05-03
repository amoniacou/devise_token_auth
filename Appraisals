# frozen_string_literal: true

[
  { name: '6-0', version: '6.0' },
  { name: '6-1', version: '6.1' }
].each do |rails|
  appraise "rails-#{rails[:name]}" do
    gem 'rails', "~> #{rails[:version]}"
    gem 'mysql2'
    gem 'pg'
  end
end

[
  { name: '6-0', ruby: '2.7.2', rails: '6.0', mongoid: '7.2' },
  { name: '6-1', ruby: '2.7.2', rails: '6.1', mongoid: '7.2' },
].each do |set|
  appraise "rails-#{set[:name]}-mongoid-#{set[:mongoid][0]}" do
    gem 'rails', "~> #{set[:rails]}"

    gem 'mongoid', "~> #{set[:mongoid]}"
    gem 'mongoid-locker', '~> 1.0'
    gem 'database_cleaner-mongoid'
  end
end
