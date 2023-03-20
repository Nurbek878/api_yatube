
# CRUD for Yatube

The project implements an API for all Yatube project models.


## Tech Stack

Python 3.9\
Django 3.2\
Djangorestframework 3.14



## Run Locally

Clone the project

```bash
  git clone https://github.com/Nurbek878/api_yatube
```

Go to the project directory

```bash
  cd api_yatube
```
Install and activate the virtual environment
```bash
  python3 -m venv venv
```
```bash
  source venv/bin/activate
```
Install dependencies from the file requirements.txt

```bash
  pip install -r requirements.txt
```
Make migrations
```bash
  python manage.py migrate
```
Start the server

```bash
  python manage.py runserver
```


## API Reference

#### Pass the username and password and get the token

```http
  POST  api/v1/api-token-auth/
```
Execute all requests with parameters
| Key             | Value    | 
| :--------       | :------- | 
| `Authorization` | `Token <your token>` |

#### Get a list of all posts or create a new post

```http
  GET,POST                   api/v1/posts/
```
#### Receive, edit or delete a post by id

```http
  GET, PUT, PATCH, DELETE    api/v1/posts/{post_id}/
```
#### Get a list of all groups

```http
  GET                        api/v1/groups/
```
#### Get information about a group by id

```http
  GET                        api/v1/groups/{group_id}/
```
#### Get a list of all post comments with id=post_id or create a new one by specifying the id of the post we want to comment on

```http
  GET,POST                    api/v1/posts/{post_id}/comments/
```
#### Receive, edit or delete a comment by the id of a post with id=post_id
```http
  GET, PUT, PATCH, DELETE     api/v1/posts/{post_id}/comments/{comment_id}/
```

## Running Tests

To run tests, run the following command

```bash
  pytest
```


## Authors

- [@nurbek878](https://github.com/Nurbek878)

