# Linux
Notes on Linux.

## Commands
### Search and replace using sed
    find . -type f -print | xargs grep "use Mojo::Base"
    find . -type f -print | xargs sed -i 's/use Mojo::Base \-base/use NMSWeb::Base/g'
    find . -type f -print | xargs sed -i 's/use Mojo::Base/use NMSWeb::Base/g'