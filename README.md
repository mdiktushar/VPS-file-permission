 # Change Ownership

 ```
 sudo chown -R www-data:www-data .
 ```
<ul>
  <li>Changes the owner and group of all files and directories in the current directory (.) to www-data.</li>
  <li>-R means it applies recursively to all subdirectories and files.</li>
</ul>

 # Add your ubuntu to group
 ```
sudo usermod -a -G www-data <username>
```
<ul>
  <li>Adds the ubuntu user to the www-data group.</li>
  <li>-a appends the user to the group without removing them from existing groups.</li>
</ul>

 # Set file(s) permission
```
 sudo find . -type f -exec chmod 644 {} \;
```
<ul>
  <li>Finds all files (-type f) in the current directory (.) and sets their permissions to 644 (read/write for owner, read-only for group and others).</li>
</ul>

 # Set folder(s) permission
```
 sudo find . -type d -exec chmod 755 {} \;
```
<ul>
  <li>Finds all directories (-type d) in the current directory and sets their permissions to 755 (read/write/execute for owner, read/execute for group and others).</li>
</ul>

 # Set cache directory permission
```
 sudo chgrp -R www-data storage bootstrap/cache
```
<ul>
  <li>Changes the group of the storage and bootstrap/cache directories (and their contents) to www-data.</li>
  <li>-R applies the change recursively.</li>
</ul>

```
 sudo chmod -R ug+rwx storage bootstrap/cache
```
<ul>
  <li>Grants read (r), write (w), and execute (x) permissions to the owner (u) and group (g) for the storage and bootstrap/cache directories (and their contents).</li>
  <li>-R applies the change recursively.</li>
</ul>
