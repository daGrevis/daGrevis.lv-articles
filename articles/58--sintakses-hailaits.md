# Sintakses hailaits

Tik tikko realizēju vēl vienu ideju, kas jau bija radusies diezgan sen — sintakses hailaits!

Lūk, mans nesen rakstītais Python kods piemēram:

<pre><code data-language="python">import os
import sys
import urllib
from pyquery import PyQuery

url = 'http://dagrevis.lv'
selector = 'img'
storage_dir = 'temp'


def main():
    dom = PyQuery(url=url)
    image_nodes = dom(selector)
    links_to_images = []
    if not os.path.isdir(storage_dir):
        os.mkdir(storage_dir)
    i = 1
    for node in image_nodes:
        src = PyQuery(node).attr('src')
        bin = urllib.urlopen(src)
        ext = os.path.splitext(src)[1]
        f = open(storage_dir + '/' + str(i) + ext, 'w+')
        f.write(bin.read())
        f.close()
        i = i + 1
    print('All done')

if __name__ == '__main__':
    main()
</code></pre>

P.S. Sintakses hailaits pilnībā ir realizēts klienta-pusē, izmantojot [Rainbow](http://craig.is/making/rainbows).