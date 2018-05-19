mkdir /tmp/svnproject
cd /tmp/svnproject
/tmp/svnproject$ svnadmin create sample
/tmp/svnproject$ svn ls file:///tmp/svnproject/sample/
/tmp/svnproject$ svn mkdir file:///tmp/svnproject/sample/trunk -m "make trunk"

Committed revision 1.
/tmp/svnproject$ svn co file:///tmp/svnproject/sample/trunk /tmp/svnproject/trunk/
Получена редакция 1.
/tmp/svnproject$ cd /tmp/svnproject/trunk/
/tmp/svnproject/trunk$ echo "test" > test.txt
/tmp/svnproject/trunk$ svn add test.txt
A         test.txt
/tmp/svnproject/trunk$ svn commit -m "First commit"
Добавляю          test.txt
Передаю данные .
Committed revision 2.
/tmp/svnproject/trunk$ svn log
------------------------------------------------------------------------
r1 | jurinva | 2018-05-20 02:09:04 +0300 (Вс., 20 мая 2018) | 1 line

make trunk
------------------------------------------------------------------------