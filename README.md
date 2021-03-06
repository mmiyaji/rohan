icat
=====

This script draws image on CUI terminal by ANSI Escape codes.
It can use like a cat command. (image cat -> icat)

------------------
About
------
ターミナルに画像を表示するスクリプト。

[Pythonでターミナルに画像表示するやつ - mmiyajix http://mmiyajix.appspot.com/entry/123001](http://mmiyajix.appspot.com/entry/123001)

引数で与えた画像ファイルをターミナル上でANSI Escape codeを使ってレンダリングするスクリプトです。
256色（xterm-256color）対応。

Require
-----
- Python2.7 or later
    - PIL (Python Image Iibrary) / pillow
    - argparse

pip install
```
$ pip install pillow
$ pip install argparse
```

How to install
-----
    $ git clone https://github.com/mmiyaji/icat.git
    $ cd icat
    $ sudo ./install.sh
    or
    $ ./install.sh --prefix=/usr/local


    Usage: [sudo] install.sh [options]

    Options (see top of install.sh for complete list):

    -h | --help
        Display this message.

    --with-python=/full/path/to/python
        Path to the Python that you wish to use with icat.
        default:  /usr/bin/python

    --prefix=/full/path/to/install
        Path to the install directoey that you wish to use with icat.
        default:  /usr

    test
        module check mode. "icat" does not install in this time.


Usage
-----
    e.g.)
        $ icat github.png
        $ icat -m h github.png
        $ icat -s 100 github.png

    usage: icat [-h] [-v] [-s SIZE] [-m {w,h}] [-d {8,256}] [-t] [-f FILE]
                    file

    icat is a image viewer on terminal. render with ANSI Escape codes.

    positional arguments:
      file                  set image file path.

    optional arguments:
      -h, --help            show this help message and exit
      -v, --version         show program's version number and exit
      -s SIZE, --size SIZE  set image width. image width fit to number of
                            character.
      -m {w,h}, --mode {w,h}
                            choice view mode. if you set "w", image width fit to
                            screen width. the case of "h", fit to screen height.
                            this option's effect is less than the size option.
      -d {8,256}, --depth {8,256}
                            set color depth. support 8(ansi) and 256(xterm-256).
      -t                    output with text format(write #).
      -f FILE, --file FILE  set image file path.

Screenshot
-----
![icat1](https://raw.githubusercontent.com/mmiyaji/icat/master/screenshot/icat1.PNG)
![icat2](https://raw.githubusercontent.com/mmiyaji/icat/master/screenshot/icat2.PNG)
![icat3](https://raw.githubusercontent.com/mmiyaji/icat/master/screenshot/icat3.PNG)


# License
The MIT License


Copyright (c) 2013 Masahiro MIYAJI


Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

以下に定める条件に従い、本ソフトウェアおよび関連文書のファイル（以下「ソフトウェア」）の複製を取得するすべての人に対し、ソフトウェアを無制限に扱うことを無償で許可します。これには、ソフトウェア
の複製を使用、複写、変更、結合、掲載、頒布、サブライセンス、および/または販売する権利、およびソフトウェアを提供する相手に同じことを許可する権利も無制限に含まれます。

上記の著作権表示および本許諾表示を、ソフトウェアのすべての複製または重要な部分に記載するものとします。

ソフトウェアは「現状のまま」で、明示であるか暗黙であるかを問わず、何らの保証もなく提供されます。ここでいう保証とは、商品性、特定の目的への適合性、および権利非侵害についての保証も含みますが、そ
れに限定されるものではありません。 作者または著作権者は、契約行為、不法行為、またはそれ以外であろうと、ソフトウェアに起因または関連し、あるいはソフトウェアの使用またはその他の扱いによって生じる一切の請求、損害、その他の義務について何らの責任も負わないものとします。
