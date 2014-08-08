CC = "gcc"

task :default => "hello"

file "hello" => "hello.o" do |t|
  sh "#{CC} -o #{t.name} #{t.prerequisites[0]}"
end

rule '.o' => '.c' do |t|
  sh "#{CC} -c #{t.source}"
end