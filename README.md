# JSON Data Hosting on Render.com

This repository demonstrates how to host JSON data on [Render.com](https://render.com/) and use it as an API for different objects. This can be particularly useful for serving static data that can be consumed by various applications.

## Table of Contents

- [JSON Data Hosting on Render.com](#json-data-hosting-on-rendercom)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Features](#features)
  - [Setup](#setup)
    - [Prerequisites](#prerequisites)
    - [Deploying to Render.com](#deploying-to-rendercom)
  - [Usage](#usage)
    - [Accessing the API](#accessing-the-api)
    - [Example Requests](#example-requests)
      - [Fetch Data](#fetch-data)

## Introduction

This project provides a simple way to host JSON data on Render.com. The hosted data can be accessed via HTTP requests and used in various applications such as websites, mobile apps, and other APIs.

## Features

- Host JSON data on Render.com
- Access JSON data via a public API endpoint
- Easy deployment and management

## Setup

### Prerequisites

- A [Render.com](https://render.com/) account
- Node.js and npm installed locally

### Deploying to Render.com

1. **Fork or Clone this repository:**

    ```sh
    git clone https://github.com/your-username/json-data-hosting.git
    cd json-data-hosting
    ```

2. **Navigate to the Render.com dashboard and create a new Web Service:**

    - Go to [Render.com](https://render.com/) and log in.
    - Click on "New" and select "Web Service".
    - Connect your GitHub repository and select the `json-data-hosting` repo.

3. **Configure the Web Service:**

    - **Name:** Choose a name for your service.
    - **Region:** Select your preferred region.
    - **Branch:** Select the branch you want to deploy (default is `main`).
    - **Build Command:** Leave it empty if there is no specific build command.
    - **Start Command:** Set to `yarn start` or `npm start` depending on your package manager.
    - **Environment:** Set to `Static Site`.

4. **Deploy the Service:**

    - Click on "Create Web Service".
    - Render.com will automatically deploy your service.

5. **Access Your API:**

    - Once deployed, you will get a public URL where your JSON data is hosted.
    - You can access the JSON data via the URL, e.g., `https://your-service-name.onrender.com/data.json`.

## Usage

### Accessing the API

To access the JSON data, simply send an HTTP GET request to the URL provided by Render.com.

### Example Requests

#### Fetch Data

```sh
curl https://your-service-name.onrender.com/data.json
