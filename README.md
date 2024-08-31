### AboutProject
![Hello Everyone](
https://jrenc.azurewebsites.net/api/signature?code=zHZRCCItO-yB8t7d2KyitELFDwADnXIotkeeIQL3juyNAzFucnyrWA%3D%3D&name=Hello%20Everyone&animate=true&speed=1&color=%230000ff)
![IAMJrenc](
https://jrenc.azurewebsites.net/api/signature?code=zHZRCCItO-yB8t7d2KyitELFDwADnXIotkeeIQL3juyNAzFucnyrWA%3D%3D&name=I%20am%20Jrenc&animate=true&speed=1&color=%230000ff)

---

# Digital Signature API

This project is a simple Node.js API that generates SVG digital signatures based on provided text input. The signatures can be customized with various options, including animation, speed, and color.

## Features

- **SVG Generation:** Creates SVG images of text with customizable stroke color.
- **Animation:** Supports animated drawing of SVG paths.
- **Caching:** Uses in-memory caching to speed up repeated requests with the same parameters.
- **Customizable:** Allows customization of stroke color, animation speed, and whether the signature is animated.

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/jrenc2002/GenLineAnimation-Server.git
   cd GenLineAnimation-Server
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

## Usage

1. **Start the server:**
   ```bash
   npm start
   ```
   The server will start on `http://localhost:3000`.

2. **Make API requests:**
   The API provides an endpoint to generate digital signatures. You can access it with the following parameters:

   - `name`: The text to be converted into a signature (default: "Signature").
   - `animate`: Whether to animate the drawing of the signature (default: false).
   - `speed`: The speed of the animation (default: 1).
   - `color`: The color of the stroke (default: "#000000").

   Example request:
   ```bash
   curl "http://localhost:3000/signature?name=JohnDoe&animate=true&speed=1&color=%230000ff"
   ```

3. **Example API Usage:**
   You can test the deployed API using this URL:
   ```
   https://jrenc.azurewebsites.net/api/signature?code=zHZRCCItO-yB8t7d2KyitELFDwADnXIotkeeIQL3juyNAzFucnyrWA%3D%3D&name=Hello%20Everyone&animate=true&speed=1&color=%230000ff
   ```

## API Endpoints

### `GET /signature`
Generates an SVG image of a digital signature.

#### Query Parameters:

- **name** (optional): The text to be rendered as a signature.
- **animate** (optional): Whether to animate the drawing of the signature (`true` or `false`).
- **speed** (optional): The speed of the animation.
- **color** (optional): The color of the stroke (hex code format).

#### Response:
- Content-Type: `image/svg+xml`
- The SVG content of the generated signature.

## Example Requests

### Basic Request
```bash
curl "http://localhost:3000/signature?name=JohnDoe"
```

### Animated Signature
```bash
curl "http://localhost:3000/signature?name=JohnDoe&animate=true&speed=2&color=%23FF0000"
```

### Cached Request
The server caches generated SVGs for repeated requests with the same parameters, improving performance.

## Deployment

You can deploy this application to Azure Functions or any other Node.js-compatible environment. The Azure Functions setup includes:

- `function.json`: Defines the HTTP trigger for the Azure function.
- `host.json`: Configures the overall hosting environment for the Azure Functions runtime.

### Azure Function URL Example:
```
https://your-function-app.azurewebsites.net/api/signature?code=<Your_Function_Code>&name=JohnDoe
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request or raise an Issue if you find a bug or have a feature request.

