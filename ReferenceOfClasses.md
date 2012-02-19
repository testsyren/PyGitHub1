You don't normaly create instances of any class but `Github`.
You obtain instances through calls to `get_` and `create_` methods.

In this documentation:

* `login` is a string containing a user's or organization's login
* `user` is an instance of `AuthenticatedUser` or `NamedUser`
* `name` is a string containing the name of a repository
* `repo` is an instance of `Repository`

Class `Github`
==============
* Constructed from user's login and password
* `get_user()`: `AuthenticatedUser`
* `get_user( login )`: `NamedUser`
* `get_organization( login )`: `Organization`

Class `AuthenticatedUser`
=========================
* Attributes: see [API](http://developer.github.com/v3/users/#get-the-authenticated-user)
* `edit( ... )`: see [API](http://developer.github.com/v3/users/#update-the-authenticated-user) for parameters

Repositories
------------
* `get_repos()`: list of `Repository`: see [API](http://developer.github.com/v3/repos/#list-your-repositories) for `type` parameter
* `get_repo( name )`: `Repository`
* `create_repo( ... )`: `Repository`: see [API](http://developer.github.com/v3/repos/#create) for parameters
* `create_fork( repo )`: `Repository`

Watching
--------
* `get_watched()`: list of `Repository`
* `has_in_watched( repo )`: `bool`
* `add_to_watched( repo )`
* `remove_from_watched( repo )`

Organizations
-------------
* `get_orgs()` : list of `Organization`

Following
---------
* `get_followers()` : list of `NamedUser`
* `get_following()` : list of `NamedUser`
* `has_in_following( user )`: `bool`
* `add_to_following( user )`
* `remove_from_following( user )`

Class `NamedUser`
=================
* Attributes: see [API](http://developer.github.com/v3/users/#get-a-single-user)

Repositories
------------
* `get_repos()`: list of `Repository`: see [API](http://developer.github.com/v3/repos/#list-user-repositories) for `type` parameter
* `get_repo( name )`: `Repository`

Watching
--------
* `get_watched()`: list of `Repository`

Organizations
-------------
* `get_orgs()` : list of `Organization`

Following
---------
* `get_followers()` : list of `NamedUser`
* `get_following()` : list of `NamedUser`

Class `Organization`
====================
* Attributes: see [API](http://developer.github.com/v3/orgs/#get)
* `edit( ... )`: see [API](http://developer.github.com/v3/orgs/#edit) for parameters

Repositories
------------
* `get_repos()`: list of `Repository`: see [API](http://developer.github.com/v3/repos/#list-organization-repositories) for `type` parameter
* `get_repo( name )`: `Repository`
* `create_repo( ... )`: `Repository`: see [API](http://developer.github.com/v3/repos/#create) for parameters
* `create_fork( repo )`: `Repository`

Members
-------
* `get_members()`: list of `NamedUser`
* `has_in_members( user )`: `bool`
* `remove_from_members( user )`
* `get_public_members()`: list of `NamedUser`
* `has_in_public_members( user )`: `bool`
* `add_to_public_members( user )`
* `remove_from_public_members( user )`

Class `Repository`
==================
* Attributes: see [API](http://developer.github.com/v3/repos/#get)
* `edit( ... )`: see [API](http://developer.github.com/v3/repos/#edit) for parameters

Collaborators
-------------
* `get_collaborators()`: list of `NamedUser`
* `has_in_collaborators( user )`: `bool`
* `add_to_collaborators( user )`
* `remove_from_collaborators( user )`

Contributors
------------
* `get_contributors()`: list of `NamedUser`

Watching
--------
* `get_watchers()`: list of `NamedUser`

Forks
-----
* `get_forks()`: list of `Repository`