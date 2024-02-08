## Tag Creator

This project provides functionality to create barcode tags for products.

### Description

The Tag Creator project allows users to generate barcode images for products. It includes endpoints to create tags and handles the generation of barcode images using the Code128 format.

### Features

- **Create Tag**: Endpoint `/create_tag` to create a barcode tag for a product.
- **Barcode Generation**: Barcode images are generated using the Code128 format.

### Installation

1. Clone the repository:

   ```bash
   git clone <repository_url>
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Set up the environment:

   ```bash
   # Assuming you're using virtualenv
   source <virtualenv_name>/bin/activate
   ```

4. Run the application:

   ```bash
   python app.py
   ```

### Usage

1. Send a POST request to `/create_tag` with the product details in the request body.
2. The application will generate a barcode image for the product and return the path to the image.

### Endpoints

- **Create Tag**:
  - URL: `/create_tag`
  - Method: `POST`
  - Request Body: JSON with product details.
  - Response: JSON with the path to the generated barcode image.

### Sample Request

```json
{
  "product_code": "123456789"
}
```

### Sample Response

```json
{
  "data": {
    "type": "Tag Image",
    "count": 1,
    "path": "/path/to/barcode.png"
  }
}
```

### Error Handling

- **HTTP 422 Unprocessable Entity**: If there are validation errors or invalid requests, the API returns an error response with details.
- **HTTP 500 Server Error**: For unexpected errors, the API returns a generic server error response.

### Technologies Used

- Python
- Flask
- Barcode (Python library)

### Contributors

- [Thiago Nunes Miziara](https://github.com/thiagonmiziara)

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
