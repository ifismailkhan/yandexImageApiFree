# Yandex Image API Node.js Wrapper

This is a simple Node.js API wrapper for the Yandex Image API, which I have reverse-engineered. The API allows you to make image search requests and retrieve results in a structured JSON format. This wrapper simplifies making requests to the API by handling the request payload and parsing the response.

## Features

- Easy to use with a simple Node.js setup.
- Supports custom search queries.
- Parses JSON responses for easy consumption.

## Installation

1. Download the ZIP file containing the project.
2. Extract the ZIP file to your desired location.
3. Navigate to the project directory in your terminal.
4. Run `npm install` to install the necessary dependencies.

## Usage

To make a request to the Yandex Image API using this wrapper, you need to construct a payload with specific parameters. Here is an example payload you can use:

```json
{
  "tmpl_version": "releases/frontend/images/v1.1199.0#88aa8cacf6a9ec000def38d5d2bc81caa27d079e",
  "format": "json",
  "request": {
    "blocks": [
      {
        "block": "extra-content",
        "params": {},
        "version": 2
      },
      {
        "block": {
          "block": "i-react-ajax-adapter:ajax"
        },
        "params": {
          "type": "ImagesApp",
          "ajaxKey": "serpList/fetch"
        },
        "version": 2
      }
    ],
    "metadata": {
      "bundles": {
        "lb": "rd]e)D)vxy+(((ek+Nw}"
      },
      "assets": {
        "las": "justifier-height=1;justifier-setheight=1;fitimages-height=1;justifier-fitincuts=1;react-with-dom=1;580180.0=1;239.0=1;215.0=1;34f306.0=1;e11d92.0=1;135.0=1;bc4f0f.0=1;199.0=1;207.0=1;319.0=1;d13b93.0=1;59eac7.0=1;eef97d.0=1"
      }
    },
    "extraContent": {
      "names": [
        "i-react-ajax-adapter"
      ]
    }
  },
  "yu": "1268539681699969707",
  "lr": "10615",
  "p": "1",
  "rpt": "image",
  "serpListType": "horizontal",
  "serpid": "ZxKzsIlt0cB5Xc6AFzrmmQ",
  "text": "Your search text will be here",
  "uinfo": "sw-425-sh-652-ww-425-wh-652-pd-2-wp-2x3_640x960"
}
```

Replace `"Your search text will be here"` with your actual search query.

To execute a request, use the provided `search` function in the API wrapper, passing the payload as an argument:

```javascript
const searchResults = search(payload);
```

## Response

The API will return a JSON object containing the search results, which you can then process according to your needs.

## Note

This API wrapper is for educational and research purposes. Please use responsibly and in accordance with Yandex's terms of service.
