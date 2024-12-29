<p align="center">
  <img src="https://github.com/Creator754915/HolyC-Code-Syntax/blob/main/images/HolyC_Logo.png" alt="HolyC Logo">
  <br>
  <img src="https://img.shields.io/badge/Version-1.0.1-green?style=for-the-badge" alt="Version Badge">
  <br>
  <img src="https://img.shields.io/badge/Author-Creator754915-blue?style=flat-square" alt="Author Badge">
  <img src="https://img.shields.io/badge/Open%20Source-Yes-darkgreen?style=flat-square" alt="Open Source Badge">
  <img src="https://img.shields.io/badge/Maintained%3F-Yes-lightblue?style=flat-square" alt="Maintained Badge">
</p>

# HolyC Code Syntax

Welcome to **HolyC Code Syntax** — the ultimate extension to simplify and accelerate your HolyC coding experience in Visual Studio Code.

---

## 🚀 Features

### Visual Studio Code Integration  
A seamless integration providing comprehensive syntax highlighting for HolyC.

### Snippets  
Efficient, prebuilt snippets to speed up your development process.

---

## 🔄 Latest Updates

### **Version 1.5.0**

- **`freeMen`**: Get free space from a pointer  
  ```holyc
  public _extern _FREE U0 Free(U0 *ptr);
  ```

- **`reAlloc`**: Relocate a portion of memory
  ```holyc
  public _extern _REALLOC U0 *ReAlloc(U0 *ptr, U64 new_size);
  ```

- List
  
  - **newList**: Create a simple list.
    ```holyc
    List *myList = ListNew();
    ```

  - **appendToList**: Add an element to a list.
    ```holyc
    U0 ListAppend(List *myList, U0 *$2);
    ```

  - **popList**: Delete the last element of a list.
    ```holyc
    U0 *ListPop(U0 *myList);
    ```

  - **isListEmpty**: Check if a list is empty.
    ```holyc
    Bool ListEmpty(List *myList);
    ```

  - **listLength**: Count the number of elements in a list.
    ```holyc
    I64 ListCount(List *myList);
    ```

- JSON

  - **jsonOk**: Validate JSON parsing.
    ```holyc
    public Bool JsonOk(Json *jsonFile);
    ```

  - **jsonToString**: Convert JSON to string.
    ```holyc
    public U8 *JsonToString(Json *jsonFile);
    ```

  - **jsonSelect**: Enable JSON selection.
    ```holyc
    public Json *JsonSelect(Json *jsonFile, U8 *JSON_ELEMENT, <some_variable>);
    ```

  - **JsonParseExample**: Example HolyC script for JSON parsing.
    ```holyc
    U0 Main()
    {
      I64 len = 0;
      U8 *raw = FileRead("./example.json",&len);
      Json *json = JsonParse(raw,len);
    
      if (!JsonOk(json)) {
        JsonPrintError(json);
        JsonRelease(json);
        return;
      }
    
      Json *id = JsonSelect(json,".ids[2]:i");
      if (!id) {
        return;
      }
      "ID = %d\n",id->int;
      JsonRelease(json);
    }
    ```

## ✂️ Custom Snippets

Total Snippets: 24
Main Project Setup: Quickly scaffold a basic HolyC project.


String Conversion: Easily convert a char or string to uppercase.


🎨 Theme and UI
Example: Game.hc


Example: Main.hc


📋 Requirements
Basic knowledge of HolyC is all you need!
🛠️ How to Install
Go to Extensions > Install from VSIX in Visual Studio Code.
Select the file holyc-code-syntax-1.0.0.vsix (version may vary).
Enjoy enhanced HolyC syntax highlighting in your editor!
📝 Release Notes
1.0.1
Added #include, union, public, and static to the syntax.
Introduced new snippets (total: 13).
1.0.0
Initial release with all basic HolyC language support.
📞 Support
For questions, suggestions, or issues, visit:
My GitHub Repository
