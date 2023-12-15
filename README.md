from crud_module import CRUD

host = "nv-desktop-services.apporto.com"
port = 31580
username = "aacuser"
password = "SNHU1234"
db_name = "AAC"
collection_name = "animals"
crud = CRUD(host, port, username, password, db_name, collection_name)

create_data = {"name": "Sample Animal", "type": "Dog"}
create_result = crud.create(create_data)
print("Create Result:", create_result)

read_query = {"type": "Dog"}
read_result = crud.read(read_query)
print("Read Result:", read_result)

update_query = {"type": "Dog"}
update_data = {"$set": {"type": "Cat"}}
update_result = crud.update(update_query, update_data)
print("Update Result:", update_result)

delete_query = {"type": "Cat"}
delete_result = crud.delete(delete_query)
print("Delete Result:", delete_result)


output

Create Result: True
Read Result: [{'_id': ObjectId('some_object_id'), 'name': 'Sample Animal', 'type': 'Dog'}]
Update Result: 1
Delete Result: 1
