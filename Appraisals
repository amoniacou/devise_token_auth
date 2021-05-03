# frozen_string_literal: true

[
  { ruby: '2.7', rails: '6.0', database: 'postgresql', gem: 'pg', version: '~> 1.2.3' },
  { ruby: '3.0', rails: '6.0', database: 'postgresql', gem: 'pg', version: '~> 1.2.3' },
  { ruby: '2.7', rails: '6.1', database: 'postgresql', gem: 'pg', version: '~> 1.2.3' },
  { ruby: '3.0', rails: '6.1', database: 'postgresql', gem: 'pg', version: '~> 1.2.3' },
  { ruby: '2.7', rails: '6.0', database: 'mysql', gem: 'mysql2', version: '~> 0.5.3' },
  { ruby: '3.0', rails: '6.0', database: 'mysql', gem: 'mysql2', version: '~> 0.5.3' },
  { ruby: '2.7', rails: '6.1', database: 'mysql', gem: 'mysql2', version: '~> 0.5.3' },
  { ruby: '3.0', rails: '6.1', database: 'mysql', gem: 'mysql2', version: '~> 0.5.3' },
  { ruby: '2.7', rails: '6.0', database: 'mongodb', gem: 'mongoid', version: '~> 7.2.2' },
  { ruby: '3.0', rails: '6.0', database: 'mongodb', gem: 'mongoid', version: '~> 7.2.2' },
  { ruby: '2.7', rails: '6.1', database: 'mongodb', gem: 'mongoid', version: '~> 7.2.2' },
  { ruby: '3.0', rails: '6.1', database: 'mongodb', gem: 'mongoid', version: '~> 7.2.2' },
].each do |matrix|
  appraise "ruby-#{matrix[:ruby]}-rails-#{matrix[:rails]}-#{matrix[:database]}" do
    gem 'rails', "~> #{matrix[:rails]}"
    gem "#{matrix[:gem]}", "#{matrix[:version]}"
    if matrix[:database] == "mongodb"
      gem 'database_cleaner-mongoid'
    else
      gem 'database_cleaner-active_record'
    end
  end
end
