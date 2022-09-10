
# Web Packers - Parcel

## 1. Steps to init a Parcel project

  ```bash
    git init
    npm init -y
    npm install -D parcel
  ```

## 2. Create the following files

  * src/index.js
  * src/index.html
  * src/styles.css

## 3. In package.json file

  * Update `main` property to:
  ```bash
    "source": "src/index.html",
  ```

  * Add scripts
  ```bash
    "start": "parcel serve --port 8080 src/index.html",
    "build": "parcel build src/index.html --public-url ./"
  ```

## 4. posthtml configuration

  * Installation
  ```bash
    npm install posthtml-include -D
  ```

  * Create .posthtmlrc file
  ```json
    {
      "plugins": {
        "posthtml-include": {
          "root": "./src"
        }
      }
    }
  ```

## 5. Deploy on Github Pages

  * Installation
  ```bash
    npm install gh-pages -D
  ```

  * Script on package.json file
  ```bash
    "deploy": "gh-page -d dist"
  ```
