### BOM (Browser Operation Model)

---

1. 浏览器 的渲染模式

   - 标准模式

     ```html
     <!DOCTYPE html>
     # 使用该头部描述的 html 采用 标准模式 进行渲染！
     ```

   - 怪异模式/混杂模式 (为了向后兼容)

     ```
     # 为了后向兼容，主动选择不采用标准模式 进行渲染
     方法是：去掉头部 DOCTYPE 描述
     ```

     