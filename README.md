# RoutineHubDocs - API

Root URL: `https://routinehub.co/api/v1/`

All API endpoints are based on the root url. 

##### Table of Content

> * [Shortcut ID](#shortcut-id)
> * [API Key](#api-key)<br>
>   * [Key Generation](#key-generation)<br>
>   * [Revoke Key](#revoke-key)<br>
>   * [Storage](#storage)<br>
> * [GET Endpoints](#get-endpoints)<br>
>   * [List User Shortcuts](#list-user-shortcuts)<br>
>   * [Get Latest Shortcut Version Info](#get-latest-shortcut-version)<br>
> * [POST Endpoints](#post-endpoints)<br>
>   * [Create Shortcut version](#create-shortcut-version)<br>
>   * [Publish Shortcut](#publish-shortcut)<br>
>   * [Unpublish Shortcut](#unpublish-shortcut)<br>

## Shortcut ID
The <shortcut_id> is a numeric ID assigned to the shortcut on the site when a new shortcut is created.

To find this ID after creating the shortcut on RoutineHub, tap/click on the address bar and view the 1-4 digit number.

Example: https://routinehub.co/shortcut/7388/version/create<br>
RoutineHub Shortcut ID: 7388

-----
## API Key

### Key Generation
Where <api_key> is needed, the user has to generate the key. This can be done from the RoutineHub settings page. 

### Revoke Key
It is not currently possible to revoke a key, but if you generate a new key, the old key will become invalid 

### Storage
It is Preferred that this be stored locally to the user's system and not on your servers anywhere.

----
## GET Endpoints

### List User Shortcuts
`GET 'api/v1/<api_key>/shortcuts'`

Simply retrieves a list of the user's shortcuts with their IDs and whether it's published or not.

### Get Latest Shortcut Version Info
`GET 'api/v1/shortcuts/<shortcut_id>/versions/latest'`

Gets the latest version of a shortcut. No api key needed.

-----
## POST Endpoints

### Create Shortcut version
`POST 'api/v1/<api_key>/shortcuts/<shortcut_id>/versions/create'`

Creates a new version for a shortcut. 

Parameters:<br>
'version' : The version number
'link' : Link to the shortcut on iCloud
'changes' : List of changes for this version

### Publish Shortcut
`POST 'api/v1/<api_key>/shortcuts/<shortcut_id>/publish'`

Changes the publish status of a shortcut to True.

### Unpublish Shortcut
`POST 'api/v1/<api_key>/shortcuts/<shortcut_id>/unpublish'`

Changes the publish status of a shortcut to False.


