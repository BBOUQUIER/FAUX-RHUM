## How to run this project
Open this directory in your favorite editor (VS code, Atom...)<br>
Write these commands in the terminal :<br>
    
    go get github.com/mattn/go-sqlite3
    
    go get github.com/satori/go.uuid
    
    go get golang.org/x/crypto/bcrypt
    
    go get golang.org/x/oauth2
    
    go get golang.org/x/oauth2/facebook
    
    go get golang.org/x/oauth2/google

    go run ./main.go

Open your browser and go to "localhost:8000"<br>
/!\ facebook and google registration are probably down due to expired token. /!\ <br><br>


# Projet-Forum

This project was about making a forum where only registered users can post, comment posts, like and dislike. Non-registered users (Guests) can see those posts and comments but cannot reply nor like.<br><br>

Everything is stored in a database (Sqlite3). <br>
- Such as users and their informations : email address, username, profile picture, id... <br>
- Posts with the original writer, id, categories, date of publication, number of like/dislike...<br>
- Comments with the id of the original post, the writer of the comment..
- Categories with their name and color<br>
- And more...<br><br>

There is four roles : Guests, Users, Moderators and Admins.<br>
By default, the first created user become an Admin. Be careful, only Admins can change the role of others Users, so if you delete the first one, you will have to clear the database and restart the app.<br><br>

Guests can only read posts<br>
Users can post, comment posts change their profile, delete and modify their own posts<br>
Moderators can delete or modify, report an abusive user to the admins and accept the pending posts before publishing<br>
Admins can delete, promote or demote any users, delete or create new categories ... <br><br>

------------------------

## Authors

Code writted by **PEYRE Brian**, **DOCKX Sven**, **BOUQUIER Baptiste**, **MORACCHINI Florian**
