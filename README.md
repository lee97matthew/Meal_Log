# README
How to Begin a MVC Ruby on Rails project

# Creating a Model
- rails g model
- rails g scaffold ClassName attr_1:datatype attr_2:datatype
  - eg rails g scaffold Entry meal_type:string calories:integer proteins:integer carbs:integer fats:integer
- created_at & updated_at column is created automatically+
  - after creating the scaffold, there is a migration file in db/migrate which needs to be dealt with
    - using rails db:migrate will create the table

# Finding Routes on the Rails server
- launch the app with rails s
  - go to http://localhost:3000/rails/info/routes

# Installing Dependencies
- Use "bundle add name" or add to the "Gemfile" like a package json
- just call "bundle" to do like a "npm install"

# Initializing Routes
- Inside of the config/routes.rb
  - root to: "entries#index" 
  - will route to the entries controller's index action
    - app/controllers/entries_controller.rb

# Activating Bulma CSS Framework
- Add [responsive viewport meta tag](https://bulma.io/documentation/overview/start/)
- and stylesheet from the starter template
  - to app/views/layouts/application.html.erb

# Partial Templates
- name file starting with _ like "_header.html.erb"
  - then use <%= render "shared/header" %> to render it out in html

# Linking
- <%= link_to "Create a New Entry", new_entry_path, class: "button is-success" %>
  - link_to "Words to show", rails path, class: "classname"

# Initializer
- Added this time_format.rb in config/initializers
  - provides a new function upon app startup

# Book keeping of params
- use <%= params %> to show the params of that page, such as what controller, view and ID are active