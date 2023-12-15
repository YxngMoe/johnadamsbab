class CRUDOperations:
    def __init__(self, username, password, database_name, collection_name):
        self.username = username
        self.password = password
        self.database_name = database_name
        self.collection_name = collection_name

    def create_document(self, data):
        print(f"Creating document in {self.database_name}.{self.collection_name}:", data)
        return "Simulated create success"

    def read_documents(self, query):
        print(f"Reading documents from {self.database_name}.{self.collection_name} with query:", query)
        return "Simulated read result"

crud_instance = CRUDOperations("dummy_user", "dummy_password", "dummy_database", "dummy_collection")

data_to_insert = {"name": "Fluffy", "type": "Cat", "age": 3}
create_result = crud_instance.create_document(data_to_insert)
print(f"Create Operation Result: {create_result}")

read_query = {"type": "Cat"}
read_result = crud_instance.read_documents(read_query)
print(f"Read Operation Result: {read_result}")
