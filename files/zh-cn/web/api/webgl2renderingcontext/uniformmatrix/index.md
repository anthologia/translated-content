---
title: WebGL2RenderingContext.uniformMatrix[234]x[234]fv()
slug: Web/API/WebGL2RenderingContext/uniformMatrix
---

{{APIRef("WebGL")}} {{SeeCompatTable}}

[WebGL 2 API](/zh-CN/docs/Web/API/WebGL_API) 的 **`WebGL2RenderingContext.uniformMatrix[234]x[234]fv()`** 方法向 uniform 变量中传入指定的矩阵值。

> **备注：** 这个方法不用 `2x2`, `3x3`, 和 `4x4` 版本 . 他们通常用`2`, `3`, 和`4`, 分别表示，详见下方语法。

## 语法

```
void gl.uniformMatrix2fv(location, transpose, data, optional srcOffset, optional srcLength);
void gl.uniformMatrix3x2fv(location, transpose, data, optional srcOffset, optional srcLength);
void gl.uniformMatrix4x2fv(location, transpose, data, optional srcOffset, optional srcLength);
void gl.uniformMatrix2x3fv(location, transpose, data, optional srcOffset, optional srcLength);
void gl.uniformMatrix3fv(location, transpose, data, optional srcOffset, optional srcLength);
void gl.uniformMatrix4x3fv(location, transpose, data, optional srcOffset, optional srcLength);
void gl.uniformMatrix2x4fv(location, transpose, data, optional srcOffset, optional srcLength);
void gl.uniformMatrix3x4fv(location, transpose, data, optional srcOffset, optional srcLength);
void gl.uniformMatrix4fv(location, transpose, data, optional srcOffset, optional srcLength);
```

### 参数

- location
  - : 一个包含想要修改的 uniform 变量的{{domxref("WebGLUniformLocation")}} 对象
- transpose
  - : 一个决定是否转置矩阵的布尔值（ {{domxref("GLboolean")}}。 在 webgl 中必须为`false`。
- data
  - : 一个包含方阵中浮点数的类数组对象 (TypeArray) {{jsxref("Float32Array")}}。

### 返回值

没有。

## 例子

```js
gl.uniformMatrix2x3fv(loc, false, [1, 2, 3, 4, 5, 6]);
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat("api.WebGL2RenderingContext.uniformMatrix2fv")}}

## 令见

- {{domxref("WebGLRenderingContext.uniformMatrix()")}}
