## BASIC Django code


**1.  Windows10 64bit install error 


   **case1) 'mysql.h': No such file or directory

      shell >  pip install wheel

            and then, download install file for python 3.x and windows 64bit from
      
            http://www.lfd.uci.edu/~gohlke/pythonlibs/#mysql-python
      
      shell > pip install mysqlclient-1.3.13-cp36-cp36m-win_amd64.whl (depend on python version)

   **case2) 'config-win.h': No such file or directory

      shell > pip install mysql




**2. mySQL connection error


      After you set settings.py 'DATABASES' like this,
      

      DATABASES = {
          'default': {
              'ENGINE': 'django.db.backends.mysql',
              'NAME': 'test',
              'USER': 'test',
              'PASSWORD': 'test',
              'HOST': '127.0.0.1',
              'PORT': '0000'
          }
      }


      and if you face to error below,
      


   **case1) django.db.utils.OperationalError: (2059, <NULL>)
      

      then, you can modify 'ENGINE' to 

      'ENGINE': 'mysql.connector.django',


      or you should check whether 'NAME' is correct or not.
