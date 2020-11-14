# RoutineHubDocs

All API endpoints are at the https://routinehub.co/api/v1/ url. Where api_key is needed, the user will have to generate it from their settings page and provide it to you. Preferred that this be stored locally to the user's system and not on your servers anywhere.

Here are the endpoints:

## List User's Shortcuts
> GET 'api/v1/<api_key>/shortcuts'

Simply retrieves a list of the user's shortcuts with their IDs and whether it's published or not.

## Create Shortcut version
> POST 'api/v1/<api_key>/shortcuts/<shortcut_id>/versions/create'

Creates a new version for a shortcut. 

Parameters:
'version' : The version number
'link' : Link to the shortcut on iCloud
'changes' : List of changes for this version

## Publish Shortcut
> POST 'api/v1/<api_key>/shortcuts/<shortcut_id>/publish'

Changes the publish status of a shortcut to True.

## Unpublish Shortcut
> POST 'api/v1/<api_key>/shortcuts/<shortcut_id>/unpublish'

Changes the publish status of a shortcut to False.

## Get latest Shortcut version
> GET 'api/v1/shortcuts/<shortcut_id>/versions/latest'

Gets the latest version of a shortcut. No api key needed.
