##Add books
Endpoint: POST /books
Url: http://localhost:9000/books
Method: POST
Body on raw json: {
    "name": "Example Books",
    "year": 2024,
    "author": "John Doe",
    "summary": "This is an example books",
    "publisher": "Publisher Awtogarr",
    "pageCount": 100,
    "readPage": 10,
    "reading": true
}


###Get All Books
Endpoint: GET /books
BaseUrl: http://localhost:9000/books.
Url: http://localhost:9000/books
Method: GET
Expected:
{
    "status": "success",
    "message": "Buku berhasil ditambahkan",
    "data": {
        "bookId": "unique-book-id"
    }
}


###Showing Books Detail
Endpoint: GET /books/{bookId}
Url: http://localhost:9000/books/Books id here
Method: GET
Excpected:
{
    "status": "success",
    "data": {
        "book": {
            "id": "unique-book-id",
            "name": "Buku A",
            "year": 2021,
            "author": "John Doe",
            "summary": "Ini adalah buku A",
            "publisher": "Publisher A",
            "pageCount": 100,
            "readPage": 10,
            "finished": false,
            "reading": true,
            "insertedAt": "timestamp",
            "updatedAt": "timestamp"
        }
    }
}


###Change books Value
Endpoint: PUT /books/{bookId}
Methode: Put
Url: http://localhost:9000/books/{bookId}
Example of value inserted:
{
    "name": "Book Revision",
    "year": 2023,
    "author": "John Doe",
    "summary": "This is an example of revision",
    "publisher": "Publisher Companny",
    "pageCount": 100,
    "readPage": 50,
    "reading": false
}
Expected:
{
    "status": "success",
    "message": "Buku berhasil diperbarui"
}


### Erase Books
Endpoint: DELETE /books/{bookId}
Methode: DELETE
Url: http://localhost:9000/books/{bookId}
Expected Response
{
    "status": "success",
    "message": "Buku berhasil dihapus"
}