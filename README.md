class CRUD:
    def __init__(self, username, password, database_name, collection_name):
        self.username = username
        self.password = password
        self.database_name = database_name
        self.collection_name = collection_name

    def create(self, data):
        # Placeholder for create method
        print(f"Creating document in {self.database_name}.{self.collection_name}:", data)
        return "Simulated create success"

    def read(self, query):
        # Placeholder for read method
        print(f"Reading documents from {self.database_name}.{self.collection_name} with query:", query)
        return "Simulated read result"

username = "aacuser"
password = "your_password"
database_name = "AAC"
collection_name = "animals"

crud_instance = CRUD(username, password, database_name, collection_name)

data_to_insert = {"name": "Fluffy", "type": "Cat", "age": 3}
crud_instance.create(data_to_insert)

read_query = {"type": "Cat"}
crud_instance.read(read_query)
