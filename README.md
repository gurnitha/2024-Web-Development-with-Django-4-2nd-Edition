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
		(dj5-bookr) λ

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



















