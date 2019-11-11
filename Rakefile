require 'pry'
namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
    # puts "Hello from the other side"
    # puts "You must've called me a thousand times!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc "link the environment file"
  task :environment do
    require_relative './config/environment'
  end

  desc "migrate changes to your database"
  task :migrate => :environment do
    Student.create_table
  end
  desc "seed the database with some dummy data"
  task :seed do
    require_relative './db/seeds.rb'
  end
  desc 'drop into the Pry console'
  task :console => :environment do
    binding.pry
  end
end
