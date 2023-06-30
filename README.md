# Docker Apps in Localhost
Tutorial for running applications (Rails and Vite) in localhost.

Video Tutorial is available [Here](https://youtu.be/w_e_TZnJ7DA)

# Ruby on Rails 7.1 Commands
```bash
rails new rails_app --main
cd rails_app
rails g scaffold post title body:text
rails db:migrate

docker build . -t rails_app
docker run -d -p 3001:3001 --network rails rails_app
```

# Vite Commands
```bash
npm create vite@latest
cd vite_app

docker build . -t vite_app
docker run -d -p 5173:5173 --network rails vite_app
```
