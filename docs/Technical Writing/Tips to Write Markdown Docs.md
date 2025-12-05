# Tips to Write Markdown Docs

## 1. Adding Images

###  1.1 Local Images

Step 1: Place image files inside the `docs` folder 

```
	docs/
	└─ Images/
		└─ Aligner.jpg
```

Step 2: Use relative paths in the Markdown files 

`[Alternative Text](image-path "Optional title")`

e.g., `[Aligner Interface](Image/xxx.jpg "Matecat Aligner Interface")`

- `Images/xxx.jpg` → path relative to the current `.md` file

- Do not use full Windows path (`D:/…`)

- Filenames are case-sensitive

### 1.2 Online Images

To reference an image hosted online, use the URL directly:

`[Alternative Text] (URL "Optional title")`

e.g., `[Aligner Interface] (https://to-be-completed/image.jpg "Matecat Aligner Interface")`

- `https://to-be-completed/image.jpg` → an online image address

### 1.3 Explanation of Image Syntax

```
![Alternative Text](image-path "Optional title")
![Alternative Text](image-path "Optional title")
```

- `![Alternative Text]` → Text shown when the image fails to load (Improves accessibility for screen readers).

- `image-path` → Path to the image (can be relative path inside `docs/` or an online URL).

- `Optional title` → Text shown when hovering the mouse over the image (optional).

## Adding Table

| CN                  | EN           | 说明          |
|:------------------- |:------------:| ------------:|
| USB debugging mode  | <span style="color:blue">USB调试模式</span>   | 调试功能<br>用于开发者      |
| APP twin            | 应用分身      | 分身应用      |

- `:---` → 左对齐

- `:---:` → 居中

- `---:` → 右对齐

- `<br>` → 换行

- `<span style="color:blue">xxxx</span> ` → 渲染文本

**Note:** 无法跨列


