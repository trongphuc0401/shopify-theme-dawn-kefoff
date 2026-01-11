# 📚 THEME DOCUMENTATION INDEX

Chào mừng bạn đến với bộ tài liệu phân tích và hướng dẫn theme Shopify!

## 📖 CÁC TÀI LIỆU HIỆN CÓ

### 1. 📘 [THEME_ANALYSIS.md](./THEME_ANALYSIS.md)
**Phân tích chi tiết toàn bộ theme**

Nội dung:
- Tổng quan về theme (Dawn v15.4.1 based)
- Kiến trúc & cấu trúc thư mục
- Phong cách code & best practices
- Hệ thống CSS (Variables, BEM, Responsive)
- Hệ thống JavaScript (Web Components, PubSub)
- Liquid Template System
- Hướng dẫn custom theme chi tiết
- Performance & Optimization
- Common customization scenarios
- Troubleshooting

**Đọc file này khi:**
- Bạn muốn hiểu sâu về cách theme hoạt động
- Cần tìm hiểu về kiến trúc và design patterns
- Muốn học cách code theo chuẩn của theme
- Cần hướng dẫn chi tiết về customization

### 2. ⚡ [QUICK_REFERENCE.md](./QUICK_REFERENCE.md)
**Tham khảo nhanh các thông tin thường dùng**

Nội dung:
- Navigation - File nào chứa gì?
- CSS Variables cheat sheet
- Responsive breakpoints
- Liquid cheat sheet (filters, objects, loops)
- Common tasks (add CSS, JS, create sections)
- Debugging tips
- Shopify CLI commands
- BEM naming examples
- Performance tips
- Security & Accessibility

**Đọc file này khi:**
- Cần tra cứu nhanh syntax
- Quên CSS variable nào đó
- Cần copy-paste code snippet
- Đang code và cần tham khảo nhanh

### 3. ✅ [CUSTOMIZATION_CHECKLIST.md](./CUSTOMIZATION_CHECKLIST.md)
**Checklist đầy đủ cho mọi giai đoạn**

Nội dung:
- Before you start (Setup)
- Customization workflow (Planning → Implementation)
- Testing checklist (Functionality, Responsive, Browser, Performance)
- Accessibility testing (WCAG 2.1)
- SEO testing
- Code quality checklist
- Documentation checklist
- Pre-launch checklist
- Post-launch monitoring
- Maintenance schedule
- Emergency procedures

**Sử dụng file này khi:**
- Bắt đầu một dự án customization mới
- Trước khi launch theme
- Review code quality
- Testing theme
- Maintenance định kỳ

---

## 🚀 BẮT ĐẦU TỪ ĐÂU?

### Nếu bạn là người mới:
1. Đọc **THEME_ANALYSIS.md** phần 1-3 để hiểu tổng quan
2. Xem **QUICK_REFERENCE.md** để biết file nào ở đâu
3. Follow **CUSTOMIZATION_CHECKLIST.md** phần "Before You Start"

### Nếu bạn đã có kinh nghiệm:
1. Skim qua **THEME_ANALYSIS.md** phần 3 (Phong cách code)
2. Bookmark **QUICK_REFERENCE.md** để tra cứu
3. Sử dụng **CUSTOMIZATION_CHECKLIST.md** khi bắt đầu custom

### Nếu bạn cần custom một feature cụ thể:
1. Tìm trong **THEME_ANALYSIS.md** phần 10 (Common Scenarios)
2. Tham khảo **QUICK_REFERENCE.md** phần "Common Tasks"
3. Follow **CUSTOMIZATION_CHECKLIST.md** phần "Implementation Phase"

---

## 🎯 USE CASES

### "Tôi muốn thêm một section mới"
```
1. THEME_ANALYSIS.md → Section 7.3 (Add Custom Section)
2. QUICK_REFERENCE.md → "Common Tasks" → "Create New Section"
3. CUSTOMIZATION_CHECKLIST.md → "For New Sections"
```

### "Tôi muốn sửa product card"
```
1. QUICK_REFERENCE.md → Navigation → Find "Product card"
2. THEME_ANALYSIS.md → Section 7.5 (Modify Existing Components)
3. CUSTOMIZATION_CHECKLIST.md → "For Modifying Existing Components"
```

### "Tôi cần optimize performance"
```
1. THEME_ANALYSIS.md → Section 8 (Performance & Optimization)
2. QUICK_REFERENCE.md → "Performance Tips"
3. CUSTOMIZATION_CHECKLIST.md → "Performance Testing"
```

### "Tôi gặp lỗi"
```
1. THEME_ANALYSIS.md → Section 11 (Troubleshooting)
2. QUICK_REFERENCE.md → "Debugging"
3. CUSTOMIZATION_CHECKLIST.md → "Emergency Checklist"
```

---

## 📊 CẤU TRÚC THEME (Quick Overview)

```
shopify-theme-dawn/
├── 📁 assets/          (184 files) - CSS, JS, images
│   ├── base.css                    # Core styles
│   ├── global.js                   # Core JavaScript
│   └── component-*.css             # Component styles
│
├── 📁 config/          (2 files)
│   ├── settings_schema.json        # Theme settings UI
│   └── settings_data.json          # Current settings
│
├── 📁 layout/          (2 files)
│   ├── theme.liquid                # Main layout
│   └── password.liquid             # Password page
│
├── 📁 locales/         (51 files)  # Translations
│
├── 📁 sections/        (54 files)  # Page sections
│   ├── header.liquid
│   ├── footer.liquid
│   ├── main-product.liquid
│   └── ...
│
├── 📁 snippets/        (37 files)  # Reusable blocks
│   ├── card-product.liquid
│   ├── icon-*.liquid
│   └── ...
│
└── 📁 templates/       (20 files)  # Page templates
    ├── index.json
    ├── product.json
    └── collection.json
```

---

## 🔑 KEY CONCEPTS

### CSS Architecture
- **CSS Variables** cho theming
- **BEM naming** convention
- **Mobile-first** responsive design
- **Utility classes** for common patterns

### JavaScript Architecture
- **Vanilla JavaScript** (no jQuery)
- **Web Components** (Custom Elements)
- **PubSub pattern** for events
- **Lazy loading** for performance

### Liquid Templates
- **Component-based** structure
- **Schema-driven** settings
- **Section & Snippet** reusability
- **Translation-ready** (i18n)

---

## 💡 TIPS & BEST PRACTICES

### ✅ DO
- Luôn tạo file custom mới thay vì sửa file gốc
- Sử dụng CSS variables thay vì hardcode values
- Follow BEM naming convention
- Test trên mobile, tablet, desktop
- Document tất cả custom code
- Backup trước khi thay đổi lớn

### ❌ DON'T
- Không sửa trực tiếp file base (base.css, global.js)
- Không hardcode colors, spacing
- Không bỏ qua accessibility
- Không skip testing
- Không quên optimize images
- Không commit settings_data.json

---

## 🛠 DEVELOPMENT TOOLS

### Required
- **Shopify CLI**: `npm install -g @shopify/cli @shopify/theme`
- **Theme Check**: `npm install -g @shopify/theme-check`
- **Git**: Version control

### Recommended
- **VS Code** + Shopify Liquid extension
- **Chrome DevTools** for debugging
- **Lighthouse** for performance testing
- **WAVE** for accessibility testing

---

## 📞 SUPPORT & RESOURCES

### Official Documentation
- [Shopify Themes](https://shopify.dev/docs/themes)
- [Liquid Reference](https://shopify.dev/docs/api/liquid)
- [Dawn GitHub](https://github.com/Shopify/dawn)

### Community
- [Shopify Community Forums](https://community.shopify.com)
- [Shopify Discord](https://discord.gg/shopify)
- [Shopify Partners Blog](https://www.shopify.com/partners/blog)

### Learning
- [Learn Shopify Development](https://learn.shopify.com)
- [Web.dev Performance](https://web.dev/performance/)
- [MDN Web Docs](https://developer.mozilla.org)

---

## 📝 VERSION HISTORY

### Current Version
- **Base Theme**: Dawn v15.4.1
- **Customization Level**: ~60% (Horizon customization)
- **Documentation Created**: 2026-01-08

### Tracking Changes
- Sử dụng Git để track changes
- Document mọi customization
- Maintain changelog for major updates

---

## 🎓 LEARNING PATH

### Beginner (1-2 weeks)
1. Đọc THEME_ANALYSIS.md phần 1-2 (Tổng quan + Kiến trúc)
2. Tìm hiểu Liquid basics
3. Học CSS Variables usage
4. Làm quen với Shopify CLI
5. Tạo section đơn giản đầu tiên

### Intermediate (2-4 weeks)
1. Đọc THEME_ANALYSIS.md phần 3-6 (Code patterns)
2. Tạo custom components
3. Học Web Components pattern
4. Optimize performance
5. Implement responsive design

### Advanced (1-2 months)
1. Đọc toàn bộ THEME_ANALYSIS.md
2. Build complex features
3. Custom JavaScript interactions
4. Advanced Liquid techniques
5. Theme architecture mastery

---

## 🚨 BEFORE LAUNCH

Checklist tối thiểu:
- [ ] Đọc CUSTOMIZATION_CHECKLIST.md phần "Pre-Launch"
- [ ] Test tất cả functionality
- [ ] Kiểm tra responsive design
- [ ] Run Lighthouse performance audit (>50 mobile, >80 desktop)
- [ ] Accessibility audit (WCAG AA)
- [ ] Test trên nhiều browsers
- [ ] Backup theme hiện tại
- [ ] Document tất cả custom code

---

**🎉 Chúc bạn thành công với việc custom theme!**

Có câu hỏi? Tra cứu trong các tài liệu trên hoặc tham khảo tài liệu chính thức của Shopify.
