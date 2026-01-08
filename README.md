import os

def list_file_extensions(directory_path):
    """Lists all files in a directory and identifies their extensions."""
    if not os.path.exists(directory_path):
        print("Path does not exist!")
        return

    for filename in os.listdir(directory_path):
        if os.path.isfile(os.path.join(directory_path, filename)):
            name, extension = os.path.splitext(filename)
            print(f"File: {name} | Extension: {extension}")

# Test the function on the current directory
list_file_extensions(".")
