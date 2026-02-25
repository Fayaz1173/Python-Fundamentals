# File Bulk Renaming

```python
import os

folder_path = "Z:/brocamp/python_week/folder"
files = os.listdir(folder_path)

for file in files:
    old_path = os.path.join(folder_path, file)
    

    new_name = "new_" + file
    new_path = os.path.join(folder_path, new_name)

    os.rename(old_path, new_path)

print("Files renamed successfully.")
```

File before renaming :

<img width="379" height="102" alt="image" src="https://github.com/user-attachments/assets/244b78ef-f1fd-4459-bd0e-f4c8e4bea374" />
<img width="379" height="102" alt="image" src="https://github.com/user-attachments/assets/244b78ef-f1fd-4459-bd0e-f4c8e4bea374" />

File after renaming : 

<img width="445" height="137" alt="image" src="https://github.com/user-attachments/assets/2ea00030-08ae-4ae7-89c4-4dd702be37e8" />
<img width="445" height="137" alt="image" src="https://github.com/user-attachments/assets/2ea00030-08ae-4ae7-89c4-4dd702be37e8" />

# Rename Files with Numbers (Sequential Naming)

```python
import os

folder_path = "Z:/brocamp/python_week/image_folder"
files = os.listdir(folder_path)

count = 1

for file in files:
    old_path = os.path.join(folder_path, file)
    
    new_name = f"image{count}.png"
    new_path = os.path.join(folder_path, new_name)
    
    os.rename(old_path, new_path)
    count += 1

print("Files renamed with numbers.")
```

File before renaming :

<img width="431" height="625" alt="image" src="https://github.com/user-attachments/assets/f018c879-a2d6-47b0-aed6-1ee8461e2301" />
<img width="431" height="625" alt="image" src="https://github.com/user-attachments/assets/f018c879-a2d6-47b0-aed6-1ee8461e2301" />

File after renaming : 

<img width="422" height="625" alt="image" src="https://github.com/user-attachments/assets/6d623db4-eb4c-4b3a-a7df-4174b8dba7ee" />
<img width="422" height="625" alt="image" src="https://github.com/user-attachments/assets/6d623db4-eb4c-4b3a-a7df-4174b8dba7ee" />
