

# desc 'outputs hello to the terminal'
# task :hello do
#   puts "hello from Rake!"
# end

# desc 'outputs hola to the terminal'
# task :hola do
#   puts "hola from rake!"
# end
# grouping
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
  
  # rake db:migrate
  namespace :db do
  # create the environment task first
  desc 'run the environment first'
  task :environment do
    require_relative './config/environment'
  end
  
   # migrating changes to our database
  desc 'migrate changes to our database'
  # task dependency => run the environment before running migrate
  task migrate: :environment do
    Student.create_table
  end

  desc 'seed our database with some placeholder data'
  task seed: :migrate do
    require_relative './db/seeds'
  end
  end
  
  desc 'run the environment first'
  task :environment do
    require_relative './config/environment'
  end
  # rake console => loads pry console for us
  desc 'drop into the pry console'
  task console: :environment do
    Pry.start
  end