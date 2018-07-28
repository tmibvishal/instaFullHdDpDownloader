# instaFullHdDpDownloader
Download Full Size HD profile picture of instagram profile. I have provided the algorithm that I have used and also the Usage just in case you want to directly use my javascript file for your web apps and android apps.

# For live program you can check this site
https://tmibvishal.github.io/instaDpDownloader/

# Algorith For the Program

1. Visit this page after replacing name with username of insta that you are looking for. https://apinsta.herokuapp.com/u/name. Source: http://stackoverflow.com
2. This is a JSON-Code file. You need to search for the user-id: graphql->user->id 
3. Visit this API-Page of instagram https://i.instagram.com/api/v1/users/user-id/info/ and replace user-id with the id from step 2 
4. This is a JSON-Code. Search for the link: user->hd_profile_pic_url_info->url. This is the full size image.

# Usage

Include this javascript file in your project
File size is 1.16 KB
```html
<script src="https://tmibvishal.github.io/instaDpDownloader/instaHDFullImage.js"></script>
```

## how to use the hdImage function from this java script file

Call hdImage with these parameters
```javascript
hdImage("username", success_function , username_not_found_error_function);
```



## sample html project using this javascript file

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
    <script src="https://tmibvishal.github.io/instaDpDownloader/instaHDFullImage.js"></script>
    <script>
        $(document).ready(function() {
            let textBox = $('#textBox');
            let btnSubmit = $('#btnSubmit');
            btnSubmit.click(function () {
                hdImage(textBox.val(),function(hdimage){
                    let imgParent = $('#imgParent');
                    let value = `<img src="${hdimage}">`;
                    imgParent.text("");
                    imgParent.append(value);
                },function(){console.log("Error")});
            });
            // hdImage("username", success_function , username_not_found_error_function); hdImage function will work like this
        });
    </script>
</head>
<body>
        <input type="text" id="textBox">
        <input type="submit" id="btnSubmit"></input>
        <div id="imgParent"></div>
</body>
</html>
```
