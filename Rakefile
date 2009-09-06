BUNDLE_ROOT = File.dirname(__FILE__)

desc "Update all Bundles"
task :default do
  Dir.chdir(BUNDLE_ROOT) do
    Dir['*.tmbundle'].each do |bundle|
      if File.directory? File.join(bundle, '.git')
        Dir.chdir(bundle) do
          `git checkout master`
          `git pull origin master`
        end
      end
    end
    # exec('git commit -a *.tmbundle`')
  end
end