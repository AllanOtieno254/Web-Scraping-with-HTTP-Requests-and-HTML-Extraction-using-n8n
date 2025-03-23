# **Web Scraping with HTTP Requests and HTML Extraction using n8n**
![main workflow](https://github.com/user-attachments/assets/0968a389-2512-4ab4-a5fc-228e46d6fbdf)

## **Project Overview**
This project demonstrates how to extract structured information from a webpage using the **HTML node** and **HTTP Request node** in n8n. The goal is to fetch and parse HTML content from a webpage using CSS selectors, which is useful for web scraping and data extraction.

The final output, named **"main output"**, integrates the workflow of making an HTTP request, extracting HTML elements, and processing the retrieved data.

## **Project Workflow**
### **1. Extracting HTML Content using CSS Selectors**
We use the **HTML node** to extract specific HTML content from a webpage by referencing **CSS selectors**. This is particularly useful when collecting structured information such as blog titles, product listings, or other webpage elements.
![html](https://github.com/user-attachments/assets/09481536-6986-41f4-bae9-48ed4ffeb10a)

### **2. HTTP Request for Web Scraping**
To retrieve webpage content, we use the **HTTP Request node** to send a `GET` request to a specified URL. This node allows us to obtain the full HTML content of the page.
![http request](https://github.com/user-attachments/assets/0b8cfdfa-0430-4aba-a8b8-b982162a5daf)

### **3. Parsing HTML and Extracting Data**
Once the webpage data is retrieved, we process it using the **HTML node** by specifying the **CSS selector** to extract desired elements.
![html](https://github.com/user-attachments/assets/09481536-6986-41f4-bae9-48ed4ffeb10a)
---

## **Project Implementation**
### **Exercise: Extracting the Title of the Latest n8n Blog Post**
This exercise demonstrates how to extract the title of the latest blog post from the **n8n blog**.

#### **Step 1: Send an HTTP Request**
1. Configure the **HTTP Request node** with the following parameters:
   - **Authentication:** None
   - **Request Method:** `GET`
   - **URL:** `https://blog.n8n.io/`

2. The expected result should return the HTML content of the blog page.

#### **Step 2: Extract Data with the HTML Node**
1. Connect an **HTML node** to the **HTTP Request node**.
2. Configure the **HTML node** with the following parameters:
   - **Operation:** Extract HTML Content
   - **Source Data:** JSON
   - **JSON Property:** `data`
   - **Extraction Values:**
     - **Key:** `title`
     - **CSS Selector:** `.post .item-title a`
     - **Return Value:** `HTML`

3. The extracted data will return the **title of the latest blog post**.

#### **Step 3: Output the Final Result**
The processed data is structured and presented as the **main output**, which consists of the extracted blog title.

---

## **Project Structure**
The project consists of the following assets:

| File Name | Description |
|-----------|-------------|
| `html.png` | A visual representation of the HTML structure used in extraction. |
| `http request.png` | An illustration of the HTTP request workflow. |
| `main workflow.png` | A complete workflow diagram showing the integration of web scraping components. |
| `main output` | The final output containing extracted blog titles from the webpage. |

---

## **Technologies Used**
- **n8n** – Workflow automation for HTTP requests and HTML parsing.
- **HTML & CSS** – Webpage structure and styling.
- **HTTP Protocol** – Request and response cycle.
- **CSS Selectors** – Extracting specific webpage elements.

---

## **How to Use This Project**
1. **Understand the workflow diagrams** (`main workflow.png`) to see the data flow.
2. **Run the HTTP Request node** to fetch webpage content.
3. **Use the HTML node** to extract the relevant elements using CSS selectors.
4. **Analyze the extracted output** to ensure data is structured correctly.

---

## **Future Improvements**
- Add more extraction values (e.g., publication dates, article descriptions).
- Implement pagination handling for multiple blog posts.
- Convert the extracted data into a structured dataset (CSV/JSON).
- Automate the process with scheduled runs.

---

## **License**
This project is open-source and can be freely used for learning and development.

---

🚀 **Happy Scraping!**
