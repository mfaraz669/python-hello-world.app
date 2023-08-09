**How to Deploy Python hello-world.app using GITHUB ACTION WORKFLOW**

**Step 1: Create a New Repository**

1. Create a new repository on GitHub by clicking the "+" button and selecting "New repository."

2. Name your repository (e.g., "Python-hello-world.app").

3. Choose any other repository settings you prefer, and create the repository.

**Step 2: Create the Python Script**

1. In your new repository, click on the "Add file" button and choose "Create new file."

2. Name the file `hello.py`.

3. Add the following Python code to the `hello.py` file:

```python
print("Hello, World!")
```

4. Commit the changes by adding a commit message and clicking "Commit new file."

**Step 3: Create a GitHub Actions Workflow**

1. In your repository, click on the "Actions" tab.

2. Choose "Set up a workflow yourself."

3. Replace the content in the text editor with the following YAML code:

```yaml
name: Hello World Python App

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    
    steps:
    - name: Check out code
      uses: actions/checkout@v2
      
    - name: Set up Python
      uses: actions/setup-python@v2
      with:
        python-version: 3.x
        
    - name: Run Python script
      run: python hello.py
```

4. Click on "Start commit" to commit the workflow file to your repository.

**Step 4: Trigger the Workflow**

1. In your repository, click on the "Actions" tab again.

2. You'll see your workflow listed. Click on "Hello World Python App."

3. On the right side, click on the "Run workflow" button. Select "Run workflow" to manually trigger the workflow.

4. You should see your workflow running. Click on the build job to see the logs.

5. Once the workflow completes, you should see the "Hello, World!" message in the logs.

