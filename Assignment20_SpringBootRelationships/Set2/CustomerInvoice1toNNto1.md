# Customer and Invoice One-to-Many Many-to-One Mapping

## Overview:
Create a Spring Boot application with two entities: "Customer" and "Invoice". A customer can have multiple invoices. Implement a many-to-one bidirectional mapping between these entities using Spring JPA.

## Functional Requirements:
Create folders named controller, model, repository, and service inside the directory **customerinvoice1tonnto1/src/main/java/com/giftabled/customerinvoice1tonnto1**. 

1. Controller:
- Create classes named CustomerController and InvoiceController.
  
2. Model:
- Create a class named Customer with the following attributes:
  - id: Long (auto-generated, primary key)
  - name: String (name of the customer)
  - email: String (email address of the customer)
  - invoices: List<Invoice> (OneToMany relationship with Invoice, mapped by the customer field, @Jsonignore annotation to avoid circular references during serialization)

- Create another class named Invoice with the following attributes:
  - id: Long (auto-generated, primary key)
  - invoiceNumber: String (invoice number assigned to the invoice)
  - amount: Double (the total amount of the invoice)
  - customer: Customer (ManyToOne relationship with Customer, @JoinColumn)

Implement getters, setters, and constructors for the Customer and Invoice entities.

3. Repository.
- Create interfaces named CustomerRepository and InvoiceRepository.

4. Service:
- Create class named CustomerService and InvoiceService.

## Project Structure
Refer the below image structure:

```text
└── src
    └── main
        ├── java
        │   └── com
        │       └── giftabled
        │           └── customerinvoice1tonnto1
        │               ├── controller
        │               │   ├── CustomerController.java
        │               │   └── InvoiceController.java
        │               │
        │               ├── model
        │               │   ├── Customer.java
        │               │   └── Invoice.java
        │               │
        │               ├── repository
        │               │   ├── CustomerRepository.java
        │               │   └── InvoiceRepository.java
        │               │
        │               ├── service
        │               │   ├── CustomerService.java
        │               │   └── InvoiceService.java
        │               │
        │               └── SpringappApplication.java
        │
        └── resources
            └── application.properties
```

## API Endpoints
- POST-/api/customers - Returns response status 201 with Customer object on successful creation, or 400 on failure.
- POST-/api/invoices/{customerid}/customer - Returns response status 201 with Invoice object upon successfully mapping the invoice to the customer, or 400 on failure.
- GET-/apl/customers - Returns response status 200 with a List<Customer> object on successful retrieval, or 404 on failure.
- GET-/api/invoices/{invoiceld} - Returns response status 200 with an Invoice object, including the associated customer information, upon successful retrieval, or 404 on failure.
- DELETE-/api/invoices/{invoiceld} - Returns response status 200 with the message "Invoice with number {invoiceNumber} deleted successfully." on successful deletion, or 404 "Invoice not found with ID: {invoiceld}" on failure.
