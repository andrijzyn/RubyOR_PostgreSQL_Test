## Actions template to setting up & prepare Ruby - Rails - PostgreSQL with ESBuild

### Steps
> [!IMPORTANT]
> Don't install any packages on behalf `root`, this may cause problems with work from IDE

> [!NOTE]
> If you have the same problem `(Init basic project)` please create Issues, maybe I forgot to specify the details

[Install **nvm & npm**](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm/)
  ```
  sudo apt update

  sudo apt install git rbenv autoconf patch build-essential rustc libssl-dev libyaml-dev libreadline6-dev zlib1g-dev libgmp-dev libncurses5-dev libffi-dev libgdbm6 libgdbm-dev libdb-dev uuid-dev

  sudo apt install postgresql-common
  
  git clone https://github.com/rbenv/ruby-build.git ~/.rbenv/plugins/ruby-build
  
  echo 'eval "$(rbenv init -)"' >> ~/.bashrc
  
  source ~/.bashrc
  
  rbenv install 3.3.6
  
  rbenv global 3.3.6
  ```

After init new project from Templates IDE you possibly will get Errors.
Go to **0.0.0.0:3000**, click `Create database` write this commant into your terminal with open project dir `bin/rails db:migrate`, `npm install --save-dev esbuild`, `npm install @hotwired/turbo-rails @hotwired/stimulus` & you beautiful 🧑‍🦽

---

### Why don't install Ruby from distro repos?

> Too old, at the moment writing latest version Ruby in [Debian repositories](https://packages.debian.org/sid/ruby) = 3.1, the latestest = 3.3.6.
> The latest version of Rails requires a newer version of Ruby

<sub>https://endoflife.date/rails<sub/>

![image](https://github.com/user-attachments/assets/8173b762-383d-4ebd-9c40-dd73c84e8aaa) 

<sub>https://www.fastruby.io/blog/ruby/rails/versions/compatibility-table.html<sub/>

![image](https://github.com/user-attachments/assets/8ee4a2c5-642c-4416-a65e-a537692ad570)
___
> Versions:
>   ##### **Ruby** 3.3.6 `(2024-11-05 revision 75015d4c1f) [x86_64-linux] by **rbenv**`.
>   ##### **Rails** 8
>   ##### **rbenv** 1.1.2
>   ##### **Debian** `GNU\Linux 6.11.7-amd64 (2024-11-09) trixie`.
