# Git Ignore
创建一个新文件 `~/.gitignore` ，并将以下内容添加进去，这样全部 git 仓库将会忽略以下内容所提及的文件。
~~~
# Folder view configuration files
.DS_Store
Desktop.ini

# Thumbnail cache files
._*
Thumbs.db

# Files that might appear on external disks
.Spotlight-V100
.Trashes

# Compiled Python files
*.pyc

# Compiled C++ files
*.out

# Application specific files
venv
node_modules
.sass-cache
~~~
