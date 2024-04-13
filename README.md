empezamos el proyecto con rails new auth

creamos el controlador de la vista controlador main y la vista se llama home
rails g controller Main home

modificamos el archivo de rutas 
con root main#home

en el archivo gemfile agregamos la gema devise
damos bundle install

rails g devise:install
este comando genera todas las configuraciones para devise

luego generamo el modelo para crear usuarios q seria user

rails g devise User

lyego hacemos la migracion

rails db:migrate


esto va en el controlador
before_action :authenticate_user!
este comando verifica si hay una sesion abierta

