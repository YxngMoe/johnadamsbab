from crud_operations import CRUDOperations

username = "aacuser"
password = "your_password"
database_name = "AAC"
collection_name = "animals"

crud_instance = CRUDOperations(username, password, database_name, collection_name)

data_to_insert = {"name": "Fluffy", "type": "Cat", "age": 3}
create_result = crud_instance.create_document(data_to_insert)
print(f"Create Operation Result: {create_result}")

read_query = {"type": "Cat"}
read_result = crud_instance.read_documents(read_query)
print(f"Read Operation Result: {read_result}")
