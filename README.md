![CI](https://github.com/pujan910/IDS568-assignment1/actions/workflows/ci.yml/badge.svg)

# IDS568-assignment1

## SETUP (reproducible environment)

**Python version:** 3.11

1. Clone the repository:
	```bash
	git clone https://github.com/pujan910/IDS568-assignment1.git
	cd IDS568-assignment1

2. Create a virtual envirnment and then activate it:
	python3 -m venv .venv
	source .venv/bin/activate

3. Install dependencies:
	pip install -r requirements.txt

4. Running the tests:
	pytest -v

THE SMOKE TEST
This repo includes a simple smoke test in tests/test_imports.py that verifies the required libraries import correctly.
If the imports work and the test passes, it confirms the environmen is set up correctly

DOCUMENTATION
Reproducibility is important in machine learning because ML projects usually fail when code works on one system but
breaks somewhere else. Small differences in library versions, Python versions, or environments can completely change
results or cause the project to crash. This is one of the main reasons many ML projects never make it to production.
In this milestone, the goal was to avoid that problem from the start.

I used a Python virtual environment to keep this projectisolated from my system setup. This ensures that the project
does not depend on globally installed packages. All dependencies are pinned to exact versions in requirements.txt,
which means that anyone running this project installs the same libraries and gets the same behavior. I also added
like a smoke test to confirm that the core packages import correctly and basic operations work.

To make this reproducible beyond my local machine, I set up a GitHub Actions CI workflow. he CI pipeline automatically
creates a fresh environment, installs dependencies, and runs tests on every push. This helps catch issues early and
simulates how the project would behave in a real production setup. Overall, this setup creates a reliable and
repeatable foundation for future ML development.
