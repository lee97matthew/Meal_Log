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
- Use bundle add name 
- just call bundle to do like a "npm install"