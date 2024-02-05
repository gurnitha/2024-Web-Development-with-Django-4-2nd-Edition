# 2024-Web-Development-with-Django-4-2nd-Edition
Belajar membangun aplikasi buku review berdasarkan buku 'Web Develoment with Django 4 2nd Edition'
Github repositori: https://github.com/gurnitha/2024-Web-Development-with-Django-4-2nd-Edition
Lokal repositori: E:\_WORKSPACE\2024\django\EBOOK-BASED-PROJECTS\2024-Web-Development-with-Django-4-2nd-Edition


## 1. SETUP


#### 1. Membuat linkungan virtual 'venv312501'

        modified:   README.md        

        λ REM: Membuat linkungan virtual

        λ python --version
        Python 3.12.1
        λ pip --vesion
        λ pip --version
        pip 23.3.2 
        λ python -m venv venv312501 --prompt dj5-bookr


#### 2. Mengaktifkan venv312501

        modified:   README.md 

        λ REM: Mengaktifkan venv312501
        λ venv312501\Scripts\activate.bat
        (dj5-bookr) λ


#### 3. Menginstal Django versi 5.0.1

        modified:   README.md 

        (dj5-bookr) λ pip install django==5.0.1
        Collecting django==5.0.1
        ...
        Successfully installed asgiref-3.7.2 django-5.0.1 sqlparse-0.4.4 tzdata-2023.4

        [notice] A new release of pip is available: 23.2.1 -> 24.0
        [notice] To update, run: python.exe -m pip install --upgrade pip


#### 3. Git commit 

        (dj5-bookr) λ git add .

        (dj5-bookr) λ git status
        On branch main
        Your branch is ahead of 'origin/main' by 3 commits.
         (use "git push" to publish your local commits)

        Changes to be committed:
         (use "git restore --staged <file>..." to unstage)
        modified:   README.md

        (dj5-bookr) λ git commit -am "3. Menginstal Django versi 5.0.1"
        [main 51d6231] 3. Menginstal Django versi 5.0.1
         1 file changed, 12 insertions(+)


#### 4. Meng-upload (push) file proyek ke remote repositori di Github

        (dj5-bookr) λ git status
        On branch main
        Your branch is ahead of 'origin/main' by 5 commits.
          (use "git push" to publish your local commits)

        nothing to commit, working tree clean

        E:\_WORKSPACE\2024\django\EBOOK-BASED-PROJECTS\2024-Web-Development-with-Django-4-2nd-Edition\the-project(main -> origin)
        (dj5-bookr) λ git push
        Enter passphrase for key '/c/Users/ING/.ssh/id_rsa':
        Enumerating objects: 17, done.
        Counting objects: 100% (17/17), done.
        Delta compression using up to 8 threads
        Compressing objects: 100% (15/15), done.
        Writing objects: 100% (15/15), 2.08 KiB | 532.00 KiB/s, done.
        Total 15 (delta 4), reused 0 (delta 0), pack-reused 0
        remote: Resolving deltas: 100% (4/4), done.
        To github.com:gurnitha/2024-Web-Development-with-Django-4-2nd-Edition.git
          942461e..f9ec014  main -> main


#### 5. Membenahi README.md file

        modified:   README.md 

        Note: Membenahi bagian no. 2


## 2. MEMBUAT PROYEK DAN APPS DJANGO


#### 1. Membuat proyek django dengan nama: bookr

        (dj5-bookr) λ REM: Memastikan django telah terinstal

        (dj5-bookr) λ pip list
        Package  Version
        -------- -------
        asgiref  3.7.2
        Django   5.0.1
        pip      23.2.1
        sqlparse 0.4.4
        tzdata   2023.4

        [notice] A new release of pip is available: 23.2.1 -> 24.0
        [notice] To update, run: python.exe -m pip install --upgrade pip

        (dj5-bookr) λ REM: Memeriksa perintah untuk membuat proyek django
        
        (dj5-bookr) λ django-admin

        ...
            startapp
            startproject <----
        ...

        (dj5-bookr) λ REM: Membuat proyek django

        (dj5-bookr) λ django-admin startproject bookr .

        modified:   README.md
        new file:   bookr/__init__.py
        new file:   bookr/asgi.py
        new file:   bookr/settings.py
        new file:   bookr/urls.py
        new file:   bookr/wsgi.py
        new file:   manage.py


#### 2. Memeriksa struktur proyek

        (dj5-bookr) λ tree /f

        E: the-project
        │   .gitignore
        │   manage.py
        │   README.md
        │
        └───bookr
                asgi.py
                settings.py
                urls.py
                wsgi.py
                __init__.py  


#### 3. Meng-upgrade pip
      
        (dj5-bookr) λ REM: Perintah meng-upgrade pip
      
        (dj5-bookr) λ python.exe -m pip install --upgrade pip
        ...
        Successfully installed pip-24.0  


#### 4. Menjalankan django development (lokal) server

        (dj5-bookr) λ REM: Memerikasa file

        (dj5-bookr) λ ls
        bookr/  manage.py*  README.md

        (dj5-bookr) λ REM: Memerikasa perintah untuk menjalankan server

        (dj5-bookr) λ python manage.py

        ...
            runserver

        (dj5-bookr) λ REM: Menjalankan server

        (dj5-bookr) λ python manage.py runserver
        Watching for file changes with StatReloader
        ...
        February 05, 2024 - 08:36:10
        Django version 5.0.1, using settings 'bookr.settings'
        Starting development server at http://127.0.0.1:8000/
        Quit the server with CTRL-BREAK.


#### 5. Membuat aplikasi django dengan nama: app_reviews

        (dj5-bookr) λ REM: Memeriksa perintah membuat aplikasi

        (dj5-bookr) λ python manage.py

        ...
            startapp <----
            startproject

        (dj5-bookr) λ REM: Membuat aplikasi reviews di dalam folder khusus 'apps'

        (dj5-bookr) λ mkdir apps
        (dj5-bookr) λ mkdir apps\reviews
        (dj5-bookr) λ python manage.py startapp reviews apps\reviews <----

        modified:   README.md
        new file:   apps/reviews/__init__.py
        new file:   apps/reviews/admin.py
        new file:   apps/reviews/apps.py
        new file:   apps/reviews/migrations/__init__.py
        new file:   apps/reviews/models.py
        new file:   apps/reviews/tests.py
        new file:   apps/reviews/views.py

        NOTE:

        1. Aplikasi reviews dibuat di dalam folder khusus 'apps'


#### 6. Meregistrasi aplikasi reviews pada bookr/settings.py

        modified:   README.md
        modified:   apps/reviews/apps.py
        modified:   bookr/settings.py




































