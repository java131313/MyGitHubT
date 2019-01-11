在 python 源码文件中用 utf-8 文字。一般会报错，如下：

File "F:\workspace\psh\src\test.py", line 2
SyntaxError: Non-ASCII character '\xe4' in file F:\workspace\psh\src\test.py on line 2, but no encoding declared; see http://www.python.org/peps/pep-0263.html for details
test.py 的内容：

print "你好"  
如果要正常运行在 test.py 文件前面加编码注释，如：

#!/usr/bin/python2.6  
# -*- coding: utf-8 -*-  
print "你好"  
或者加入：

import sys
reload(sys)
sys.setdefaultencoding('utf-8')
