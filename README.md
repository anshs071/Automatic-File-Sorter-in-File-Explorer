# Automatic-File-Sorter-in-File-Explorer

This code snippet is a Python script designed to organize files in a specified directory into different folders based on their file extensions. Here's a breakdown of how it works:

1. **Importing Necessary Modules**: 
   - `os`: Provides functions for interacting with the operating system, such as file manipulation and directory operations.
   - `shutil`: Offers high-level file operations such as moving and copying files.

2. **Defining the Path and Listing Files**:
   - `path`: A string variable containing the path to the desired folder.
   - `file_name`: A list containing the names of all the files in the specified directory obtained using `os.listdir(path)`.

3. **Defining Folder Names**:
   - `folder_names`: A list containing the names of folders to store files with specific extensions.

4. **Creating Folders if They Don't Exist**:
   - A loop iterates over the `folder_names` list.
   - For each folder name, it checks if the corresponding folder exists in the specified directory using `os.path.exists()`.
   - If the folder doesn't exist, it creates the folder using `os.makedirs()`.

5. **Organizing Files Based on Extensions**:
   - Another loop iterates over the list of file names (`file_name`).
   - For each file, it checks its extension and moves it to the corresponding folder if it meets the conditions:
     - If the file has a ".csv" or ".xlsx" extension and is not already in the "excel files" folder, it is moved to the "excel files" folder.
     - Similar checks are performed for other file types (images, PDFs, Word documents, PowerPoint presentations) and moved to their respective folders if they are not already there.

6. **Comments for Customization**:
   - The script includes comments to guide users on how to customize the folder names, file extensions, and path according to their needs.

Overall, this script automates the task of organizing files into different folders based on their extensions, providing a convenient way to manage files in a directory.
