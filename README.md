from mongodb_crud import MongoDBCrud

# MongoDB connection parameters
username = "your_username"
password = "your_password"
host = "localhost"
port = 27017
database = "your_database"


mongo_crud = MongoDBCrud(username, password, host, port, database)


collection = "your_collection"

document = {"name": "John", "age": 30}
create_result = mongo_crud.create_document(collection, document)
print("Create Result:", create_result)


query = {"name": "John"}
read_result = mongo_crud.read_documents(collection, query)
print("Read Result:", read_result)


query = {"name": "John"}
update_data = {"age": 31}
update_result = mongo_crud.update_documents(collection, query, update_data)
print("Update Result:", update_result)


query = {"name": "John"}
delete_result = mongo_crud.delete_documents(collection, query)
print("Delete Result:", delete_result)
