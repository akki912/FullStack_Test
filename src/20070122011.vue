<template>
    <div>
      <h1>List of Books</h1>
      <table>
        <thead>
          <tr>
            <th>Id</th>
            <th>Book Name</th>
            <th>Author Name</th>
            <th>Number of Pages</th>
            <th>Status</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(book, index) in books" :key="index">
            <td>{{ book.id }}</td>
            <td>{{ book.bookName }}</td>
            <td>{{ book.authorName }}</td>
            <td>{{ book.numPages }}</td>
            <td>{{ book.status }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        books: [
          {
            id: 1,
            bookName: 'The Catcher in the Rye',
            authorName: 'J.D. Salinger',
            numPages: 224,
            status: 'available',
          },
          {
            id: 2,
            bookName: 'To Kill a Mockingbird',
            authorName: 'Harper Lee',
            numPages: 281,
            status: 'issued',
          },
          {
            id: 3,
            bookName: '1984',
            authorName: 'George Orwell',
            numPages: 328,
            status: 'available',
          },
          {
            id: 4,
            bookName: 'Animal Farm',
            authorName: 'George Orwell',
            numPages: 112,
            status: 'available',
          },
          {
            id: 5,
            bookName: 'The Great Gatsby',
            authorName: 'F. Scott Fitzgerald',
            numPages: 180,
            status: 'issued',
          },
          {
            id: 6,
            bookName: 'The Hobbit',
            authorName: 'J.R.R. Tolkien',
            numPages: 310,
            status: 'issued',
          },
          {
            id: 7,
            bookName: 'The Lord of the Rings',
            authorName: 'J.R.R. Tolkien',
            numPages: 1178,
            status: 'available',
          },
          {
            id: 8,
            bookName: 'Pride and Prejudice',
            authorName: 'Jane Austen',
            numPages: 279,
            status: 'available',
          },
          {
            id: 9,
            bookName: 'Jane Eyre',
            authorName: 'Charlotte Bronte',
            numPages: 507,
            status: 'issued',
          },
          {
            id: 10,
            bookName: 'Wuthering Heights',
            authorName: 'Emily Bronte',
            numPages: 288,
            status: 'available',
          },
        ],
      };
    },
  };
  </script>
  

