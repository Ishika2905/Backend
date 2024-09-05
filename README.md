Microsoft Windows [Version 10.0.22631.4112]
(c) Microsoft Corporation. All rights reserved.

C:\Users\Admin>--version
'--version' is not recognized as an internal or external command,
operable program or batch file.

C:\Users\Admin>mongosh --version
2.3.0

C:\Users\Admin>mongosh
Current Mongosh Log ID: 66d9a5aa512dde14c62710bb
Connecting to:          mongodb://127.0.0.1:27017/?directConnection=true&serverSelectionTimeoutMS=2000&appName=mongosh+2.3.0
Using MongoDB:          7.0.14
Using Mongosh:          2.3.0

For mongosh info see: https://www.mongodb.com/docs/mongodb-shell/

------
   The server generated these startup warnings when booting
   2024-08-30T18:35:35.962+05:30: Access control is not enabled for the database. Read and write access to data and configuration is unrestricted
------

test> show dbs
Chitkara    8.00 KiB
admin      40.00 KiB
config    108.00 KiB
local      72.00 KiB
test> use Chitkara
switched to db Chitkara
Chitkara>  db.createCollections("students")
TypeError: db.createCollections is not a function
Chitkara>  db.createCollections("students")
TypeError: db.createCollections is not a function
Chitkara> db.createCollection("students")
{ ok: 1 }
Chitkara>  db.createCollection("user")
{ ok: 1 }
Chitkara> db.user.insertOne({name:"Ishika Bedi",age:19,class:"G9"})
{
  acknowledged: true,
  insertedId: ObjectId('66d9a638512dde14c62710bc')
}
Chitkara> db.user.insertMany({
... db.createCollection("student")
Uncaught:
SyntaxError: Unexpected token, expected "," (2:2)

  1 | db.user.insertMany({
> 2 | db.createCollection("student")
    |   ^
  3 |

Chitkara> db.createCollection("student")
{ ok: 1 }
Chitkara>  db.student.insertMany([{ name: "Jack", age: 20, marksChitkara>  db.student.insertMany([{ name: "Jack", age: 20, marksChitkara>  db.student.insertMany([{ name: "Jack", age: 20, marks: 85, subject: "Mathematics" }, { name: "Bob", age: 22, marks: 78, subject: "Physics" }, { name: "Nav", age: 21, marks: 92, subject: "Chemistry" }, { name: "Illu", age: 23, marks: 88, subject: "Biology" }, { name: "Eva", age: 19, marks: 95, subject: "Computer Science" }])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('66d9a672512dde14c62710bd'),
    '1': ObjectId('66d9a672512dde14c62710be'),
    '2': ObjectId('66d9a672512dde14c62710bf'),
    '3': ObjectId('66d9a672512dde14c62710c0'),
    '4': ObjectId('66d9a672512dde14c62710c1')
  }
}
Chitkara>  db.createCollection("faculty")
{ ok: 1 }
Chitkara> db.faculty.insertMany([{name : "Simran", age : 45, ratChitkara> db.faculty.insertMany([{name : "Simran", age : 45, ratChitkara> db.faculty.insertMany([{name : "Simran", age : 45, rating :3.2,subject:"Math"},{name : "Raj", age : 55, rating :3.5,subject:"Physics"},{name : "Abc", age : 32, rating :2.5,subject:"Chemistry"},{name : "Lmno", age : 29, rating :5.2,subject:"Biology"},{name : "Arjun", age : 32, rating :4.0,subject:"Computer Science"}])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('66d9a687512dde14c62710c2'),
    '1': ObjectId('66d9a687512dde14c62710c3'),
    '2': ObjectId('66d9a687512dde14c62710c4'),
    '3': ObjectId('66d9a687512dde14c62710c5'),
    '4': ObjectId('66d9a687512dde14c62710c6')
  }
}
Chitkara> db.user.insertMany([{ name: "Jack", age: 20, marks: 85, subject: "Mathematics" }, { name: "Bob", age: 22, marks: 78, subject: "Physics" }, { name: "Nav", age: 21, marks: 92, subject: "Chemistry" }, { name: "Illu", age: 23, marks: 88, subject: "Biology" }, { name: "Eva", age: 19, marks: 95, subject: "Computer Science" }])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('66d9a69c512dde14c62710c7'),
    '1': ObjectId('66d9a69c512dde14c62710c8'),
    '2': ObjectId('66d9a69c512dde14c62710c9'),
    '3': ObjectId('66d9a69c512dde14c62710ca'),
    '4': ObjectId('66d9a69c512dde14c62710cb')
  }
Chitkara>
