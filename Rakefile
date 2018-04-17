require 'rubygems'
require 'bundler/setup'
require 'sinatra/activerecord/rake'
require 'taza/tasks'
require 'active_record'

require File.expand_path('../shoe_store.rb', __FILE__)
require 'sinatra/activerecord/rake'

namespace :db do
  desc 'Load the seed data from db/seeds.rb'
  task :seed do

    ActiveRecord::Base.establish_connection(
        :adapter => "sqlite3",
        :database => "shoes.db"
    )

    seed_file = File.join(File.dirname(__FILE__), 'db', 'seeds.rb')
    system("racksh < #{seed_file}")
  end
end

