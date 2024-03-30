## :nerd_face: About Me

Briefly,
```python
class AboutMe:
    """Introduction of Dustin Baek."""

    def __init__(self):
        self.__company: str = "Deloitte"
        self.__position: str = "Machine Learning Engineer"
        self._workspace: dict[str, str] = {
            "company": self.__company,
            "position": self.__position,
        }
        self.__interested_positions: set[str] = {
            "Software Engineer",
            "Data Engineer",
            "Machine Learning Engineer",
            "Python Developer",
        }
        self._programming: list[str] = ["Python", "SQL", "Bash"]

    def __repr__(self):
        """Show who I am."""
        return f"Hi! I'm Dustin working as {self._workspace.get("position")}" +\
               f"at {self._workspace.get("company")}."

    @property
    def workspace(self) -> list[str, str]:
        """Get workspace details."""
        return self._workspace

    @workspace.setter
    def workspace(self, value: Iterable[bool, str, str]):
        """Update workspace details if conditions met."""
        try:
            career_growth, new_company, new_role = value
        except ValueError as e:
            raise ValueError(
                "To set workspace you need to pass in iterable of three elements."
            ) from e
        else:
            if career_growth and new_role in self.__interested_positions:
                self._workspace["company"] = new_company
                self._workspace["position"] = new_role
            elif career_growth and new_role not in self.__interested_positions:
                raise ValueError(
                    "I want to become better "
                    + " or ".join(s for s in self.__interested_positions)
                )
            else:
                raise ValueError("Sorry maybe not position suitable for me.")

    @property
    def programming(self) -> list[str]:
        """Get current programming skils."""
        return self._programming

    @programming.setter
    def programming(self, language: str):
        """Willing to learn any language!"""
        if isinstance(language, str):
            self._programming.append(language)

    @property
    def education(self) -> str:
        """No setter since it wouldn't change."""
        degree: str = "MEng Information and Computer Engineering"
        where: str = "University of Cambridge"
        when: str = "10.2018 - 06.2022"
        return " | ".join([degree, where, when])

    @property
    def location(self) -> tuple[float, float]:
        """I prefer to work in london for now."""
        return 51.493879, -0.218356
```

## :chart_with_upwards_trend: Github Stats
[![Dustin's GitHub stats](https://github-readme-stats.vercel.app/api?username=dustinbaekpersonal&show_icons=true&theme=dracula)](https://github.com/anuraghazra/github-readme-stats)

## :hammer_and_wrench: Technologies
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Pytest](https://a11ybadges.com/badge?logo=pytest)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)

![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)

![Snowflake](https://a11ybadges.com/badge?logo=snowflake)
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)

![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![GitLab CI](https://img.shields.io/badge/gitlab%20ci-%23181717.svg?style=for-the-badge&logo=gitlab&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)

![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)

![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)
![Vim](https://img.shields.io/badge/VIM-%2311AB00.svg?style=for-the-badge&logo=vim&logoColor=white)

![macOS](https://img.shields.io/badge/mac%20os-000000?style=for-the-badge&logo=macos&logoColor=F0F0F0)
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
