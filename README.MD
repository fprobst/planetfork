# Workflow working with fork and remote repo 

1. Create own GitHub-Repository

2. Search for foreign GitHub-Repository and fork it within GitHub

3.  git clone foreign GitHub-Repository
<pre><code>
    $ git clone https://github.com/USERNAME/REPONAME.git
    $ cd REPONAME
</code></pre>

4. Create and add connection to foreign GitHub-Repository. Typically this is named as upstream. Your own GitHub-Repository is stored as orgin.
5. Connect foreign GitHub-Repository with lokal git project
<pre><code>
    $ git remote add upstream https://github.com/ANDERER_USER/ORIGINALREPO.git
    # Check remote connections
    $ git remote -v
</code></pre>

6. To pull data from the foreign repo add tracking info [git command -u]( https://git-scm.com/docs/git-branch#Documentation/git-branch.txt--ultupstreamgt) The command -u is the same as --track
<pre><code> 
    # Create remote connections for pull
    $ git branch -u upstream/master
    # Check remote connections
    $ git branch --all
    # Checkout remote 
    $ git fetch upstream
    $ git pull
    #Alternativ: $ git merge
</code></pre>

7.  Make your changes and add it to your GitHub-Repository
<pre><code>  
    $ git add file
    $ git commit -m "message"
    $ git push origin main
</code></pre>

8. Create an PR within Github to transfer changes to the foreign GitHub-Repository
9. Waiting for apporval and merge in the foreign repositroy
10. Fetch and merge changes back to your repoistory

