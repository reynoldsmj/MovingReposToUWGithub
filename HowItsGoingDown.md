# UW-Libraries GitHub Moving to UW GitHub Service On/After July 8th!

## Background
UW has contracted with Github to provide UW departments with fully-featured Github organizations (teams) upon request. See https://uw.service-now.com/sp?id=sc_entry&sys_id=9fb5de4e13777f0811cdd2f18144b01f for details. We have requested that our "UW-Libraries" Github organization be migrated to the UW Github service. This will enable us to save the cost of a separate subscription to Github (and maybe more benefits, such as larger storage capacity? not sure)

## When?
The request to move us will be submitted to Github on July 8th. Sometime that day or shortly thereafter, UW-Libraries will be moved to the UW Github service. We will not be notified.

## How Will This Impact Me?
Once UW-Libraries has moved, you will need to link your Github account to your UWNetID. This will happen automatically the first time you sign into github.com using your Github account and visit our UW-Libraries organization. (Unclear exactly what the steps are, but apparently they are user-friendly enough that UW does not feel the need to document them.) Also, any SSH key you have set up in your user profile for password-less access to the UW-Libraries Github organization (e.g. for git access to the uwlib-ansible Ansible on leguinn) will not work until you manually authorize that key for use with the UW Shibboleth Single-Sign-On (SSO) service.

## How Do I Authorize My Personal SSH Key for SSO?
Click your profile photo, click Settings, click SSH and GPG Keys, click Enable SSO. Find "UW-Libraries" organization, click Authorize. 
See https://docs.github.com/en/github/authenticating-to-github/authorizing-an-ssh-key-for-use-with-saml-single-sign-on for a nice graphical walk-thru

## Will This Break All My Other Shit?
It shouldn't. For instance, if you're using deploy keys to enable Ansible to fetch a UW-Libraries Github repo, your deploy key should still work. (See https://docs.github.com/en/developers/overview/managing-deploy-keys for more information about repo deploy keys for Github.)
