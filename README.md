from pathlib import Path

path = Path("/mnt/data/README.md")
content = path.read_text(encoding="utf-8")

content = content.replace(
    "https://github.com/yashganar90",
    "https://github.com/yashterdayyyy"
)
content = content.replace(
    "https://github.com/yashganar90/trading-simulator",
    "https://github.com/yashterdayyyy/trading-simulator"
)

# The user's GitHub profile repository should match the actual username.
content = content.replace(
    "Your GitHub username appears to be **`yashganar90`**",
    "Your GitHub username is **`yashterdayyyy`**"
)

path.write_text(content, encoding="utf-8")
print("Updated GitHub links to https://github.com/yashterdayyyy")
