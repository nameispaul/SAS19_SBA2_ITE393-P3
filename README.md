# MyApplication

## Overview
MyApplication is a simple Android application that demonstrates how to parse a JSON object and display the data in a `ListView`. The app reads a hardcoded JSON string containing user details (name, designation, and location), extracts the data using `JSONObject`, and presents it in a structured list format.

This project is based on the original tutorial from GeeksforGeeks: [JSON Parsing in Android](https://www.geeksforgeeks.org/json-parsing-in-android/).

## Features
- Parses JSON data containing user details.
- Displays extracted user information in a `ListView`.
- Uses `SimpleAdapter` to populate the list dynamically.
- Handles potential JSON parsing exceptions with proper logging.

## Technologies Used
- **Language**: Kotlin
- **Framework**: Android SDK
- **UI Components**: `ListView`, `SimpleAdapter`
- **Parsing Library**: `org.json.JSONObject`

## Project Structure
```
MyApplication/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/example/myapplication/
│   │   │   │   ├── MainActivity.kt  # Main application logic
│   │   │   ├── res/
│   │   │   │   ├── layout/
│   │   │   │   │   ├── activity_main.xml  # Main layout containing ListView
│   │   │   │   │   ├── list_row.xml  # Layout for individual list items
│   ├── AndroidManifest.xml  # App manifest file
```

## Code Explanation
1. **Parsing JSON**:
   - A JSON string is stored in `listData`.
   - The app converts this string into a `JSONObject` and retrieves the array of users.
   - It extracts the `name`, `designation`, and `location` values and stores them in a list.

2. **Displaying Data**:
   - A `ListView` is initialized in `onCreate()`.
   - A `SimpleAdapter` maps the extracted data to UI elements in `list_row.xml`.
   - The adapter is then set to the `ListView` to display the data.

3. **Error Handling**:
   - If JSON parsing fails, an error is logged using `Log.e()`.

## How to Run
1. Clone this repository:
   ```sh
   git clone https://github.com/your-repo/MyApplication.git
   ```
2. Open the project in Android Studio.
3. Build and run the application on an emulator or a physical device.

## Screenshots
| List View UI |
|-------------|
| ![App UI](![Screenshot_2025-03-21-11-51-44-764_com example myapplication](https://github.com/user-attachments/assets/7442373a-f141-408e-90d7-64314dac3525)
) |

## Future Enhancements
- Fetch JSON data from a remote API instead of using hardcoded strings.
- Improve UI with `RecyclerView` for better performance.
- Implement search and filter functionality.
