### Setup and Configuration

> [!IMPORTANT] 
> Do not install any packages as root, this may cause problems with permissions in IDE's.

> [!NOTE]
> If you are experiencing the same issue (Init basic project), please create an Issue, I may have forgotten to specify some details.

1. Install Ruby:
    - Install [rbenv](https://github.com/rbenv/rbenv)
    - Install [ruby-build](https://github.com/rbenv/ruby-build)
    - ```
      rbenv init
      rbenv install 3.3.6
      rbenv global 3.3.6
      ```
2. Install [Ruby on Rails](https://github.com/rails/rails)

3. Create a new project
> In the Ruby settings `File | Settings | Languages & Frameworks | Ruby SDK and Gems`, choose the required version:

<p align="center">
  <img src="https://github.com/user-attachments/assets/271e48f5-2825-4be2-b307-cf9e95f4d35b" />
</p>

4. Create database & install eslint(optionaly):
>  ```
>  rails db:create
>  npm install @hotwired/turbo-rails @hotwired/stimulus
>  npm install --save-dev esbuild
>  ```
