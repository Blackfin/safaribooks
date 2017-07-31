# safaribooks
Convert safaribooksonline ebook to Kindle format

# Usage

1. Download kindlegen from Amazon: https://www.amazon.com/gp/feature.html?docId=1000765211 
   
   Bullet list:
     * create file kindlegen with content:
     
     ```bash
     #!/bin/sh
     /home/user/KindleGen/kindlegen $1
     ```

     * Put the kindlegen file somewhere in PATH, for example: /bin/kindlegen and execute `chmod a+x /bin/kindlegen`

     * Check the README: https://kindlegen.s3.amazonaws.com/Readme.txt
    
   If you only need epub books this step can be skipped.

2. Make sure you have Python, Scrapy, jinja2, beautifulsoup are installed.
   
   Then run `./craw.sh user password bookid book-name`.
   
   Where the bookid is the id in url such as `https://www.safaribooksonline.com/library/view/real-world-machine-learning/9781617291920/kindle_split_011.html` (9781617291920 in this case) when you read books in safaribooksonline.
   
   Full cmd line for run: `./crawl.sh user password 9781617291920 real-world-machine-learning`.

3. An epub and mobi file will be generated and placed in programm directory.
   
