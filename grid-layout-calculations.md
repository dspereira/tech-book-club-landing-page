# CSS Grid Layout Calculations

## Mobile

- **6 columns** in total:
  - **4 center columns**
  - **2 margin columns** (left and right)

- **21px** margin on the left and right:
  - Total margin: `2 * 21px = 42px`

- **3 gutters** in the middle, each **20px** wide:
  - Total gutters width: `3 * 20px`


```css
    calc((100% - 42px - 3 * 20px) / 4)
```

```css
    .grid-main {
        display: grid;
        grid-template-columns: 1fr repeat(4, calc((100% - 42px - 3 * 20px) / 4)) 1fr;
        gap: 20px;
    }
```

## Tablet > 700px
  
- **10 columns** in total:
- **6 center columns**
- **2 margin columns** (left and right)

- **32px** margin on the left and right:
  - Total margin: `2 * 32px = 64px`

- **7 gutters** in the middle, each **24px** wide:
  - Total gutters width: `7 * 24px`


```css
    calc((100% - 64px - 7 * 24px) / 8)
```

```css
    .grid-main {
        display: grid;
        grid-template-columns: 1fr repeat(8, calc((100% - 64px - 7 * 24px) / 8)) 1fr;
        gap: 24px;
    }
```

## Desktop > 1240px

- **14 columns** in total:
- **12 center columns**
- **2 margin columns** (left and right)

- **11 gutters** in the middle, each **30px** wide:
  - Total gutters width: `11 * 30px`

- **Content size**: 1170px (calculated as `117rem * 10px`)


```css
    calc((117rem - 11 * 30px) / 12)
```

```css
    .grid-main {
        display: grid;
        grid-template-columns: 1fr repeat(12, calc((117rem - 11 * 30px) / 12)) 1fr;
        gap: 30px;
    }
```