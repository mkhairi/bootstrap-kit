require "bundler/gem_tasks"
task :default => :spec

source_dir = "bootstrap-kit-src" 

namespace :stylesheets do
  desc "Cleaning stylesheets directory"
  task :clean do
   rm_rf "vendor/assets/stylesheets/boostrap-kit"
  end

  desc "Copy #{source_dir}/scss/"
  task :copy do
    src_dir = "#{source_dir}/scss/."
    tgt_dir = "vendor/assets/stylesheets/bootstrap-kit/"
    mkdir_p tgt_dir
    cp_r src_dir, tgt_dir
  end

  desc "Setup stylesheet assets"
  task setup: [:clean, :copy]
end

desc "Setup or update assets files"
task setup: ["stylesheets:setup"]