# Collab_Branch_Workflow

Esercizio sul workflow collaborativo

## The problem

While it's nice and easy to onlt work on the master branch, this leads to some serious issues on teams!

* Lots of time spent resolving conflicts and merging code, especially as team size scales up

* No one can work on anything without disturbing the main codebase. How do you try adding something radically different in? How do you experiment?

* The only way to collaborate on a feature together with another teammate is to push incomplete code to master/main. Other teammates now have broken code...

## Feature Branches

Rather than working directly on master/main, all new development should be done on separate branches.

* Treat master/main branch as the official project history

* Multiple teamates can collaborate on a single feature and share code back and forth without polluting the master/main branch

* Master/main branch won't contain broken code, or at least, it won't unless someone messes up.

## Merging in Feature branches

At some point the new work on feature branches will need to be merged in to the master branch.

There are a couple of options for how to do this:

1. Merge _at will_ without any sort of discussion with teammates. Just _do it whenever you want_ .

2. Send an email or chat message or something to your team to discuss if the changes should be merged in.

3. **Pull Request!**
