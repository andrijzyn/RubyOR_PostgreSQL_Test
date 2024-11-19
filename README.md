### Setup and Configuration


### ⚠️ Important:
-  **Do not install packages as `root`** - this may cause permissions problems in the IDE.
-  **It is recommended to run `rails` from `~/bin`** to avoid possible conflicts.

---

### ℹ️ Notes:
-  If you encounter the same problem when initialising the base project, please create **Issue**. I may have forgotten to specify some details.
-  Separation of tasks by console:
-  🟩-**System console** (for example, a terminal outside the project).
-  🟥-**Project console** (terminal opened in the project root).
-  🟪-**Postgre console** (terminal opened by sudo -u postgres psql).

---

### 🟩 🛠 Install dependencies:

1. Make sure you have **Node.js** and **npm** installed.

2. To install dependencies, run the command:
```bash
pnpm install @hotwired/turbo-rails @hotwired/stimulus
```
 
3. Install Ruby:
Install [rbenv](https://github.com/rbenv/rbenv)
Install [ruby-build](https://github.com/rbenv/ruby-build)
```bash
rbenv init
rbenv install 3.3.6
rbenv global 3.3.6
```

4. Install [Ruby on Rails](https://github.com/rails/rails)

---

### 🟩 🔧 PostgreSQL Setup:

1. **Install PostgreSQL**:

For **Arch**:
```bash
sudo pacman -S postgresql
```
For **Debian**:
```bash
sudo apt install postgresql postgresql-contrib
```
For **macOS** using Homebrew:
```bash
brew install postgresql
```

2. Start the PostgreSQL service:

For **Debian**:
```bash
sudo systemctl enable postgresql
sudo service postgresql start
```
For **macOS** using Homebrew:
```bash
brew services start postgresql
```
    
---

### 🌱 Database Setup

To set up the PostgreSQL database for the project, follow the steps below:
1. Create the Database

- 🟥 Create a database using the command:
```bash
rails db:create
rails db:migrate
```
- 🟩 Open the postgres console:
```bash
sudo -u postgres psql
```
- 🟪 Create a new PostgreSQL user (if necessary):
It is better for {username} to use the vlast name on the system
```bash
CREATE ROLE {username} WITH LOGIN PASSWORD '{password}';
```
- 🟪 Grant permissions to connect and use the database :
```bash
GRANT CONNECT ON DATABASE {database_name} TO {username};
GRANT USAGE ON SCHEMA public TO {username};
```
- 🟪 Grant permissions to create and modify tables in the schema :
```bash
GRANT CREATE ON SCHEMA public TO {username};
GRANT ALL PRIVILEGES ON ALL TABLES IN SCHEMA public TO {username};
```
