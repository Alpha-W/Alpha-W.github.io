==========================
批量转换djvu为pdf
==========================
:Author: Hau Wong
:Date:   2018-11-22
:Category: 程序

利用python写了一个批量转换djvu为pdf的脚本。

.. code:: python

   import os
   import subprocess as sp
   finished=0
   path='/home/hau/Ebook'
   os.chdir(path)
   for foldernames,subfolders,filenames in os.walk(path):
        for file in filenames:
            if file.endswith(".djvu"):
                sp.run(['echo \"'+str(file)+'\" >>log.txt'],shell=True)
                sp.run(["ddjvu -format=tiff "+foldernames+'/'+str(file)+" "+foldernames+'/'+str(file)[:-5]+".tiff 2>>log.txt"],shell=True)
                sp.run(["tiff2pdf -j -o "+foldernames+'/'+str(file)[:-5]+".pdf "+foldernames+'/'+str(file)[:-5]+".tiff 2>>log.txt"],shell=True)
                if os.path.exists(foldernames+'/'+str(file)[:-5]+".pdf"):
                    os.unlink(foldernames+'/'+str(file))
                    os.unlink(foldernames+'/'+str(file)[:-5]+".tiff")
                    finished=finished+1
                    print(finished)
