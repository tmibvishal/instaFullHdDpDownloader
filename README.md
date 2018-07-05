# instaFullHdDpDownloader
Download Full Size HD profile picture of instagram profile

# Algorith For the Program

1. Visit this page after replacing name with username of insta that you are looking for. https://apinsta.herokuapp.com/u/name. Source: http://stackoverflow.com
2. This is a JSON-Code file. You need to search for the user-id: graphql->user->id
3.Visit this API-Page of instagram https://i.instagram.com/api/v1/users/user-id/info/ and replace user-id with the id from step 2
4.This is a JSON-Code. Search for the link: user->hd_profile_pic_url_info->url. This is the full size image.
