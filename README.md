# iclass-api-py

Python API client library for TronClass / iClass learning management system.

## Features

- **Authentication**: SSO login handling via `Authenticator`
- **Course Activities**: Read, mark completed, create, publish, and delete activities
- **Exams / Quizzes**: Fetch exams, retrieve questions, save drafts, submit exam papers, create & delete classroom exams
- **Courses**: Retrieve course information, syllabus management, module deletion, bulletins, todos, and invitation codes
- **Files**: Upload, download, and delete attachments
- **Forum / Discussions**: Category topics retrieval with filtering and sorting, replying, and liking topics
- **Roll Call**: Roll call / attendance querying and responses

## Installation

### As Git Submodule

```bash
git submodule add https://github.com/GGQQmax/iclass-api-py.git api
```

### Via Pip

```bash
pip install -r requirements.txt
```

## Quick Start

```python
import asyncio
from api.auth_module import Authenticator
from api.iclass_api import TronClassAPI

async def main():
    auth = Authenticator()
    auth.perform_auth()

    api = TronClassAPI(auth.session)
    todos = await api.get_todos()
    print("Todos:", todos)

if __name__ == "__main__":
    asyncio.run(main())
```

## License

THE BEERWARE LICENSE (Revision 42)
