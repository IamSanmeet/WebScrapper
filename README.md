# WebScapper

It imports necessary libraries including requests, urlopen from urllib.request, ssl, and BeautifulSoup.

The script defines a URL (url) pointing to a web page from which images will be scraped.

It sends an HTTP request to the specified URL using the requests.get() function to retrieve the HTML content of the web page.

The HTML content is then parsed using BeautifulSoup to create a structured representation of the page's elements.

The script searches for img tags within the parsed HTML, both with data-src and src attributes, which typically contain image URLs.

For each image URL found, the script sends another HTTP request to download the image content.

If the image request is successful (status code 200), the script extracts the image filename from the URL and saves the image content to a file in the same directory as the script.

If an image request fails, the script prints a message indicating the failure.

Once all images are processed, the script displays "Done."

This script essentially scrapes images from the specified web page and downloads them to your local machine. It uses the requests library to interact with web resources and the BeautifulSoup library to parse HTML content and extract image URLs. It's important to note that the script assumes the presence of either data-src or src attributes in img tags to retrieve image URLs.
