# table user
- user_id: INT UNSIGNED AUTO_INCREMENT
- username: VARCHAR(50)
- email: VARCHART(100)
- password: VARCHART(255)
- telp: VARCHART(15)
- role : ENUM('ADMIN', 'USER')

# table profile_user
- user_id: INT UNSIGNED 
- date_birth: DATE
- photo: VARCHART(255)
- first_name: VARCHART(50)
- last_name: VARCHART(50)
- gender: ENUM('MALE', 'FEMALE' )
- employee_id(nullable): VARCHART(20)
- position (nullable): VARCHART(50)
- address_id: INT UNSIGNED, FK

# table address
- address_id: INT UNSIGNED AUTO_INCREMENT
- full_name: VARCHART(100)
- telp: VARCHART(15)
- full_adress: TEXT
- detail_address: VARCHART(255)

# table product
- product_id: INT UNSIGNED AUTO_INCREMENT
- user_id: INT UNSIGNED, FK
- product_name: VARCHART(100)
- price: DECIMAL(10, 2)
- quantity: INT UNSIGNED
- description: TEXT
- rate_product: DECIMAL(3, 2)
- image_product: VARCHART(255)

# Tabel order:
- order_id: INT UNSIGNED AUTO_INCREMENT
- user_id: INT UNSIGNED, FK
- total_price: DECIMAL(10, 2)
- date_sales: DATETIME
- invoice_number: VARCHART(50)
- payment_id: INT UNSIGNED, FK

# Tabel order_details:
- order_detail_id: INT UNSIGNED AUTO_INCREMENT
- order_id: INT UNSIGNED, FK
- product_id: INST UNSIGNED, FK
- quantity: INT UNSIGNED
- total_price: DECIMAL (10,2)


# table payment
- payment_id: INT UNSIGNED AUTO_INCREMENT
- payment_method: VARCHART(50)
- status_payment: ENUM('PENDING', 'CLOMPLETED', 'FAILED')
- payment_date: DATETIME

# table comment
- comment_id: INT UNSIGNED AUTO_INCREMENT
- user_id: INT UNSIGNED, FK
- product_id: INT UNSIGNED, FK
- comment: TEXT

# table massage
- massage_id: INT UNSIGNED AUTO_INCREMENT
- user_id: INT UNSIGNED, FK
- recipient_id: INT UNSIGNED, FK
- massage_content: TEXT
- data_sent: DATETIME




