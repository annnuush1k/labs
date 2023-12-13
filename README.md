lab1

 1. Ստեղծել lab1 անունով դիրեկտորիա, որում ստեղծել 4 տեքստային ֆայլ՝ file.txt, file1.txt,
file2.txt, file3.txt և 2 դիրեկտորիա՝ dir1, dir2։

Professional@User-PC MINGW64 ~
$ mkdir lab1

Professional@User-PC MINGW64 ~
$ cd lab1/

Professional@User-PC MINGW64 ~/lab1
$ touch file.txt file1.txt file2.txt file3.txt

Professional@User-PC MINGW64 ~/lab1
$ mkdir dir1 dir2


2. Կատարել հետևյալ հրամանները և բացատրել տարբերությունը։

Professional@User-PC MINGW64 ~/lab1
$ ls *.txt
file.txt  file1.txt  file2.txt  file3.txt

Professional@User-PC MINGW64 ~/lab1
$ ls * .txt
ls: cannot access '.txt': No such file or directory
file.txt  file1.txt  file2.txt  file3.txt

dir1:

dir2:
 
//Տարբերությունը՝
ls *.txt կփնտրի և կարտածի ֆալերը որոնց անունները
վերջանում է *.txt ֆայլեր
ls * .txt կփնտրի և ցույց կտա տվյալ ինչ-որ ․txt ֆայլ։


3. Ցուցադրել բոլոր տեքստային ֆայլերը (ավարտվում է .txt սիմվոլներով), որոնց
անվանումը սկսվում է f սիմվոլով և բաղկացած է 4 սիմվոլից։

Professional@User-PC MINGW64 ~/lab1
$ ls f???.txt
file.txt


4. Ցուցադրել բոլոր տեքստային ֆայլերը, որոնց անվանումը սկսվում է file բառով, որին
հաջորդում է թվանշան։

Professional@User-PC MINGW64 ~/lab1
$ ls file[[:digit:]].txt
file1.txt  file2.txt  file3.txt


5. Ցուցադրել բոլոր տեքստային ֆայլերը, որոնց անվան վերջին սիմվոլը փոքրատառ է,
կամ 1, 2 թվանշաններից որևէ մեկը։

Professional@User-PC MINGW64 ~/lab1
$ ls *[[:lower:]12].txt
file.txt  file1.txt  file2.txt
//կամ հետևյալ հրամանների միջոցով․
ls *[a-z12].txt
ls *[a-z,12].txt


6. Պատճենել /etc/passwd ֆայլը lab1 դիրեկտորիայում։

Professional@User-PC MINGW64 ~/lab1
$ cp /etc/passwd passwd


7. Անվանափոխել պատճենված ֆայլը՝ այն դարձնելով new: Տեղափոխել new ֆայլը դեպի
dir1, այնուհետև տեղափոխել դեպի dir2:

Professional@User-PC MINGW64 ~/lab1
$ mv passwd new

Professional@User-PC MINGW64 ~/lab1
$ mv new dir1/

Professional@User-PC MINGW64 ~/lab1
$ mv dir1/new dir2/


8. Անվանափոխել dir2-ը՝ այն դարձնելով dir3։ Տեղափոխել dir3-ը դեպի dir1։

Professional@User-PC MINGW64 ~/lab1
$ mv dir2 dir3

Professional@User-PC MINGW64 ~/lab1
$ mv dir3 dir1/


9. Տեղափոխել dir3-ում գտնվող new ֆայլը դեպի lab1։

Professional@User-PC MINGW64 ~/lab1
$ mv dir1/dir3/new ./


10. Ջնջել lab1 դիրեկտորիան։

Professional@User-PC MINGW64 ~/lab1
$ cd ..

Professional@User-PC MINGW64 ~
$ rm -r lab1
