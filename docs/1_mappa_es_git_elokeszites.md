1. Mappaszerkezet
2. Git inicializálás
    - .gitignore:
        * text=auto eol=lf

        *.png binary
        *.jpg binary
        *.jpeg binary
        *.gif binary
        *.ico binary
        *.woff binary
        *.woff2 binary
    - .gitattributes:
        #helyi kornyezet
        .env
        .env.*
        !.env.example

        #fuggosegek
        backend/vendor/
        frontend/node_modules/

        #build kimenet
        frontend/dist/

        #laravel futas kozbeni fajlok
        backend/storage/*.key
        backend/storage/logs/*.log
        backend/bootstrap/cache/*.php
        backend/public/hot
        backend/public/storage

        #vsc filejai
        .idea/
        .vscode/
        .DS_Store
        thumbs.db
        *.log
        
    - git init; git status; git add .; git commit -m "message";
3. Lokális repo feltöltése githubra:
    - Githubon a távoli repo létrehozása
    - git branch -M main
    - git remote add origin https://github.com/rises3/todo-app
    - ellenorzo parancsok: git config user.name; git config user.email
    - bongeszos autentikacio elfogadasa
    - git push -u origin main