# OCR++ : A Framework to extract information from Scholastic Articles 

NOTE : The tool works only on Linux-based systems

##### Installation : 
  - Install the dependencies.
  - Clone this repo and copy the OCR++ folder in  **/var/www/html** and make a directory named "**media**" in **/var/www/html**
  
      ```sh
      git clone https://github.com/ocrplusplus/ocrplusplus
      cd ocrplusplus
      mkdir -p /var/www/html/media
      mkdir -p /var/www/html/media/documents
      cp -r OCR++ /var/www/html/ 
      ```
  - If you are using an apache server, run this command too

##### Usage:
  - ###### With localhost as server :
    - Run the following commands : 
    
        ```sh
        cd /var/www/html/OCR++
        python manage.py runserver
        ```
    - Now open a web-browser and go to **127.0.0.1:8000/home**
    
  - ###### Without a server : 
    - Rename and cpoy the pdf as "**input.pdf**" on which you want to run OCR++ in the given directory using the command 
    
        ```sh
        cp path/to/pdf /var/www/html/OCR++/myproject/media/documents/input.pdf
        ```
    - run the OCR++ engine by running the Script
    
        ```sh
        cd /var/www/html/OCR++/myproject/media/documents/
        python main_script_batch.py
        ```

##### Dependencies:
    - nltk
    - django (Only if you want to run it as a server)
    - crfpp
    
