import requests
from bs4 import BeautifulSoup
import webbrowser

def open_download_pages(file_path):
    with open(file_path, 'r') as file:
        urls = file.readlines()

    for url in urls:
        url = url.strip()
        response = requests.get(url)
        soup = BeautifulSoup(response.text, 'html.parser')
        download_links = soup.find_all('a', text='Download')

 #       if len(download_links) == 0:
 #           print(f"No download links found for URL: {url}")
        continue

        for link in download_links:
            download_url = link.get('href')
            webbrowser.open(download_url)

# Example usage
file_path = "/Users/kampaysalut/Desktop/urls.txt"
open_download_pages(file_path)
