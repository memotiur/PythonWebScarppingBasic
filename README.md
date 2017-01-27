# PythonWebScarppingBasic

''' Get source code
import bs4 as bs
import urllib.request

source = urllib.request.urlopen('https://pythonprogramming.net/parsememcparseface/').read()
soup = bs.BeautifulSoup(source,'lxml')
print (soup)
'''

#Get Title
import bs4 as bs
import urllib.request
#url="https://pythonprogramming.net/parsememcparseface/";
url="http://www.prothom-alo.com"
source = urllib.request.urlopen(url).read()
soup = bs.BeautifulSoup(source,'lxml')
#print (soup.title)
#print (soup.title.string)#also work for text
#print (soup.p)
#print (soup.find_all('p'))
#print (soup.find_all('p'))
#for paragraph in soup.find_all('p'):
#	print(paragraph.text)
print(soup.get_text())
for url in soup.find_all('a'):
	#print(url.text)
        print(url.get('href'))
#print(soup.get_text())
'''
body=soup.body
for paragraph in body.find_all('p'):
	#print(url.text)
	print(paragraph.text)

'''
