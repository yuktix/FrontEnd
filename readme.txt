Paste below code When Files are in Deployed in .htacess


# compress text, html, javascript, css, xml:
AddOutputFilterByType DEFLATE text/plain
AddOutputFilterByType DEFLATE text/html
AddOutputFilterByType DEFLATE text/xmlin
AddOutputFilterByType DEFLATE text/css
AddOutputFilterByType DEFLATE application/xml
AddOutputFilterByType DEFLATE application/xhtml+xml
AddOutputFilterByType DEFLATE application/rss+xml
AddOutputFilterByType DEFLATE application/javascript
AddOutputFilterByType DEFLATE application/x-javascript
# Or, compress certain file types by extension:
<files *.html>
SetOutputFilter DEFLATE
</files>

# Turn on Expires and set default to 0
ExpiresActive On
ExpiresDefault A0
# Set up caching on media files for 1 year (forever?)
<FilesMatch "\.(flv|ico|pdf|avi|mov|ppt|doc|mp3|wmv|wav)$">
ExpiresDefault A29030400
Header append Cache-Control "public"
</FilesMatch>