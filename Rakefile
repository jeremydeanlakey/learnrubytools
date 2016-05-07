# code taken from tutorial at http://jasonseifer.com/2010/04/06/rake-tutorial
directory "tmp"
 
file "tmp/hello.tmp" => "tmp" do
  sh "echo 'Hello4' >> 'tmp/hello.tmp'"
end


task :turn_off_alarm do
  puts "Turned off alarm. Would have liked 5 more minutes, though."
end

task :groom_myself do
  puts "Brushed teeth."
  puts "Showered."
  puts "Shaved."
end

task :make_coffee do
  cups = ENV["COFFEE_CUPS"] || 2
  puts "Made #{cups} cups of coffee. Shakes are gone."
end

task :walk_dog do
  puts "Dog walked."
end

task :ready_for_the_day => [:turn_off_alarm, :groom_myself, :make_coffee, :walk_dog] do
  puts "Ready for the day!"
end


namespace :morning do
  task :turn_off_alarm do
    puts "Turned off alarm. Would have liked 5 more minutes, though."
  end
end


task :default => 'morning:turn_off_alarm'

