# MtjreeGate


**Mtjree Gate** is a Partner with multiple payment gateways and commission agent, affiliate trading.

## Getting Started

### If You Have a Custom-Built Website and Want to Integrate

1. First, contact us [here](#) to get set up within our system.
2. After you are set up, you can start sending requests to our API.

### API Integration

When sending data, make sure the request is a `POST` request and the body contains the following fields (each on a new line):

| Field            | Type                        | Description                                    |
|------------------|-----------------------------|------------------------------------------------|
| `order_id`       | `number` or `string`        | Unique identifier for the order.               |
| `email`          | `string`                    | Customer's email address.                      |
| `shop_type`      | `string`                    | Type of shop (e.g., "wordpress", "react").       |
| `shop_url`       | `string`                    | URL of the shop.                               |
| `currency`       | `string` (3-letter format)  | Currency code (e.g., USD, EUR).                |
| `total`          | `number`                    | Total order amount.                            |
| `first_name`     | `string`                    | Customer's first name.                         |
| `last_name`      | `string`                    | Customer's last name.                          |
| `country`        | `string` (2-letter code)    | Country code (e.g., US, CA).                   |
| `city`           | `string`                    | City of the customer.                          |
| `billing_address`| `string`                    | Customer's billing address.                    |
| `postcode`       | `number`                    | Postal code of the billing address.            |
| `hookUrl`        | `string`                    | Webhook URL for order updates.                 |
| `customer_id`    | `number` or `string`        | Unique identifier for the customer.            |
| `timestamp`      | `string` (16 characters)    | A unique 16-character alphanumeric value in a 16-character format.      |
| `phone`          | `string`                    | Customer's phone number.                       |
| `fail_url`       | `string` (optional)         | URL to redirect to in case of failure.         |
| `meta_data`      | `json`                      | Additional data you want to receive in the request. |
| `logo_url`       | `string`                    | URL of the photo to be displayed on the payment page. |
| `vendor_name`    | `string`                    | Name of the vendor to be displayed on the payment page. |
| `test_mode`    | `bool`                    | Indicates whether the order is in test mode (true for test, false for live).|

- `timestamp` (A unique 16-character alphanumeric value, e.g., generate it like this:
    ```php
    $bytes = random_bytes(8);
    $timestamp = bin2hex($bytes);
    ```
- `phone`
### Required Headers

When making a request, ensure to include the following headers:

| Header            | Value                        | Description                                    |
|-------------------|------------------------------|------------------------------------------------|
| `Authorization`   | `Bearer <API_key>`           | Your API key for authorization.                |
| `Content-Type`    | `application/json`           | The content type of the request.               |

### Send Your Request To:

`https://mtjree.link/wp-json/custom/v1/proxy`

---

**Note:** Ensure that the `hookUrl` is on the same domain as `shop_url` to maintain security and data integrity.
**In case of disagreement, contact us.**

For any questions or support, please don't hesitate to contact us.
