desc "Unpublish all posts"
task :unpublish do
  Dir["_posts/*.textile"].each do |post|
    puts "Unpublishing #{post}"
    lines = File.readlines(post)
    lines.insert(1, "published: false\n")
    File.open(post, "w") { |f| f.write lines.join }
  end
end
