https://stackoverflow.com/questions/24844729/download-pdf-using-urllib



import urllib2

def main():
    download_file("http://mensenhandel.nl/files/pdftest2.pdf")

def download_file(download_url):
    response = urllib2.urlopen(download_url)
    file = open("document.pdf", 'wb')
    file.write(response.read())
    file.close()
    print("Completed")

if __name__ == "__main__":
    main()
