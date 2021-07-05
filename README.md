# OptimoRoute integration

## Description
Integration template between Linx and the OptimoRoute API.

## Installation

### Register for an API Key

1. Login to the OptimoRoute.
2. Generate new API Key (Settings → WS API → API Enabled)
3. Copy the **API key**.

### Configure the Solution's $.Settings:

1. Open the [sample Solution](Solution.lsoz) in your Linx Designer.
1. Edit the $.Settings values:

   - `OR_APIKey`: Your API Key.

1. Save the Solution.


## Usage

### CreateOrder

Creates an order on OptimoRoute.

Makes a `POST` request to the `/create_order` endpoint and returns the details of the created order.

### GetOrders

Gets orders according to list of Order Numbers supplied.

Makes a `GET` request to the `/get_orders` endpoint and returns the details of the orders.

> An important note to keep in mind, OptimoRoute doesn’t seem to have an operation to retrieve all the orders for the day or for a span, thus, for a system using this, I’d keep a database of Order numbers to reference.


## Contributing

For questions please ask the [Linx community](https://linx/software/community) or use the [Slack channel](https://linxsoftware.slack.com/archives/C01FLBC1XNX). 

## License

[MIT](https://github.com/linx-software/template-repo/blob/main/LICENSE.txt)
