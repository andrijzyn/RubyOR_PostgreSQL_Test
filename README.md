### Setup and Configuration for Debian-based distros

> [!IMPORTANT] 
> Do not install any packages as root, this may cause problems when working from the IDE.

> [!NOTE]
> If you are experiencing the same issue (Init basic project), please create an Issue, I may have forgotten to specify some details.

1. Install [nvm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm/)
2. Install the required system packages:
>  ```
>  sudo apt update && sudo apt install git rbenv autoconf patch build-essential rustc libssl-dev libyaml-dev libreadline6-dev zlib1g-dev libgmp-dev libncurses5-dev libffi-dev libgdbm6 libgdbm-dev libdb-dev uuid-dev postgresql-common
>  ```
>  _Note: This command installs essential packages needed for Ruby and Rails development._

3. Using rbenv to install Ruby:
>  ```
>  git clone https://github.com/rbenv/ruby-build.git ~/.rbenv/plugins/ruby-build
>  echo 'eval "$(rbenv init -)"' >> ~/.bashrc
>  source ~/.bashrc
>  rbenv install 3.3.6
>  rbenv global 3.3.6
>  ```
>  _This will set up rbenv and install Ruby version 3.3.6._

4. After initializing a new project from the IDE templates, you may encounter errors.
In the Ruby settings `File | Settings | Languages & Frameworks | Ruby SDK and Gems`, choose the required version:

<p align="center">
  <img src="https://github.com/user-attachments/assets/271e48f5-2825-4be2-b307-cf9e95f4d35b" />
</p>

6. Run the following commands in the terminal with the project open:
>  ```
>  rails db:create
>  npm install --save-dev esbuild
>  npm install @hotwired/turbo-rails @hotwired/stimulus
>  ```
>  _These commands will set up your database and install the necessary JavaScript dependencies._

### Why don't install Ruby from Distro Repos?

> The version of Ruby in the Debian repositories is currently 3.1, while the latest version is 3.3.6. The latest version of Rails requires a newer version of Ruby.
> 
> For more information on Ruby and Rails compatibility, see:
> * [End of Life Dates for Rails](https://endoflife.date/rails)
> * [Ruby & Rails Compatibility Table](https://www.fastruby.io/blog/ruby/rails/versions/compatibility-table.html)

### Versions:
>   ##### **Ruby** 3.3.6 `(2024-11-05 revision 75015d4c1f) [x86_64-linux] by **rbenv**`.
>   ##### **Rails** 8
>   ##### **rbenv** 1.1.2
>   ##### **Debian** `GNU\Linux 6.11.7-amd64 (2024-11-09) trixie`.
