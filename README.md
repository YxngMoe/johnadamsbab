# Import the CRUD module
from your_crud_module import CRUD

username = "aacuser"
password = "your_password"
database_name = "AAC"
collection_name = "animals"

crud_instance = CRUD(username, password, database_name, collection_name)

data_to_insert = {"name": "Fluffy", "type": "Cat", "age": 3}
# You can display the data_to_insert to show what you would insert
data_to_insert

read_query = {"type": "Cat"}
# You can display the read_query to show what you would query
read_query
