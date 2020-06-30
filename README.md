# MovingReposToUWGithub

Per younga3, two steps:

1. Get a UW Gibhub account (appears this step can also migrate our UW-Libraries organization to the UW Github)
1. Move all our bitbucket repos to our UW Github

## Getting a UW Github account
### 2020.06.29 requested that UW-Libraries org be migrated to UW Github (filled out form)
* form had "questions" box where i asked if moving to UW would break anything
* did request from my personal netid, so whole move thing tied to my netid. oops

## Migrating Bitbucket Repos
OK, so the only problem with migrating Bitbucket repos is, I think, that any that are tied to Ansible will need to have Ansible "git" paths updated
I guess I can start by migrating one or two of my repos
* Then share with group steps to take
* Then migrate rest of my own repos
* Then help others with repo migration as needed

## Instructions from UWIT
From UW REQ3717904 ] UW GitHub Enterprise: migrate https://github.com/UW-Libraries:
```
It depends.
After your organization is migrated, members will have to authenticate with a UW NetID to access it. GitHub accounts that haven't previously been linked to a NetID will be automatically linked to the authenticating NetID the first time a connection is made. Users will also have to authorize SSH keys and other tokens for use with a Single Sign-On identity. So to answer your question, integrations that depend on SSH keys and access tokens will have interrupted service after the migration until the accounts that own those credentials complete the SSO authorization step. Complete information on using Single Sign-On identities is available from GitHub.
If you have users without NetIDs, they can be given access on a per-repository basis as "outside collaborators", or you can get them sponsored NetIDs. You must also use a shared NetID to authenticate any system/bot accounts with access to your organization. Shared and sponsored NetIDs must be granted permission on our side to authenticate to GitHub; you can provide us with any such NetIDs that need access.
Repository URLs will not change, and installed GitHub Apps should still work without interruption.
If you tell me a bit more about your Ansible setup and what accesses what from where I may be able to offer more specific predictions/guesses about what will happen.
We've been asked to limit requests for migration to once a month, since this is currently done by GitHub's support staff. I plan to make my next request around July 8, but no other requests are pending right now so I can probably wait until you're ready to go even if it takes longer than that. Let me know if you have further questions.
Evan Silberman
Service Manager, Developer & Integration Tools
UW-IT
```

So I believe that, mostly, our github accounts provide access to all our repos (primary one being our github info-hole "ids-docs" doc repo.
The outlier is the "uwlib-ansible" repo. I believe that each of us who uses this repo from leguinn has set up a private key at leguinn and has added the corresponding public key at github that permits our leguinn logon to commit ansible changes from leguinn to the github repo. (At least, that's how mine is set up.)

I will write back to Evan describing our setup to confirm what I think will happen when we move, which is:
We move organization
For each of our users
  first time visiting github web site, will get prompted for uwnetid auth, which will link github account with uwnetid
  I *believe* at that point that if the user has a public key in their github account profile, they will get prompted to somehow authorize those public keys. Once this is done, the user should be able to do ansible repo updates from leguinn
  
Also the issue of repo access keys. asked uwit guy separately about
