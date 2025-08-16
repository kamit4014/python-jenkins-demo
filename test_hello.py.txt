# test_hello.py
import subprocess

result = subprocess.run(
    ['python', 'hello.py'], capture_output=True, text=True
)
assert "Hello, World!" in result.stdout
print("Test Passed!")
