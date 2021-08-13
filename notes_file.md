
from github import GitHub  --- github import
g = Github("user token") ---  USING ACCESS TOKEN FOR USER


for repo in g.get_user("kbeeperez").get_repos(): -- get repos ONLY user owns. if you do not specify a user it will
    print(repo.name)                            --- grab all the repos the authorized user is a part of.


repo = g.get_repo("kbeeperez/github-api-tester") -- name repo you would like to create the file in
repo.create_file("file name.type", "commit message", "file contents", branch="name_of_branch")
  - **"file contents" can hold large bodies of text using (three single quotes) *body of text* (three single quotes)**

pr = repo.create_pull(title="PR title", body=*create a var 'body' ex. below*, head="*name of the branch to be merged into main*", base=*main/master*)


