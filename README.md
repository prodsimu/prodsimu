```python
#!/usr/bin/env python3
# developer_profile.py

import fastapi
import docker
import pytest

from typing import Dict, List


class BackendDeveloper:

    def __init__(self) -> None:
        self.name: str = "Simu"
        self.role: str = "Backend Developer"

        self.stack: Dict[str, List[str]] = {
            "language": ["Python"],
            "framework": ["FastAPI"],
            "databases": ["PostgreSQL", "MySQL", "SQLite"],
            "tools": ["Docker", "Git", "Linux", "Pytest"]
        }

        self.currently_learning: List[str] = [
            "System Design",
            "Scalable APIs",
            "Docker best practices"
        ]

        self.contact: Dict[str, str] = {
            "email": "dev.lopes@pm.me"
        }

    def introduce(self) -> None:
        print(f"Hi, I'm {self.name} 👋")
        print(f"Role: {self.role}\n")

        print("Tech Stack:")
        for category, items in self.stack.items():
            print(f"- {category}: {', '.join(items)}")

        print("\nCurrently learning:")
        for topic in self.currently_learning:
            print(f"- {topic}")
        print(f"\nContact: {self.contact['email']}")


def main() -> None:
    me = BackendDeveloper()
    me.introduce()


if __name__ == "__main__":
    main()

```
