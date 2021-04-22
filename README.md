# OptimoRoute integration

## Overview

The provided sample includes:

---

### Additional resources

- [OptimoRoute - Linx integration guide](https://community.linx.software/community/t/optimoroute-api-example/521)
- [OptimoRoute API reference docs](https://optimoroute.com/api/#introduction)

---

## Dependencies

### Pre-requisites

- Linx Designer
- OptimoRoute account ([sign up here](https://optimoroute.com/))

### Linx Designer

This solution was developed in the Linx Designer `v5.20.2.0`

---

## Setting up the sample

Register for an API Key

1. Login to the OptimoRoute.
2. Generate new API Key (Settings → WS API → API Enabled)
3. Copy the **API key**.

Configure the Solution's $.Settings:

1. Open the [sample Solution](Solution.lsoz) in your Linx Designer.
1. Edit the $.Settings values:

   - `OR_APIKey`: Your API Key.

1. Save the Solution.

---

## Using the sample

### Authentication

In order to authenticate the request, the API Key is included the `key` query parameter.

## Template HTTP requests

The following custom functions wrap the different types of HTTP calls into their own re-usable functions which can be thought of as 'custom MS Graph connectors'.

---

### CreateOrder

Creates an order on OptimoRoute.

Makes a `POST` request to the `/create_order` endpoint and returns the details of the created order.

### GetOrders

Gets orders according to list of Order Numbers supplied.

Makes a `GET` request to the `/get_orders` endpoint and returns the details of the orders.

> An important note to keep in mind, OptimoRoute doesn’t seem to have an operation to retrieve all the orders for the day or for a span, thus, for a system using this, I’d keep a database of Order numbers to reference.
