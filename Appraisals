# frozen_string_literal: true

[
  { name: '6-0', ruby: '2.7.2', rails: '6.0', mongoid: '7.0' },
  { name: '6-1', ruby: '2.7.2', rails: '6.1', mongoid: '7.2' },
  { name: '6-1-3.0', ruby: '3.0.1', rails: '6.1', mongoid: '7.2' }
].each do |set|
  appraise "rails-#{set[:name]}-mongoid-#{set[:mongoid][0]}" do
    gem 'rails', "~> #{set[:rails]}"

    gem 'mongoid', "~> #{set[:mongoid]}"
    gem 'mongoid-locker', '~> 1.0'
  end
end
