# Import the CRUD module
from your_crud_module import CRUD

username = "aacuser"
password = "your_password"
database_name = "AAC"
collection_name = "animals"

crud_instance = CRUD(username, password, database_name, collection_name)

data_to_insert = {"name": "Fluffy", "type": "Cat", "age": 3}
data_to_insert

read_query = {"type": "Cat"}
read_query
