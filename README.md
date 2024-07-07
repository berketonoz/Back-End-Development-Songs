# Song Microservice for Django Web Application

This repository contains the microservice responsible for managing song-related operations within a Django web application. It is part of the [Back-end Development Capstone](https://github.com/berketonoz/Back-end-Development-Capstone) project. This microservice includes APIs for performing CRUD operations on song data, user authentication, and other related functionalities.

## Table of Contents

- [Features](#features)
- [Architecture](#architecture)
- [Getting Started](#getting-started)
- [Installation](#installation)
- [Deployment](#deployment)
- [Usage](#usage)
- [Running Tests](#running-tests)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Features

- User authentication and authorization
- CRUD operations for songs
- RESTful APIs with Django Rest Framework
- Search functionality for songs
- Playlist management
- Admin interface for managing songs and users

## Architecture

This microservice is a part of a larger Django web application. It focuses on handling all operations related to songs, including:

- Creating, reading, updating, and deleting song records
- User authentication and authorization for accessing song data
- Managing playlists and song metadata

## Getting Started

These instructions will help you set up the microservice on your local machine for development and testing purposes.

### Prerequisites

- Python 3.x
- Django 3.x or higher
- pip (Python package installer)

### Installation

1. Clone the repository:

```bash
git clone https://github.com/berketonoz/Back-End-Development-Songs.git
cd Back-End-Development-Songs
```

2. Create a virtual environment:

```bash
python3 -m venv venv
source venv/bin/activate   # On Windows, use `venv\Scripts\activate`
```

3. Install the required packages:

```bash
pip install -r requirements.txt
```

4. Set up the database:

```bash
python manage.py migrate
```

5. Create a superuser:

```bash
python manage.py createsuperuser
```

6. Run the development server:

```bash
python manage.py runserver
```

The application will be available at `http://127.0.0.1:8000`.

## Deployment

This microservice is deployed on IBM Cloud Code Engine. Follow these steps to deploy:

1. Install the IBM Cloud CLI and Code Engine plugin:

```bash
ibmcloud plugin install code-engine
```

2. Log in to your IBM Cloud account:

```bash
ibmcloud login
```

3. Target your project and region:

```bash
ibmcloud target --cf
ibmcloud ce project select --name YOUR_PROJECT_NAME
```

4. Create and configure the Code Engine application:

```bash
ibmcloud ce app create --name song-microservice --image YOUR_DOCKER_IMAGE --cpu 1 --memory 2G --port 8080 --min-scale 1 --max-scale 3
```

5. Access your application:

After deployment, your application will be available at the URL provided by IBM Cloud Code Engine.

## Usage

- Access the admin interface at `http://YOUR_DEPLOYED_URL/admin` to manage songs and users.
- Use the API endpoints to interact with the song data programmatically.

## Running Tests

To run the tests, use the following command:

```bash
python manage.py test
```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any changes.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a pull request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

Berketonoz - [GitHub](https://github.com/berketonoz)

Feel free to contact me if you have any questions or suggestions.
