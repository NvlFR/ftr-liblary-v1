# Cheat Sheet Markdown Lengkap

## 1. Heading (Judul)
Gunakan tanda pagar `#` untuk membuat heading (1–6 level).

```markdown
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```

### Hasil:
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6

---

## 2. Format Teks

### 2.1 Format Dasar
```markdown
**Tebal** atau __Tebal__
*Miring* atau _Miring_
***Tebal & Miring*** atau ___Tebal & Miring___
~~Coret~~
`Inline Code`
```

### Hasil:
**Tebal** atau __Tebal__  
*Miring* atau _Miring_  
***Tebal & Miring*** atau ___Tebal & Miring___  
~~Coret~~  
`Inline Code`

### 2.2 Format Lanjutan
```markdown
H~2~O (subscript - GitHub)
X^2^ (superscript - GitHub)
==Highlight== (beberapa platform)
> Blockquote
>> Nested blockquote
```

---

## 3. Daftar (List)

### 3.1 Unordered List
```markdown
- Item 1
- Item 2
  - Subitem
    - Sub-subitem
+ Atau gunakan plus
* Atau gunakan asterisk
```

### Hasil:
- Item 1
- Item 2
  - Subitem
    - Sub-subitem

### 3.2 Ordered List
```markdown
1. Item pertama
2. Item kedua
   1. Subitem
   2. Subitem
3. Item ketiga
```

### Hasil:
1. Item pertama
2. Item kedua
   1. Subitem
   2. Subitem
3. Item ketiga

### 3.3 Task List (Checklist)
```markdown
- [x] Task selesai
- [ ] Task belum selesai
- [x] ~~Task yang dibatalkan~~
```

### Hasil:
- [x] Task selesai
- [ ] Task belum selesai
- [x] ~~Task yang dibatalkan~~

---

## 4. Link dan Gambar

### 4.1 Link
```markdown
[Link biasa](https://example.com)
[Link dengan title](https://example.com "Hover text")
<https://example.com> (auto link)
[Link referensi][1]
[Link referensi dengan teks berbeda][ref-link]

[1]: https://example.com
[ref-link]: https://example.com "Title opsional"
```

### 4.2 Gambar
```markdown
![Alt text](https://via.placeholder.com/150)
![Alt text](https://via.placeholder.com/150 "Title")
[![Gambar dengan link](image.jpg)](https://example.com)

<!-- Gambar referensi -->
![Alt text][image-ref]
[image-ref]: https://via.placeholder.com/150
```

---

## 5. Kode (Code)

### 5.1 Inline Code
```markdown
Gunakan `backtick` untuk inline code: `console.log("Hello")`
```

### 5.2 Code Block
Tanpa syntax highlighting:
````markdown
```
function hello() {
    console.log("Hello World!");
}
```
````

Dengan syntax highlighting:
````markdown
```javascript
function hello() {
    console.log("Hello World!");
}
```

```python
def hello():
    print("Hello World!")
```

```bash
echo "Hello World!"
```

```html
<h1>Hello World!</h1>
```

```css
body {
    color: #333;
    font-family: Arial, sans-serif;
}
```
````

---

## 6. Tabel

### 6.1 Tabel Dasar
```markdown
| Kolom 1 | Kolom 2 | Kolom 3 |
|---------|---------|---------|
| Baris 1 | Data 1  | Data 2  |
| Baris 2 | Data 3  | Data 4  |
```

### Hasil:
| Kolom 1 | Kolom 2 | Kolom 3 |
|---------|---------|---------|
| Baris 1 | Data 1  | Data 2  |
| Baris 2 | Data 3  | Data 4  |

### 6.2 Tabel dengan Alignment
```markdown
| Kiri    | Tengah  | Kanan   |
|:--------|:-------:|--------:|
| Kiri    | Tengah  | Kanan   |
| Text    | Text    | Text    |
```

### Hasil:
| Kiri    | Tengah  | Kanan   |
|:--------|:-------:|--------:|
| Kiri    | Tengah  | Kanan   |
| Text    | Text    | Text    |

---

## 7. Garis Horizontal (Horizontal Rule)
```markdown
---
***
___
```

### Hasil:
---

## 8. Blockquote (Kutipan)
```markdown
> Ini adalah blockquote
> Bisa multi-line

> Blockquote dengan **formatting**
> 
> > Nested blockquote
```

### Hasil:
> Ini adalah blockquote
> Bisa multi-line

> Blockquote dengan **formatting**
> 
> > Nested blockquote

---

## 9. Escape Character
```markdown
\*Tidak akan jadi miring\*
\`Tidak akan jadi code\`
\# Tidak akan jadi heading
```

### Hasil:
\*Tidak akan jadi miring\*  
\`Tidak akan jadi code\`  
\# Tidak akan jadi heading

---

## 10. HTML dalam Markdown
```html
<details>
<summary>Click untuk expand</summary>
Konten yang bisa di-expand/collapse
</details>

<kbd>Ctrl</kbd> + <kbd>C</kbd>

<mark>Highlighted text</mark>

<sub>subscript</sub> dan <sup>superscript</sup>
```

### Hasil:
<details>
<summary>Click untuk expand</summary>
Konten yang bisa di-expand/collapse
</details>

<kbd>Ctrl</kbd> + <kbd>C</kbd>

---

## 11. Footnote (Catatan Kaki)
```markdown
Ini adalah teks dengan footnote[^1].
Ini footnote lain[^note].

[^1]: Ini adalah footnote pertama.
[^note]: Ini adalah footnote dengan nama.
```

---

## 12. Definition Lists
```markdown
Term 1
:   Definisi term 1

Term 2
:   Definisi term 2
:   Definisi kedua untuk term 2
```

---

## 13. Math (LaTeX) - Platform tertentu
```markdown
Inline math: $E = mc^2$

Block math:
$$
\sum_{i=1}^{n} x_i = x_1 + x_2 + \ldots + x_n
$$
```

---

## 14. Emoji (GitHub, Discord, dll)
```markdown
:smile: :heart: :thumbsup: :rocket: :fire: :100:
```

### Hasil (di platform yang support):
:smile: :heart: :thumbsup: :rocket: :fire: :100:

---

## 15. Line Break
```markdown
Baris pertama  
Baris kedua (2 spasi di akhir baris pertama)

Baris pertama\
Baris kedua (backslash di akhir)

Baris pertama<br>
Baris kedua (HTML tag)
```

---

## 16. Comments (Komentar)
```markdown
<!-- Ini adalah komentar yang tidak akan ditampilkan -->

[//]: # (Ini juga komentar)
[//]: <> (Alternatif lain untuk komentar)
```

---

## 17. Mentions dan References (GitHub)
```markdown
@username (mention user)
#123 (reference issue/PR)
SHA: a5c3785ed8d6a35868bc169f07e40e889087fd2e
user/repo#123 (cross-repo reference)
```

---

## 18. Keyboard Shortcuts
```markdown
<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>Del</kbd>
<kbd>⌘</kbd> + <kbd>Space</kbd> (Mac)
```

### Hasil:
<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>Del</kbd>

---

## 19. Admonitions/Callouts (Platform tertentu)
```markdown
> [!NOTE]
> Informasi berguna yang perlu diperhatikan

> [!TIP]
> Tips atau saran yang membantu

> [!IMPORTANT]
> Informasi penting yang krusial

> [!WARNING]
> Peringatan tentang sesuatu yang berisiko

> [!CAUTION]
> Peringatan negatif tentang tindakan berisiko
```

---

## 20. Mermaid Diagrams (GitHub, GitLab)
````markdown
```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```
````

---

## Tips dan Best Practices

### 1. Konsistensi
- Pilih satu style untuk format yang sama (misalnya `*` atau `_` untuk miring)
- Konsisten dalam penggunaan spasi dan indentasi

### 2. Readability
- Gunakan baris kosong untuk memisahkan section
- Indentasi yang proper untuk nested lists
- Gunakan heading hierarchy yang logis

### 3. Compatibility
- Test di platform target Anda
- Beberapa fitur hanya work di platform tertentu (GitHub, GitLab, dll)
- Fallback untuk fitur yang tidak universal

### 4. Performance
- Optimasi gambar sebelum embed
- Gunakan relative path untuk project lokal
- Pertimbangkan loading time untuk konten berat

---

## Platform-Specific Features

### GitHub Flavored Markdown (GFM)
- Task lists
- Tables
- Strikethrough
- Auto-linking
- Emoji shortcodes
- Syntax highlighting

### Discord
- Spoiler tags: `||spoiler text||`
- Code blocks dengan syntax highlighting

### Obsidian
- Wiki links: `[[Link]]`
- Tags: `#tag`
- Math dengan MathJax

### Notion
- Callout blocks
- Toggle blocks
- Databases

---

*Cheat sheet ini mencakup mayoritas syntax Markdown yang umum digunakan. Selalu check dokumentasi platform spesifik untuk fitur tambahan.*