## Description

This project implements a database management system for a library using MySQL. It allows for the management of books, authors, genres, library members, and the tracking of book loans.

## How to Run/Setup the Project (or import SQL)

1.  Ensure you have MySQL installed on your system.
2.  You can import the SQL schema into your MySQL database using the following command in your terminal or MySQL client:

    ```bash
    mysql -u your_username -p < library_management_system.sql
    ```

    Replace `your_username` with your MySQL username. You will be prompted for your password.

## ERD (Entity Relationship Diagram)

Authors {author_id INT PKfirst_name VARCHAR(50)last_name VARCHAR(50)}Genres {genre_id INT PKgenre_name VARCHAR(50) U}Books {book_id INT PKtitle VARCHAR(255)isbn VARCHAR(20) Upublication_year SMALLINTauthor_id INT FK - Authors.author_idgenre_id INT FK - Genres.genre_idquantity INTavailable_quantity INT}Members {member_id INT PKfirst_name VARCHAR(50)last_name VARCHAR(50)membership_date DATEemail VARCHAR(100) Uphone_number VARCHAR(20) U}Loans {loan_id INT PKbook_id INT FK - Books.book_idmember_id INT FK - Members.member_idloan_date DATEreturn_date DATEdue_date DATE}Key:PK - Primary KeyFK - Foreign KeyU  - Unique
*(You can replace the above textual representation with a link to an image of your ERD if you have created one.  For example: `![ERD](erd.png)` if you have a file named "erd.png" in the same directory, or `[ERD Image](https://your-image-url.com/erd.png)` if it's hosted online.)*
