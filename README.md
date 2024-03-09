Event-driven Ecommerce Architecture
=========================================

## I am attempting an unsupervised approach to building an event-driven Ecommerce platform. I intend to document my journey as I progress


## Order Management System

This project aims to build an Order Management System consisting of various components including frontend, backend, event-driven architecture, and database management.

## Components

### Frontend (React using NextJs)

The frontend component serves as the user interface for creating orders. It facilitates product selection, quantity input, and other relevant actions for order creation.

### Backend (Node.js usting NestJS and typescript)

The backend component consists of several sub-components:

1. **REST API**: Responsible for handling order creation and providing endpoints for retrieving order status. There's also a potential for exploring GraphQL in the future to enhance querying capabilities.

2. **Event Producer**: Publishes order creation events to the message broker, enabling communication between various system components.

### Event Broker (Kafka or RabbitMQ)

The Event Broker serves as a middleware, receiving order creation events from the Event Producer and distributing them to subscribed components for further processing.

### Worker (Node.js)

The Worker component carries out the following tasks:

- Subscribes to the message broker to receive order creation events.
- Processes these events, which may involve tasks such as inventory management, payment processing simulation, and sending order confirmation emails.

### Database (PostgreSQL with Prisma as ORM)

The Database component stores crucial information related to orders, inventory, and user details. PostgreSQL is chosen as the database management system for its robustness and reliability.

## Technologies

- **Frontend**: React
- **Backend**: Node.js
- **Event Broker**: Kafka or RabbitMQ (to be decided)
- **Database**: PostgreSQL

## Getting Started

To get started with the Order Management System:

1. Clone this repository as well as the frontend app here https://github.com/datrine.
2. Set up the frontend and backend according to their respective README files.
3. Configure the Event Broker and Worker components.
4. Set up the PostgreSQL database and ensure it's running properly.
5. Connect all components together as per the system architecture.
6. Start the system and begin managing orders efficiently.

## Future Improvements

- Implement GraphQL for enhanced querying capabilities in the backend.
- Explore scalability options for the Event Broker to handle increased event traffic.
- Enhance Worker functionality to include more sophisticated order processing tasks.
- Improve frontend user experience and interface design.

## Contributors

- Alabi Temitope David

Feel free to contribute to this project by forking and submitting pull requests.

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).
