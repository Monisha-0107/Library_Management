A simple Library Management System built to manage books, authors, users, and borrowing details efficiently. This project helps librarians maintain records and perform operations like adding books, and viewing reports.



ADDBOOK
<img width="562" height="478" alt="Screenshot 2026-02-11 114305" src="https://github.com/user-attachments/assets/5bfe7fdd-51a4-4757-8796-822bbbe57dd1" />


VIEWBOOK
<img width="525" height="364" alt="image" src="https://github.com/user-attachments/assets/4e1f4a0d-cd6e-4330-a7aa-bb8a339e5d08" />


QUERY
Create table AUTHOR_TBL (
Author_code number(5) PRIMARY KEY,
Author_name varchar2(20) NOT NULL , 
Contact_no varchar2(10));
 
 DROP TABLE AUTHOR_TBL;

INSERT INTO AUTHOR_TBL (Author_code, Author_name, Contact_no)
VALUES (1, 'Robin Sharma', '8800799224');

INSERT INTO AUTHOR_TBL (Author_code, Author_name, Contact_no)
VALUES (2, 'R.K.Narayan', '9971933500');

INSERT INTO AUTHOR_TBL (Author_code, Author_name, Contact_no)
VALUES (3, 'Paulo Coelho', '1234567890');

Create table BOOK_TBL (
ISBN Varchar2(10) PRIMARY KEY, 
Book_title Varchar2(20) NOT NULL,
Book_type Char(1) CHECK(Book_type IN('T','G')),
Author_code Number(5),
CONSTRAINT fk_author FOREIGN KEY(Author_code)REFERENCES AUTHOR_TBL(Author_code),

Book_Cost Number(8,2) NOT NULL);





SELECT * FROM AUTHOR_TBL;

SELECT * FROM BOOK_TBL;
