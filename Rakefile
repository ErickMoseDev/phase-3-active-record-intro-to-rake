namespace :greeting do
  desc 'Outputs Hello from rake in the terminal'
  task :hello do
    puts 'hello from Rake!'
  end

  desc 'outputs hola de Rake! terminal'
  task :hola do
    puts 'hola de Rake!'
  end
end

# Namespacing basically means a way to group or contain something, i.e our rake tasks.


namespace :db do
  task migrate: :environment do    # this syntax creates a task dependency
    Student.create_table
  end

  desc 'plant some seeds-add placeholder data in the db'
  task seed: :environment do
    require_relative './db/seeds'
  end
end

desc 'load up the environment configuration first'
task :environment do
  require_relative './config/environment'
end

desc 'start up the Pry console. will be dependant on the env file'
task console: :environment do
  Pry.start
end