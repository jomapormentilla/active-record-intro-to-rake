require 'bundler'
Bundler.require

namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

desc 'start pry session'
task :console => :environment do
  Pry.start
end

namespace :db do
  desc 'migrate'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'load data'
  task :seed do
    require_relative './db/seeds'
  end
end

task :environment do
  require_relative './config/environment'
end