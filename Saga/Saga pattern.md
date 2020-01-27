# SAGA pattern ?

One of the most well-known patterns for distributed transactions is called Saga. The first paper about it was published back in 1987 and has it been a popular solution since then.

A saga is a sequence of local transactions where each transaction updates data within a single service. The first transaction is initiated by an external request corresponding to the system operation, and then each subsequent step is triggered by the completion of the previous one.

A Saga is a long-lived transaction that can be written as a sequence of transactions that can be interleaved.

# example (e-commerce)
Order Service saves a new order, set the state as pending and publish an event called ORDER_CREATED_EVENT.
The Payment Service listens to ORDER_CREATED_EVENT, charge the client and publish the event BILLED_ORDER_EVENT.
The Stock Service listens to BILLED_ORDER_EVENT, update the stock, prepare the products bought in the order and publish ORDER_PREPARED_EVENT.
Delivery Service listens to ORDER_PREPARED_EVENT and then pick up and deliver the product. At the end, it publishes an ORDER_DELIVERED_EVENT
 Finally, Order Service listens to ORDER_DELIVERED_EVENT and set the state of the order as concluded.
In the case above, if the state of the order needs to be tracked, Order Service could simply listen to all events and update its state.

# Why redux-saga instead of redux-thunk
Well, straight from the docs:

<strong>“Contrary to redux thunk, you don’t end up in callback hell, you can test your asynchronous flows easily and your actions stay pure.”</strong>




