require 'rake-jekyll'

# This task builds the Jekyll site and deploys it to a remote Git repository.
# It's preconfigured to be used with GitHub and Travis CI.
# See http://github.com/jirutka/rake-jekyll for more options.
Rake::Jekyll::GitDeployTask.new(:deploy) do |t|
    t.committer = 'Mark R. Reed <mreedmdev@gmail.com>'

    # Overrides the *author* of the commit being created with author of the
    # source commit (i.e. HEAD in the current branch).
    t.author = -> {
      `git log -n 1 --format='%aN <%aE>'`.strip
  }
end
