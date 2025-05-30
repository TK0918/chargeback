# 拒付预警管理平台 UI 设计规范

## 1. 设计概述

### 1.1 设计理念
- **扁平化设计**: 简洁明了，突出功能性
- **数据驱动**: 以数据展示和操作为核心的界面设计
- **用户友好**: 降低学习成本，提升操作效率
- **专业感**: 符合金融风控平台的专业要求

### 1.2 设计原则
- 信息层次清晰，关键数据突出显示
- 交互简单直观，减少用户认知负担
- 响应式设计，适配不同设备屏幕
- 一致性设计语言，统一用户体验

## 2. 视觉设计系统

### 2.1 色彩规范

#### 主色调系统
```css
/* 主色调 - 橙色系 */
--primary-orange: #FF6B35;        /* 主橙色 */
--primary-orange-light: #FF8659;  /* 浅橙色 */
--primary-orange-dark: #E55A2B;   /* 深橙色 */
--primary-orange-pale: #FFF4F0;   /* 极浅橙色背景 */

/* 辅助色彩 */
--secondary-blue: #2E86C1;        /* 辅助蓝色 */
--secondary-green: #28B463;       /* 成功绿色 */
--secondary-red: #E74C3C;         /* 危险红色 */
--secondary-yellow: #F39C12;      /* 警告黄色 */

/* 中性色彩 */
--gray-50: #F8FAFC;               /* 极浅灰 */
--gray-100: #F1F5F9;              /* 浅灰背景 */
--gray-200: #E2E8F0;              /* 边框灰 */
--gray-300: #CBD5E1;              /* 分割线 */
--gray-400: #94A3B8;              /* 次要文字 */
--gray-500: #64748B;              /* 普通文字 */
--gray-600: #475569;              /* 主要文字 */
--gray-700: #334155;              /* 标题文字 */
--gray-800: #1E293B;              /* 深色文字 */
--gray-900: #0F172A;              /* 最深色 */

/* 背景色彩 */
--bg-primary: #FFFFFF;            /* 主背景 */
--bg-secondary: #F8FAFC;          /* 次背景 */
--bg-tertiary: #F1F5F9;           /* 三级背景 */
```

#### 语义化颜色
```css
/* 状态色彩 */
--success: #22C55E;               /* 成功状态 */
--success-light: #DCFCE7;         /* 成功背景 */
--warning: #F59E0B;               /* 警告状态 */
--warning-light: #FEF3C7;         /* 警告背景 */
--danger: #EF4444;                /* 危险状态 */
--danger-light: #FEE2E2;          /* 危险背景 */
--info: #3B82F6;                  /* 信息状态 */
--info-light: #DBEAFE;            /* 信息背景 */

/* 风险等级色彩 */
--risk-high: #DC2626;             /* 高风险 */
--risk-medium: #F59E0B;           /* 中风险 */
--risk-low: #16A34A;              /* 低风险 */
```

### 2.2 字体规范

#### 字体族
```css
/* 中文字体 */
--font-family-base: 'PingFang SC', 'Hiragino Sans GB', 'Microsoft YaHei', 
                    'WenQuanYi Micro Hei', sans-serif;

/* 数字字体 */
--font-family-number: 'SF Mono', 'Monaco', 'Inconsolata', 'Roboto Mono', 
                      monospace;
```

#### 字体大小层级
```css
/* 标题字体 */
--font-size-h1: 32px;             /* 页面主标题 */
--font-size-h2: 24px;             /* 模块标题 */
--font-size-h3: 20px;             /* 卡片标题 */
--font-size-h4: 18px;             /* 子标题 */
--font-size-h5: 16px;             /* 小标题 */

/* 正文字体 */
--font-size-base: 14px;           /* 基础文字 */
--font-size-large: 16px;          /* 大号文字 */
--font-size-small: 12px;          /* 小号文字 */
--font-size-xs: 10px;             /* 极小文字 */

/* 行高 */
--line-height-base: 1.5;          /* 基础行高 */
--line-height-tight: 1.25;        /* 紧密行高 */
--line-height-loose: 1.75;        /* 宽松行高 */
```

### 2.3 间距规范

```css
/* 间距系统 */
--spacing-xs: 4px;                /* 极小间距 */
--spacing-sm: 8px;                /* 小间距 */
--spacing-md: 16px;               /* 中等间距 */
--spacing-lg: 24px;               /* 大间距 */
--spacing-xl: 32px;               /* 超大间距 */
--spacing-2xl: 48px;              /* 巨大间距 */

/* 组件间距 */
--component-padding: 16px;        /* 组件内边距 */
--card-padding: 20px;             /* 卡片内边距 */
--section-margin: 32px;           /* 模块间距 */
```

### 2.4 圆角与阴影

```css
/* 圆角 */
--border-radius-sm: 4px;          /* 小圆角 */
--border-radius-md: 6px;          /* 中圆角 */
--border-radius-lg: 8px;          /* 大圆角 */
--border-radius-xl: 12px;         /* 超大圆角 */

/* 阴影 */
--shadow-sm: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
--shadow-md: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
--shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
--shadow-xl: 0 20px 25px -5px rgba(0, 0, 0, 0.1);
```

## 3. 组件设计规范

### 3.1 按钮设计

#### 主要按钮
```html
<!-- 主要按钮 -->
<button class="btn btn-primary">
  <svg class="btn-icon">...</svg>
  确认处理
</button>

<!-- 次要按钮 -->
<button class="btn btn-secondary">取消</button>

<!-- 危险按钮 -->
<button class="btn btn-danger">删除</button>

<!-- 文字按钮 -->
<button class="btn btn-text">查看详情</button>
```

```css
.btn {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 8px 16px;
  border-radius: var(--border-radius-md);
  font-size: var(--font-size-base);
  font-weight: 500;
  border: none;
  cursor: pointer;
  transition: all 0.2s ease;
}

.btn-primary {
  background: var(--primary-orange);
  color: white;
}

.btn-primary:hover {
  background: var(--primary-orange-dark);
  transform: translateY(-1px);
  box-shadow: var(--shadow-md);
}

.btn-secondary {
  background: var(--gray-100);
  color: var(--gray-600);
  border: 1px solid var(--gray-200);
}

.btn-danger {
  background: var(--danger);
  color: white;
}

.btn-text {
  background: transparent;
  color: var(--primary-orange);
  padding: 4px 8px;
}
```

### 3.2 表单控件

#### 输入框设计
```html
<div class="form-field">
  <label class="form-label">商户描述符</label>
  <input type="text" class="form-input" placeholder="请输入商户描述符">
  <div class="form-hint">2-50个字符，支持字母数字和常见符号</div>
</div>
```

```css
.form-field {
  margin-bottom: var(--spacing-md);
}

.form-label {
  display: block;
  margin-bottom: var(--spacing-sm);
  font-size: var(--font-size-base);
  font-weight: 500;
  color: var(--gray-700);
}

.form-input {
  width: 100%;
  padding: 12px 16px;
  border: 1px solid var(--gray-200);
  border-radius: var(--border-radius-md);
  font-size: var(--font-size-base);
  transition: border-color 0.2s ease;
}

.form-input:focus {
  outline: none;
  border-color: var(--primary-orange);
  box-shadow: 0 0 0 3px var(--primary-orange-pale);
}

.form-hint {
  margin-top: var(--spacing-xs);
  font-size: var(--font-size-small);
  color: var(--gray-400);
}
```

#### 选择器设计
```html
<!-- 下拉选择 -->
<div class="form-field">
  <label class="form-label">风险等级</label>
  <select class="form-select">
    <option value="">全部</option>
    <option value="HIGH">高风险</option>
    <option value="MEDIUM">中风险</option>
    <option value="LOW">低风险</option>
  </select>
</div>

<!-- 单选按钮 -->
<div class="form-field">
  <label class="form-label">处理动作</label>
  <div class="radio-group">
    <label class="radio-item">
      <input type="radio" name="action" value="confirm">
      <span class="radio-label">确认交易</span>
    </label>
    <label class="radio-item">
      <input type="radio" name="action" value="refund">
      <span class="radio-label">申请退款</span>
    </label>
  </div>
</div>
```

### 3.3 卡片设计

```html
<div class="card">
  <div class="card-header">
    <h3 class="card-title">预警详情</h3>
    <div class="card-actions">
      <button class="btn btn-text">导出</button>
    </div>
  </div>
  <div class="card-body">
    <div class="info-grid">
      <div class="info-item">
        <span class="info-label">预警ID</span>
        <span class="info-value">CHB_20241201_001</span>
      </div>
      <div class="info-item">
        <span class="info-label">风险等级</span>
        <span class="badge badge-danger">高风险</span>
      </div>
    </div>
  </div>
</div>
```

```css
.card {
  background: var(--bg-primary);
  border-radius: var(--border-radius-lg);
  box-shadow: var(--shadow-sm);
  border: 1px solid var(--gray-200);
  overflow: hidden;
}

.card-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: var(--card-padding);
  border-bottom: 1px solid var(--gray-200);
  background: var(--bg-secondary);
}

.card-title {
  margin: 0;
  font-size: var(--font-size-h4);
  font-weight: 600;
  color: var(--gray-700);
}

.card-body {
  padding: var(--card-padding);
}

.info-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: var(--spacing-md);
}

.info-item {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-xs);
}

.info-label {
  font-size: var(--font-size-small);
  color: var(--gray-400);
  font-weight: 500;
}

.info-value {
  font-size: var(--font-size-base);
  color: var(--gray-700);
  font-weight: 500;
}
```

### 3.4 标签与状态

```html
<!-- 状态标签 -->
<span class="badge badge-success">已处理</span>
<span class="badge badge-warning">待处理</span>
<span class="badge badge-danger">高风险</span>
<span class="badge badge-info">已报备</span>

<!-- 风险等级标签 -->
<span class="risk-badge risk-high">高风险</span>
<span class="risk-badge risk-medium">中风险</span>
<span class="risk-badge risk-low">低风险</span>
```

```css
.badge {
  display: inline-flex;
  align-items: center;
  padding: 4px 8px;
  border-radius: 12px;
  font-size: var(--font-size-small);
  font-weight: 500;
  line-height: 1;
}

.badge-success {
  background: var(--success-light);
  color: var(--success);
}

.badge-warning {
  background: var(--warning-light);
  color: var(--warning);
}

.badge-danger {
  background: var(--danger-light);
  color: var(--danger);
}

.badge-info {
  background: var(--info-light);
  color: var(--info);
}

.risk-badge {
  padding: 6px 12px;
  border-radius: var(--border-radius-md);
  font-weight: 600;
  font-size: var(--font-size-small);
}

.risk-high {
  background: var(--risk-high);
  color: white;
}

.risk-medium {
  background: var(--risk-medium);
  color: white;
}

.risk-low {
  background: var(--risk-low);
  color: white;
}
```

## 4. 页面布局设计

### 4.1 整体布局结构

```html
<div class="app-layout">
  <!-- 顶部导航栏 -->
  <header class="app-header">
    <div class="header-left">
      <div class="logo">
        <img src="/logo.svg" alt="拒付预警平台">
        <span class="logo-text">拒付预警平台</span>
      </div>
    </div>
    <div class="header-right">
      <div class="user-menu">
        <div class="user-avatar">
          <img src="/avatar.png" alt="用户头像">
        </div>
        <span class="user-name">张三</span>
        <div class="dropdown-menu">
          <a href="/profile">个人信息</a>
          <a href="/logout">退出登录</a>
        </div>
      </div>
    </div>
  </header>

  <!-- 侧边导航栏 -->
  <aside class="app-sidebar">
    <nav class="sidebar-nav">
      <a href="/dashboard" class="nav-item active">
        <svg class="nav-icon">...</svg>
        <span class="nav-text">概览</span>
      </a>
      <a href="/cards" class="nav-item">
        <svg class="nav-icon">...</svg>
        <span class="nav-text">卡片管理</span>
      </a>
      <a href="/alerts" class="nav-item">
        <svg class="nav-icon">...</svg>
        <span class="nav-text">预警中心</span>
      </a>
      <a href="/reports" class="nav-item">
        <svg class="nav-icon">...</svg>
        <span class="nav-text">数据报表</span>
      </a>
      <a href="/settings" class="nav-item">
        <svg class="nav-icon">...</svg>
        <span class="nav-text">系统设置</span>
      </a>
    </nav>
  </aside>

  <!-- 主内容区域 -->
  <main class="app-main">
    <div class="page-header">
      <h1 class="page-title">预警中心</h1>
      <div class="page-actions">
        <button class="btn btn-primary">新增卡片</button>
      </div>
    </div>
    <div class="page-content">
      <!-- 页面具体内容 -->
    </div>
  </main>
</div>
```

```css
.app-layout {
  display: grid;
  grid-template-areas: 
    "header header"
    "sidebar main";
  grid-template-columns: 260px 1fr;
  grid-template-rows: 64px 1fr;
  height: 100vh;
  background: var(--bg-secondary);
}

.app-header {
  grid-area: header;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 var(--spacing-lg);
  background: var(--bg-primary);
  border-bottom: 1px solid var(--gray-200);
  box-shadow: var(--shadow-sm);
}

.app-sidebar {
  grid-area: sidebar;
  background: var(--bg-primary);
  border-right: 1px solid var(--gray-200);
  padding: var(--spacing-lg) 0;
}

.app-main {
  grid-area: main;
  padding: var(--spacing-lg);
  overflow-y: auto;
}

/* 响应式设计 */
@media (max-width: 768px) {
  .app-layout {
    grid-template-areas: 
      "header"
      "main";
    grid-template-columns: 1fr;
  }
  
  .app-sidebar {
    display: none;
  }
}
```

### 4.2 页面头部设计

```css
.logo {
  display: flex;
  align-items: center;
  gap: var(--spacing-sm);
}

.logo img {
  width: 32px;
  height: 32px;
}

.logo-text {
  font-size: var(--font-size-large);
  font-weight: 600;
  color: var(--gray-700);
}

.user-menu {
  position: relative;
  display: flex;
  align-items: center;
  gap: var(--spacing-sm);
  cursor: pointer;
}

.user-avatar img {
  width: 36px;
  height: 36px;
  border-radius: 50%;
}

.page-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: var(--spacing-xl);
}

.page-title {
  margin: 0;
  font-size: var(--font-size-h2);
  font-weight: 600;
  color: var(--gray-700);
}
```

### 4.3 侧边导航设计

```css
.sidebar-nav {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-xs);
  padding: 0 var(--spacing-md);
}

.nav-item {
  display: flex;
  align-items: center;
  gap: var(--spacing-sm);
  padding: 12px var(--spacing-md);
  border-radius: var(--border-radius-md);
  color: var(--gray-600);
  text-decoration: none;
  transition: all 0.2s ease;
}

.nav-item:hover {
  background: var(--gray-100);
  color: var(--gray-700);
}

.nav-item.active {
  background: var(--primary-orange-pale);
  color: var(--primary-orange);
}

.nav-icon {
  width: 20px;
  height: 20px;
  fill: currentColor;
}

.nav-text {
  font-size: var(--font-size-base);
  font-weight: 500;
}
```

## 5. 具体页面设计

### 5.1 登录页面

```html
<div class="login-page">
  <div class="login-container">
    <div class="login-header">
      <div class="logo">
        <img src="/logo.svg" alt="Logo">
        <h1>拒付预警管理平台</h1>
      </div>
      <p class="login-subtitle">为商户提供专业的拒付预警服务</p>
    </div>
    
    <form class="login-form">
      <div class="form-field">
        <label class="form-label">邮箱/手机号</label>
        <input type="text" class="form-input" placeholder="请输入邮箱或手机号">
      </div>
      
      <div class="form-field">
        <label class="form-label">密码</label>
        <input type="password" class="form-input" placeholder="请输入密码">
      </div>
      
      <div class="form-options">
        <label class="checkbox-item">
          <input type="checkbox">
          <span>记住密码</span>
        </label>
        <a href="/forgot-password" class="link">忘记密码？</a>
      </div>
      
      <button type="submit" class="btn btn-primary btn-block">登录</button>
      
      <div class="form-footer">
        <span>还没有账户？</span>
        <a href="/register" class="link">立即注册</a>
      </div>
    </form>
  </div>
  
  <div class="login-illustration">
    <img src="/login-bg.svg" alt="Login Background">
  </div>
</div>
```

```css
.login-page {
  display: grid;
  grid-template-columns: 1fr 1fr;
  min-height: 100vh;
  background: linear-gradient(135deg, var(--primary-orange-pale) 0%, var(--bg-primary) 100%);
}

.login-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: var(--spacing-2xl);
  max-width: 400px;
  margin: 0 auto;
}

.login-header {
  text-align: center;
  margin-bottom: var(--spacing-2xl);
}

.login-header .logo {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: var(--spacing-md);
}

.login-header h1 {
  color: var(--gray-700);
  font-size: var(--font-size-h2);
  margin: 0;
}

.login-subtitle {
  color: var(--gray-500);
  margin-top: var(--spacing-sm);
}

.login-form {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-lg);
}

.form-options {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.btn-block {
  width: 100%;
  padding: 14px;
  font-size: var(--font-size-large);
}

.form-footer {
  text-align: center;
  color: var(--gray-500);
}

.login-illustration {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: var(--spacing-2xl);
  background: var(--primary-orange-pale);
}

/* 响应式设计 */
@media (max-width: 768px) {
  .login-page {
    grid-template-columns: 1fr;
  }
  
  .login-illustration {
    display: none;
  }
}
```

### 5.2 仪表板页面

```html
<div class="dashboard">
  <!-- 关键指标卡片 -->
  <div class="metrics-grid">
    <div class="metric-card">
      <div class="metric-icon metric-icon-orange">
        <svg>...</svg>
      </div>
      <div class="metric-content">
        <div class="metric-value">1,234</div>
        <div class="metric-label">今日预警</div>
        <div class="metric-change positive">+12.5%</div>
      </div>
    </div>
    
    <div class="metric-card">
      <div class="metric-icon metric-icon-blue">
        <svg>...</svg>
      </div>
      <div class="metric-content">
        <div class="metric-value">89.2%</div>
        <div class="metric-label">处理率</div>
        <div class="metric-change positive">+2.1%</div>
      </div>
    </div>
    
    <div class="metric-card">
      <div class="metric-icon metric-icon-green">
        <svg>...</svg>
      </div>
      <div class="metric-content">
        <div class="metric-value">156</div>
        <div class="metric-label">活跃商户</div>
        <div class="metric-change positive">+5</div>
      </div>
    </div>
    
    <div class="metric-card">
      <div class="metric-icon metric-icon-red">
        <svg>...</svg>
      </div>
      <div class="metric-content">
        <div class="metric-value">23</div>
        <div class="metric-label">高风险预警</div>
        <div class="metric-change negative">-8</div>
      </div>
    </div>
  </div>
  
  <!-- 图表区域 -->
  <div class="charts-grid">
    <div class="chart-card">
      <div class="card-header">
        <h3 class="card-title">预警趋势</h3>
        <div class="chart-filters">
          <button class="filter-btn active">7天</button>
          <button class="filter-btn">30天</button>
          <button class="filter-btn">90天</button>
        </div>
      </div>
      <div class="card-body">
        <div class="chart-container" id="alertTrendChart"></div>
      </div>
    </div>
    
    <div class="chart-card">
      <div class="card-header">
        <h3 class="card-title">风险等级分布</h3>
      </div>
      <div class="card-body">
        <div class="chart-container" id="riskDistributionChart"></div>
      </div>
    </div>
  </div>
  
  <!-- 最新预警列表 -->
  <div class="recent-alerts">
    <div class="card">
      <div class="card-header">
        <h3 class="card-title">最新预警</h3>
        <a href="/alerts" class="btn btn-text">查看全部</a>
      </div>
      <div class="card-body">
        <div class="alert-list">
          <div class="alert-item">
            <div class="alert-info">
              <div class="alert-id">CHB_20241201_001</div>
              <div class="alert-merchant">ABC商户</div>
            </div>
            <div class="alert-amount">$1,250.00</div>
            <div class="alert-risk">
              <span class="risk-badge risk-high">高风险</span>
            </div>
            <div class="alert-time">2分钟前</div>
            <div class="alert-actions">
              <button class="btn btn-text">处理</button>
            </div>
          </div>
          <!-- 更多预警项... -->
        </div>
      </div>
    </div>
  </div>
</div>
```

```css
.dashboard {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-xl);
}

.metrics-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: var(--spacing-lg);
}

.metric-card {
  display: flex;
  align-items: center;
  gap: var(--spacing-md);
  padding: var(--spacing-lg);
  background: var(--bg-primary);
  border-radius: var(--border-radius-lg);
  box-shadow: var(--shadow-sm);
  border: 1px solid var(--gray-200);
}

.metric-icon {
  width: 48px;
  height: 48px;
  border-radius: var(--border-radius-lg);
  display: flex;
  align-items: center;
  justify-content: center;
}

.metric-icon-orange { background: var(--primary-orange-pale); color: var(--primary-orange); }
.metric-icon-blue { background: var(--info-light); color: var(--info); }
.metric-icon-green { background: var(--success-light); color: var(--success); }
.metric-icon-red { background: var(--danger-light); color: var(--danger); }

.metric-content {
  flex: 1;
}

.metric-value {
  font-size: var(--font-size-h2);
  font-weight: 700;
  color: var(--gray-700);
  font-family: var(--font-family-number);
}

.metric-label {
  font-size: var(--font-size-base);
  color: var(--gray-500);
  margin-top: var(--spacing-xs);
}

.metric-change {
  font-size: var(--font-size-small);
  font-weight: 600;
  margin-top: var(--spacing-xs);
}

.metric-change.positive { color: var(--success); }
.metric-change.negative { color: var(--danger); }

.charts-grid {
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: var(--spacing-lg);
}

.chart-card {
  background: var(--bg-primary);
  border-radius: var(--border-radius-lg);
  box-shadow: var(--shadow-sm);
  border: 1px solid var(--gray-200);
}

.chart-filters {
  display: flex;
  gap: var(--spacing-xs);
}

.filter-btn {
  padding: 6px 12px;
  border: 1px solid var(--gray-200);
  background: var(--bg-primary);
  border-radius: var(--border-radius-sm);
  font-size: var(--font-size-small);
  cursor: pointer;
  transition: all 0.2s ease;
}

.filter-btn.active {
  background: var(--primary-orange);
  color: white;
  border-color: var(--primary-orange);
}

.chart-container {
  height: 300px;
  width: 100%;
}

.alert-list {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-sm);
}

.alert-item {
  display: grid;
  grid-template-columns: 2fr 1fr 100px 80px 80px;
  gap: var(--spacing-md);
  padding: var(--spacing-md);
  border-radius: var(--border-radius-md);
  border: 1px solid var(--gray-200);
  align-items: center;
}

.alert-id {
  font-weight: 600;
  color: var(--gray-700);
  font-family: var(--font-family-number);
}

.alert-merchant {
  font-size: var(--font-size-small);
  color: var(--gray-500);
  margin-top: 2px;
}

.alert-amount {
  font-weight: 600;
  color: var(--gray-700);
  font-family: var(--font-family-number);
}

.alert-time {
  font-size: var(--font-size-small);
  color: var(--gray-400);
}

/* 响应式设计 */
@media (max-width: 1024px) {
  .charts-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 768px) {
  .metrics-grid {
    grid-template-columns: 1fr;
  }
  
  .alert-item {
    grid-template-columns: 1fr;
    gap: var(--spacing-sm);
  }
}
```

### 5.3 预警列表页面

```html
<div class="alerts-page">
  <!-- 筛选栏 -->
  <div class="filters-bar">
    <div class="filters-left">
      <div class="filter-group">
        <label>时间范围</label>
        <select class="form-select">
          <option>今天</option>
          <option>最近7天</option>
          <option>最近30天</option>
          <option>自定义</option>
        </select>
      </div>
      
      <div class="filter-group">
        <label>处理状态</label>
        <select class="form-select">
          <option>全部</option>
          <option>待处理</option>
          <option>已处理</option>
          <option>已忽略</option>
        </select>
      </div>
      
      <div class="filter-group">
        <label>风险等级</label>
        <select class="form-select">
          <option>全部</option>
          <option>高风险</option>
          <option>中风险</option>
          <option>低风险</option>
        </select>
      </div>
      
      <div class="filter-group">
        <input type="text" class="form-input" placeholder="搜索预警ID或交易ID">
      </div>
    </div>
    
    <div class="filters-right">
      <button class="btn btn-secondary">重置</button>
      <button class="btn btn-primary">
        <svg class="btn-icon">...</svg>
        导出数据
      </button>
    </div>
  </div>
  
  <!-- 预警列表 -->
  <div class="alerts-table">
    <div class="table-header">
      <div class="table-actions">
        <div class="table-info">
          <span>共 1,234 条预警</span>
        </div>
        <div class="table-controls">
          <div class="pagination-size">
            <select class="form-select">
              <option>10条/页</option>
              <option>20条/页</option>
              <option>50条/页</option>
            </select>
          </div>
        </div>
      </div>
    </div>
    
    <div class="table-container">
      <table class="data-table">
        <thead>
          <tr>
            <th>
              <input type="checkbox" class="select-all">
            </th>
            <th>预警ID</th>
            <th>商户</th>
            <th>交易金额</th>
            <th>风险等级</th>
            <th>预警时间</th>
            <th>处理状态</th>
            <th>操作</th>
          </tr>
        </thead>
        <tbody>
          <tr class="table-row">
            <td>
              <input type="checkbox">
            </td>
            <td>
              <div class="alert-id-cell">
                <span class="alert-id">CHB_20241201_001</span>
                <span class="transaction-id">TXN_987654321</span>
              </div>
            </td>
            <td>
              <div class="merchant-cell">
                <span class="merchant-name">ABC商户</span>
                <span class="card-info">****1234</span>
              </div>
            </td>
            <td>
              <div class="amount-cell">
                <span class="amount">$1,250.00</span>
                <span class="currency">USD</span>
              </div>
            </td>
            <td>
              <span class="risk-badge risk-high">高风险</span>
            </td>
            <td>
              <div class="time-cell">
                <span class="time">2024-12-01 14:30:25</span>
                <span class="relative-time">2小时前</span>
              </div>
            </td>
            <td>
              <span class="badge badge-warning">待处理</span>
            </td>
            <td>
              <div class="action-buttons">
                <button class="btn btn-text">查看</button>
                <button class="btn btn-text">处理</button>
              </div>
            </td>
          </tr>
          <!-- 更多行... -->
        </tbody>
      </table>
    </div>
    
    <!-- 分页器 -->
    <div class="table-footer">
      <div class="pagination">
        <button class="pagination-btn" disabled>上一页</button>
        <div class="pagination-pages">
          <button class="pagination-page active">1</button>
          <button class="pagination-page">2</button>
          <button class="pagination-page">3</button>
          <span class="pagination-ellipsis">...</span>
          <button class="pagination-page">10</button>
        </div>
        <button class="pagination-btn">下一页</button>
      </div>
    </div>
  </div>
</div>
```

```css
.alerts-page {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-lg);
}

.filters-bar {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  gap: var(--spacing-lg);
  padding: var(--spacing-lg);
  background: var(--bg-primary);
  border-radius: var(--border-radius-lg);
  box-shadow: var(--shadow-sm);
  border: 1px solid var(--gray-200);
}

.filters-left {
  display: flex;
  gap: var(--spacing-lg);
  flex-wrap: wrap;
}

.filters-right {
  display: flex;
  gap: var(--spacing-sm);
}

.filter-group {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-xs);
  min-width: 120px;
}

.filter-group label {
  font-size: var(--font-size-small);
  font-weight: 500;
  color: var(--gray-600);
}

.alerts-table {
  background: var(--bg-primary);
  border-radius: var(--border-radius-lg);
  box-shadow: var(--shadow-sm);
  border: 1px solid var(--gray-200);
  overflow: hidden;
}

.table-header {
  padding: var(--spacing-lg);
  border-bottom: 1px solid var(--gray-200);
  background: var(--bg-secondary);
}

.table-actions {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.table-info {
  color: var(--gray-600);
  font-size: var(--font-size-base);
}

.data-table {
  width: 100%;
  border-collapse: collapse;
}

.data-table th {
  padding: var(--spacing-md);
  text-align: left;
  font-weight: 600;
  color: var(--gray-700);
  background: var(--bg-secondary);
  border-bottom: 1px solid var(--gray-200);
}

.data-table td {
  padding: var(--spacing-md);
  border-bottom: 1px solid var(--gray-200);
}

.table-row:hover {
  background: var(--bg-secondary);
}

.alert-id-cell {
  display: flex;
  flex-direction: column;
  gap: 2px;
}

.alert-id {
  font-weight: 600;
  color: var(--gray-700);
  font-family: var(--font-family-number);
}

.transaction-id {
  font-size: var(--font-size-small);
  color: var(--gray-400);
  font-family: var(--font-family-number);
}

.merchant-cell {
  display: flex;
  flex-direction: column;
  gap: 2px;
}

.merchant-name {
  font-weight: 500;
  color: var(--gray-700);
}

.card-info {
  font-size: var(--font-size-small);
  color: var(--gray-400);
  font-family: var(--font-family-number);
}

.amount-cell {
  display: flex;
  flex-direction: column;
  gap: 2px;
}

.amount {
  font-weight: 600;
  color: var(--gray-700);
  font-family: var(--font-family-number);
}

.currency {
  font-size: var(--font-size-small);
  color: var(--gray-400);
}

.time-cell {
  display: flex;
  flex-direction: column;
  gap: 2px;
}

.time {
  font-size: var(--font-size-small);
  color: var(--gray-600);
  font-family: var(--font-family-number);
}

.relative-time {
  font-size: var(--font-size-small);
  color: var(--gray-400);
}

.action-buttons {
  display: flex;
  gap: var(--spacing-xs);
}

.table-footer {
  padding: var(--spacing-lg);
  border-top: 1px solid var(--gray-200);
  background: var(--bg-secondary);
}

.pagination {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: var(--spacing-sm);
}

.pagination-btn {
  padding: 8px 16px;
  border: 1px solid var(--gray-200);
  background: var(--bg-primary);
  border-radius: var(--border-radius-md);
  cursor: pointer;
  transition: all 0.2s ease;
}

.pagination-btn:hover:not(:disabled) {
  background: var(--gray-100);
}

.pagination-btn:disabled {
  opacity: 0.5;
  cursor: not-allowed;
}

.pagination-pages {
  display: flex;
  gap: var(--spacing-xs);
}

.pagination-page {
  width: 36px;
  height: 36px;
  border: 1px solid var(--gray-200);
  background: var(--bg-primary);
  border-radius: var(--border-radius-md);
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.2s ease;
}

.pagination-page.active {
  background: var(--primary-orange);
  color: white;
  border-color: var(--primary-orange);
}

.pagination-page:hover:not(.active) {
  background: var(--gray-100);
}

/* 响应式设计 */
@media (max-width: 768px) {
  .filters-bar {
    flex-direction: column;
    align-items: stretch;
  }
  
  .filters-left {
    flex-direction: column;
    gap: var(--spacing-md);
  }
  
  .table-container {
    overflow-x: auto;
  }
  
  .data-table {
    min-width: 800px;
  }
}
```

### 5.4 预警详情页面

```html
<div class="alert-detail">
  <!-- 面包屑导航 -->
  <div class="breadcrumb">
    <a href="/alerts">预警中心</a>
    <span class="breadcrumb-separator">/</span>
    <span class="breadcrumb-current">预警详情</span>
  </div>
  
  <!-- 预警基本信息 -->
  <div class="alert-summary">
    <div class="alert-header">
      <div class="alert-title">
        <h1>预警详情</h1>
        <span class="alert-id">CHB_20241201_001</span>
      </div>
      <div class="alert-status">
        <span class="risk-badge risk-high">高风险</span>
        <span class="badge badge-warning">待处理</span>
      </div>
    </div>
    
    <div class="alert-meta">
      <div class="meta-item">
        <span class="meta-label">预警时间</span>
        <span class="meta-value">2024-12-01 14:30:25</span>
      </div>
      <div class="meta-item">
        <span class="meta-label">交易金额</span>
        <span class="meta-value">$1,250.00 USD</span>
      </div>
      <div class="meta-item">
        <span class="meta-label">商户名称</span>
        <span class="meta-value">ABC商户</span>
      </div>
      <div class="meta-item">
        <span class="meta-label">最后更新</span>
        <span class="meta-value">2小时前</span>
      </div>
    </div>
  </div>
  
  <!-- 详细信息区域 -->
  <div class="detail-content">
    <div class="detail-left">
      <!-- 交易信息 -->
      <div class="card">
        <div class="card-header">
          <h3 class="card-title">交易信息</h3>
        </div>
        <div class="card-body">
          <div class="info-grid">
            <div class="info-item">
              <span class="info-label">交易ID</span>
              <span class="info-value">TXN_987654321</span>
            </div>
            <div class="info-item">
              <span class="info-label">交易金额</span>
              <span class="info-value">$1,250.00</span>
            </div>
            <div class="info-item">
              <span class="info-label">货币类型</span>
              <span class="info-value">USD</span>
            </div>
            <div class="info-item">
              <span class="info-label">交易时间</span>
              <span class="info-value">2024-12-01 12:15:30</span>
            </div>
          </div>
        </div>
      </div>
      
      <!-- 卡片信息 -->
      <div class="card">
        <div class="card-header">
          <h3 class="card-title">卡片信息</h3>
        </div>
        <div class="card-body">
          <div class="info-grid">
            <div class="info-item">
              <span class="info-label">卡片BIN</span>
              <span class="info-value">****1234</span>
            </div>
            <div class="info-item">
              <span class="info-label">卡片类型</span>
              <span class="info-value">Visa Credit</span>
            </div>
            <div class="info-item">
              <span class="info-label">发卡行</span>
              <span class="info-value">Chase Bank</span>
            </div>
            <div class="info-item">
              <span class="info-label">持卡人</span>
              <span class="info-value">John D****</span>
            </div>
          </div>
        </div>
      </div>
      
      <!-- 风险信息 -->
      <div class="card">
        <div class="card-header">
          <h3 class="card-title">风险信息</h3>
        </div>
        <div class="card-body">
          <div class="risk-details">
            <div class="risk-score">
              <div class="score-circle">
                <svg class="score-progress">
                  <circle cx="50" cy="50" r="40" stroke="var(--gray-200)" stroke-width="8" fill="none"/>
                  <circle cx="50" cy="50" r="40" stroke="var(--danger)" stroke-width="8" fill="none" 
                          stroke-dasharray="251.2" stroke-dashoffset="75.36"/>
                </svg>
                <div class="score-text">
                  <span class="score-value">85</span>
                  <span class="score-label">风险评分</span>
                </div>
              </div>
            </div>
            
            <div class="risk-factors">
              <h4>风险因素</h4>
              <ul class="risk-list">
                <li class="risk-factor">
                  <span class="factor-icon high">⚠️</span>
                  <span class="factor-text">异常交易模式</span>
                </li>
                <li class="risk-factor">
                  <span class="factor-icon medium">⚡</span>
                  <span class="factor-text">频繁小额交易</span>
                </li>
                <li class="risk-factor">
                  <span class="factor-icon low">📍</span>
                  <span class="factor-text">地理位置异常</span>
                </li>
              </ul>
            </div>
          </div>
          
          <div class="recommendations">
            <h4>建议处理措施</h4>
            <div class="recommendation-list">
              <div class="recommendation-item">
                <div class="recommendation-icon">💡</div>
                <div class="recommendation-text">
                  建议立即联系持卡人确认交易真实性
                </div>
              </div>
              <div class="recommendation-item">
                <div class="recommendation-icon">🔍</div>
                <div class="recommendation-text">
                  审查最近30天内的相关交易记录
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    
    <!-- 处理操作区域 -->
    <div class="detail-right">
      <div class="card action-card">
        <div class="card-header">
          <h3 class="card-title">处理预警</h3>
        </div>
        <div class="card-body">
          <form class="process-form">
            <div class="form-field">
              <label class="form-label">处理动作 <span class="required">*</span></label>
              <div class="radio-group">
                <label class="radio-item">
                  <input type="radio" name="action" value="confirm">
                  <span class="radio-label">确认交易</span>
                  <span class="radio-desc">交易合法，无需处理</span>
                </label>
                <label class="radio-item">
                  <input type="radio" name="action" value="refund">
                  <span class="radio-label">申请退款</span>
                  <span class="radio-desc">主动退款给客户</span>
                </label>
                <label class="radio-item">
                  <input type="radio" name="action" value="dispute">
                  <span class="radio-label">争议处理</span>
                  <span class="radio-desc">提供证据材料进行争议</span>
                </label>
                <label class="radio-item">
                  <input type="radio" name="action" value="fraud">
                  <span class="radio-label">标记欺诈</span>
                  <span class="radio-desc">确认为欺诈交易</span>
                </label>
                <label class="radio-item">
                  <input type="radio" name="action" value="ignore">
                  <span class="radio-label">忽略预警</span>
                  <span class="radio-desc">不进行任何处理</span>
                </label>
              </div>
            </div>
            
            <div class="form-field">
              <label class="form-label">处理原因 <span class="required">*</span></label>
              <textarea class="form-textarea" placeholder="请详细说明处理原因..." rows="4"></textarea>
            </div>
            
            <div class="form-field refund-amount" style="display: none;">
              <label class="form-label">退款金额</label>
              <div class="amount-input">
                <input type="number" class="form-input" placeholder="0.00" max="1250.00">
                <span class="currency-suffix">USD</span>
              </div>
              <div class="form-hint">最大退款金额: $1,250.00</div>
            </div>
            
            <div class="form-field">
              <label class="form-label">证据文件</label>
              <div class="file-upload">
                <div class="upload-area">
                  <svg class="upload-icon">...</svg>
                  <p>点击上传或拖拽文件到此处</p>
                  <p class="upload-hint">支持 PDF、JPG、PNG 格式，单文件不超过 10MB</p>
                </div>
                <input type="file" class="file-input" multiple accept=".pdf,.jpg,.jpeg,.png">
              </div>
            </div>
            
            <div class="form-field">
              <label class="form-label">备注说明</label>
              <textarea class="form-textarea" placeholder="可选的补充说明..." rows="3"></textarea>
            </div>
            
            <div class="form-actions">
              <button type="button" class="btn btn-secondary">取消</button>
              <button type="submit" class="btn btn-primary">提交处理</button>
            </div>
          </form>
        </div>
      </div>
      
      <!-- 处理历史 -->
      <div class="card">
        <div class="card-header">
          <h3 class="card-title">处理历史</h3>
        </div>
        <div class="card-body">
          <div class="timeline">
            <div class="timeline-item">
              <div class="timeline-marker received"></div>
              <div class="timeline-content">
                <div class="timeline-title">预警创建</div>
                <div class="timeline-desc">系统接收到拒付预警</div>
                <div class="timeline-time">2024-12-01 14:30:25</div>
              </div>
            </div>
            <div class="timeline-item">
              <div class="timeline-marker notified"></div>
              <div class="timeline-content">
                <div class="timeline-title">邮件通知</div>
                <div class="timeline-desc">已发送邮件通知到 admin@abc.com</div>
                <div class="timeline-time">2024-12-01 14:31:02</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
```

```css
.alert-detail {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-lg);
}

.breadcrumb {
  display: flex;
  align-items: center;
  gap: var(--spacing-sm);
  font-size: var(--font-size-base);
  color: var(--gray-500);
}

.breadcrumb a {
  color: var(--primary-orange);
  text-decoration: none;
}

.breadcrumb-separator {
  color: var(--gray-300);
}

.breadcrumb-current {
  color: var(--gray-700);
  font-weight: 500;
}

.alert-summary {
  background: var(--bg-primary);
  border-radius: var(--border-radius-lg);
  box-shadow: var(--shadow-sm);
  border: 1px solid var(--gray-200);
  padding: var(--spacing-xl);
}

.alert-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: var(--spacing-lg);
}

.alert-title {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-xs);
}

.alert-title h1 {
  margin: 0;
  font-size: var(--font-size-h2);
  color: var(--gray-700);
}

.alert-id {
  font-family: var(--font-family-number);
  font-size: var(--font-size-large);
  color: var(--gray-500);
  font-weight: 500;
}

.alert-status {
  display: flex;
  gap: var(--spacing-sm);
  align-items: center;
}

.alert-meta {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: var(--spacing-lg);
}

.meta-item {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-xs);
}

.meta-label {
  font-size: var(--font-size-small);
  color: var(--gray-400);
  font-weight: 500;
}

.meta-value {
  font-size: var(--font-size-base);
  color: var(--gray-700);
  font-weight: 600;
}

.detail-content {
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: var(--spacing-xl);
}

.detail-left {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-lg);
}

.detail-right {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-lg);
}

.action-card {
  position: sticky;
  top: var(--spacing-lg);
}

.risk-details {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: var(--spacing-xl);
  margin-bottom: var(--spacing-lg);
}

.risk-score {
  display: flex;
  justify-content: center;
}

.score-circle {
  position: relative;
  width: 100px;
  height: 100px;
}

.score-progress {
  width: 100%;
  height: 100%;
  transform: rotate(-90deg);
}

.score-text {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
}

.score-value {
  display: block;
  font-size: var(--font-size-h2);
  font-weight: 700;
  color: var(--danger);
  font-family: var(--font-family-number);
}

.score-label {
  display: block;
  font-size: var(--font-size-small);
  color: var(--gray-500);
  margin-top: var(--spacing-xs);
}

.risk-factors h4 {
  margin: 0 0 var(--spacing-md) 0;
  font-size: var(--font-size-base);
  color: var(--gray-700);
}

.risk-list {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-direction: column;
  gap: var(--spacing-sm);
}

.risk-factor {
  display: flex;
  align-items: center;
  gap: var(--spacing-sm);
}

.factor-icon {
  font-size: 16px;
}

.factor-text {
  font-size: var(--font-size-base);
  color: var(--gray-600);
}

.recommendations {
  grid-column: 1 / -1;
}

.recommendations h4 {
  margin: 0 0 var(--spacing-md) 0;
  font-size: var(--font-size-base);
  color: var(--gray-700);
}

.recommendation-list {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-md);
}

.recommendation-item {
  display: flex;
  gap: var(--spacing-sm);
  padding: var(--spacing-md);
  background: var(--bg-secondary);
  border-radius: var(--border-radius-md);
  border-left: 4px solid var(--primary-orange);
}

.recommendation-icon {
  font-size: 18px;
  flex-shrink: 0;
}

.recommendation-text {
  font-size: var(--font-size-base);
  color: var(--gray-600);
  line-height: var(--line-height-base);
}

.process-form {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-lg);
}

.radio-group {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-md);
}

.radio-item {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-xs);
  padding: var(--spacing-md);
  border: 1px solid var(--gray-200);
  border-radius: var(--border-radius-md);
  cursor: pointer;
  transition: all 0.2s ease;
}

.radio-item:hover {
  border-color: var(--primary-orange);
  background: var(--primary-orange-pale);
}

.radio-item input[type="radio"] {
  position: absolute;
  opacity: 0;
}

.radio-item input[type="radio"]:checked + .radio-label {
  color: var(--primary-orange);
  font-weight: 600;
}

.radio-item:has(input[type="radio"]:checked) {
  border-color: var(--primary-orange);
  background: var(--primary-orange-pale);
}

.radio-label {
  font-size: var(--font-size-base);
  font-weight: 500;
  color: var(--gray-700);
  position: relative;
  padding-left: 24px;
}

.radio-label::before {
  content: '';
  position: absolute;
  left: 0;
  top: 2px;
  width: 16px;
  height: 16px;
  border: 2px solid var(--gray-300);
  border-radius: 50%;
  background: white;
}

.radio-item input[type="radio"]:checked + .radio-label::before {
  border-color: var(--primary-orange);
}

.radio-item input[type="radio"]:checked + .radio-label::after {
  content: '';
  position: absolute;
  left: 4px;
  top: 6px;
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background: var(--primary-orange);
}

.radio-desc {
  font-size: var(--font-size-small);
  color: var(--gray-500);
  padding-left: 24px;
}

.form-textarea {
  width: 100%;
  padding: 12px 16px;
  border: 1px solid var(--gray-200);
  border-radius: var(--border-radius-md);
  font-size: var(--font-size-base);
  font-family: inherit;
  resize: vertical;
  min-height: 80px;
}

.form-textarea:focus {
  outline: none;
  border-color: var(--primary-orange);
  box-shadow: 0 0 0 3px var(--primary-orange-pale);
}

.amount-input {
  position: relative;
  display: flex;
  align-items: center;
}

.amount-input input {
  padding-right: 50px;
}

.currency-suffix {
  position: absolute;
  right: 16px;
  color: var(--gray-500);
  font-size: var(--font-size-base);
  pointer-events: none;
}

.file-upload {
  border: 2px dashed var(--gray-200);
  border-radius: var(--border-radius-md);
  transition: border-color 0.2s ease;
}

.file-upload:hover {
  border-color: var(--primary-orange);
}

.upload-area {
  padding: var(--spacing-xl);
  text-align: center;
  cursor: pointer;
}

.upload-icon {
  width: 48px;
  height: 48px;
  color: var(--gray-400);
  margin-bottom: var(--spacing-md);
}

.upload-area p {
  margin: var(--spacing-sm) 0;
  color: var(--gray-600);
}

.upload-hint {
  font-size: var(--font-size-small);
  color: var(--gray-400);
}

.file-input {
  display: none;
}

.form-actions {
  display: flex;
  gap: var(--spacing-sm);
  justify-content: flex-end;
  padding-top: var(--spacing-lg);
  border-top: 1px solid var(--gray-200);
}

.timeline {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-lg);
}

.timeline-item {
  display: flex;
  gap: var(--spacing-md);
  position: relative;
}

.timeline-item:not(:last-child)::after {
  content: '';
  position: absolute;
  left: 8px;
  top: 24px;
  bottom: -24px;
  width: 2px;
  background: var(--gray-200);
}

.timeline-marker {
  width: 16px;
  height: 16px;
  border-radius: 50%;
  flex-shrink: 0;
  margin-top: 2px;
}

.timeline-marker.received { background: var(--info); }
.timeline-marker.notified { background: var(--success); }
.timeline-marker.processed { background: var(--primary-orange); }

.timeline-content {
  flex: 1;
}

.timeline-title {
  font-weight: 600;
  color: var(--gray-700);
  margin-bottom: var(--spacing-xs);
}

.timeline-desc {
  font-size: var(--font-size-base);
  color: var(--gray-600);
  margin-bottom: var(--spacing-xs);
}

.timeline-time {
  font-size: var(--font-size-small);
  color: var(--gray-400);
  font-family: var(--font-family-number);
}

/* 响应式设计 */
@media (max-width: 1024px) {
  .detail-content {
    grid-template-columns: 1fr;
  }
  
  .action-card {
    position: static;
  }
  
  .risk-details {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 768px) {
  .alert-header {
    flex-direction: column;
    gap: var(--spacing-md);
    align-items: flex-start;
  }
  
  .alert-meta {
    grid-template-columns: 1fr;
  }
  
  .form-actions {
    justify-content: stretch;
  }
  
  .form-actions .btn {
    flex: 1;
  }
}
```

## 6. 图表组件设计

### 6.1 图表容器样式

```css
.chart-wrapper {
  background: var(--bg-primary);
  border-radius: var(--border-radius-lg);
  box-shadow: var(--shadow-sm);
  border: 1px solid var(--gray-200);
  padding: var(--spacing-lg);
}

.chart-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: var(--spacing-lg);
}

.chart-title {
  font-size: var(--font-size-h4);
  font-weight: 600;
  color: var(--gray-700);
  margin: 0;
}

.chart-controls {
  display: flex;
  gap: var(--spacing-sm);
}

.chart-container {
  position: relative;
  height: 400px;
  width: 100%;
}

.chart-legend {
  display: flex;
  justify-content: center;
  gap: var(--spacing-lg);
  margin-top: var(--spacing-md);
  flex-wrap: wrap;
}

.legend-item {
  display: flex;
  align-items: center;
  gap: var(--spacing-xs);
  font-size: var(--font-size-small);
  color: var(--gray-600);
}

.legend-color {
  width: 12px;
  height: 12px;
  border-radius: 2px;
}
```

### 6.2 图表色彩主题

```javascript
// 图表颜色配置
const chartColors = {
  primary: ['#FF6B35', '#FF8659', '#FFA07A', '#FFB89A', '#FFC9B1'],
  risk: {
    high: '#DC2626',
    medium: '#F59E0B', 
    low: '#16A34A'
  },
  status: {
    pending: '#F59E0B',
    processed: '#22C55E',
    ignored: '#6B7280'
  },
  gradients: {
    orange: 'linear-gradient(135deg, #FF6B35 0%, #FF8659 100%)',
    blue: 'linear-gradient(135deg, #3B82F6 0%, #60A5FA 100%)',
    green: 'linear-gradient(135deg, #22C55E 0%, #4ADE80 100%)',
    red: 'linear-gradient(135deg, #EF4444 0%, #F87171 100%)'
  }
};
```

## 7. 响应式设计

### 7.1 断点定义

```css
/* 断点定义 */
:root {
  --breakpoint-sm: 640px;
  --breakpoint-md: 768px;
  --breakpoint-lg: 1024px;
  --breakpoint-xl: 1280px;
  --breakpoint-2xl: 1536px;
}

/* 响应式 Mixins */
@media (max-width: 640px) {
  /* 小屏幕样式 */
  .container {
    padding: var(--spacing-md);
  }
  
  .btn {
    padding: 12px 16px;
    font-size: var(--font-size-large);
  }
  
  .form-input {
    padding: 14px 16px;
    font-size: var(--font-size-large);
  }
}

@media (max-width: 768px) {
  /* 平板样式 */
  .app-layout {
    grid-template-areas: 
      "header"
      "main";
    grid-template-columns: 1fr;
  }
  
  .sidebar-toggle {
    display: block;
  }
  
  .metrics-grid {
    grid-template-columns: 1fr;
  }
  
  .charts-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 1024px) {
  /* 小屏笔记本样式 */
  .detail-content {
    grid-template-columns: 1fr;
  }
  
  .table-container {
    overflow-x: auto;
  }
}
```

### 7.2 移动端优化

```css
/* 移动端触摸优化 */
@media (hover: none) and (pointer: coarse) {
  .btn {
    min-height: 44px;
    min-width: 44px;
  }
  
  .nav-item {
    min-height: 48px;
  }
  
  .table-row {
    min-height: 56px;
  }
  
  .form-input,
  .form-select {
    min-height: 44px;
  }
}

/* 移动端导航 */
.mobile-nav {
  display: none;
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  background: var(--bg-primary);
  border-top: 1px solid var(--gray-200);
  box-shadow: 0 -4px 6px -1px rgba(0, 0, 0, 0.1);
  z-index: 100;
}

@media (max-width: 768px) {
  .mobile-nav {
    display: flex;
  }
  
  .app-main {
    padding-bottom: 80px;
  }
}

.mobile-nav-list {
  display: flex;
  width: 100%;
}

.mobile-nav-item {
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: var(--spacing-xs);
  padding: var(--spacing-sm);
  color: var(--gray-500);
  text-decoration: none;
  transition: color 0.2s ease;
}

.mobile-nav-item.active {
  color: var(--primary-orange);
}

.mobile-nav-icon {
  width: 24px;
  height: 24px;
  fill: currentColor;
}

.mobile-nav-text {
  font-size: var(--font-size-xs);
  font-weight: 500;
}
```

## 8. 动画与交互

### 8.1 过渡动画

```css
/* 全局过渡 */
* {
  transition: color 0.2s ease, background-color 0.2s ease, border-color 0.2s ease, 
              box-shadow 0.2s ease, transform 0.2s ease, opacity 0.2s ease;
}

/* 页面加载动画 */
.page-loader {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: var(--bg-primary);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 9999;
}

.loader-spinner {
  width: 40px;
  height: 40px;
  border: 4px solid var(--gray-200);
  border-top-color: var(--primary-orange);
  border-radius: 50%;
  animation: spin 1s linear infinite;
}

@keyframes spin {
  to { transform: rotate(360deg); }
}

/* 卡片悬停效果 */
.card {
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.card:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow-lg);
}

/* 按钮点击效果 */
.btn {
  position: relative;
  overflow: hidden;
}

.btn::before {
  content: '';
  position: absolute;
  top: 50%;
  left: 50%;
  width: 0;
  height: 0;
  border-radius: 50%;
  background: rgba(255, 255, 255, 0.3);
  transition: width 0.3s ease, height 0.3s ease;
  transform: translate(-50%, -50%);
}

.btn:active::before {
  width: 200px;
  height: 200px;
}

/* 表单焦点动画 */
.form-input,
.form-select,
.form-textarea {
  transition: border-color 0.2s ease, box-shadow 0.2s ease;
}

.form-input:focus,
.form-select:focus,
.form-textarea:focus {
  transform: none;
  animation: focusGlow 0.3s ease;
}

@keyframes focusGlow {
  0% { box-shadow: 0 0 0 0 var(--primary-orange-pale); }
  50% { box-shadow: 0 0 0 6px var(--primary-orange-pale); }
  100% { box-shadow: 0 0 0 3px var(--primary-orange-pale); }
}

/* 数据加载骨架屏 */
.skeleton {
  background: linear-gradient(90deg, var(--gray-200) 25%, var(--gray-100) 50%, var(--gray-200) 75%);
  background-size: 200% 100%;
  animation: loading 1.5s infinite;
}

@keyframes loading {
  0% { background-position: 200% 0; }
  100% { background-position: -200% 0; }
}

.skeleton-text {
  height: 16px;
  border-radius: 4px;
  margin-bottom: 8px;
}

.skeleton-title {
  height: 24px;
  border-radius: 4px;
  width: 60%;
  margin-bottom: 12px;
}

.skeleton-avatar {
  width: 40px;
  height: 40px;
  border-radius: 50%;
}
```

### 8.2 微交互效果

```css
/* 成功提示动画 */
.toast {
  position: fixed;
  top: 20px;
  right: 20px;
  background: var(--bg-primary);
  border-radius: var(--border-radius-lg);
  box-shadow: var(--shadow-xl);
  border: 1px solid var(--gray-200);
  padding: var(--spacing-md) var(--spacing-lg);
  display: flex;
  align-items: center;
  gap: var(--spacing-sm);
  z-index: 1000;
  transform: translateX(100%);
  animation: slideIn 0.3s ease forwards;
}

@keyframes slideIn {
  to { transform: translateX(0); }
}

.toast.success {
  border-left: 4px solid var(--success);
}

.toast.error {
  border-left: 4px solid var(--danger);
}

.toast.warning {
  border-left: 4px solid var(--warning);
}

/* 数字计数动画 */
.counter {
  font-family: var(--font-family-number);
}

.counter.animate {
  animation: countUp 0.8s ease;
}

@keyframes countUp {
  from { transform: translateY(20px); opacity: 0; }
  to { transform: translateY(0); opacity: 1; }
}

/* 进度条动画 */
.progress-bar {
  width: 100%;
  height: 8px;
  background: var(--gray-200);
  border-radius: 4px;
  overflow: hidden;
}

.progress-fill {
  height: 100%;
  background: linear-gradient(90deg, var(--primary-orange), var(--primary-orange-light));
  border-radius: 4px;
  transition: width 0.8s ease;
  position: relative;
}

.progress-fill::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
  animation: shimmer 2s infinite;
}

@keyframes shimmer {
  0% { transform: translateX(-100%); }
  100% { transform: translateX(100%); }
}
```

## 9. 可访问性设计

### 9.1 键盘导航

```css
/* 焦点样式 */
*:focus {
  outline: 2px solid var(--primary-orange);
  outline-offset: 2px;
}

/* 跳过链接 */
.skip-link {
  position: absolute;
  top: -40px;
  left: 6px;
  background: var(--primary-orange);
  color: white;
  padding: 8px;
  text-decoration: none;
  border-radius: 4px;
  transition: top 0.3s ease;
}

.skip-link:focus {
  top: 6px;
}

/* 键盘导航指示 */
.keyboard-navigation .nav-item:focus,
.keyboard-navigation .btn:focus,
.keyboard-navigation .form-input:focus {
  box-shadow: 0 0 0 3px var(--primary-orange-pale);
}
```

### 9.2 屏幕阅读器支持

```html
<!-- ARIA 标签示例 -->
<button class="btn btn-primary" aria-describedby="btn-help">
  处理预警
</button>
<div id="btn-help" class="sr-only">
  点击此按钮开始处理当前预警
</div>

<!-- 表格可访问性 -->
<table role="table" aria-label="预警列表">
  <caption class="sr-only">
    包含 1,234 条预警记录的表格，可按列排序
  </caption>
  <thead>
    <tr role="row">
      <th role="columnheader" aria-sort="none">
        <button class="sort-btn">预警ID</button>
      </th>
      <!-- 更多列... -->
    </tr>
  </thead>
</table>

<!-- 状态更新 -->
<div aria-live="polite" aria-atomic="true" class="sr-only" id="status-update">
  <!-- 动态状态更新内容 -->
</div>
```

```css
/* 屏幕阅读器专用样式 */
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border: 0;
}

/* 高对比度模式支持 */
@media (prefers-contrast: high) {
  :root {
    --gray-200: #000000;
    --gray-600: #000000;
    --primary-orange: #000000;
    --bg-primary: #ffffff;
  }
  
  .btn {
    border: 2px solid currentColor;
  }
}

/* 减少动画偏好 */
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
```

## 10. 性能优化

### 10.1 CSS 优化

```css
/* 关键路径CSS优化 */
.critical {
  /* 首屏关键样式内联 */
  font-family: var(--font-family-base);
  line-height: var(--line-height-base);
  color: var(--gray-700);
}

/* 字体预加载 */
@font-face {
  font-family: 'PingFang SC';
  font-display: swap;
  src: local('PingFang SC Regular');
}

/* 图片优化 */
.image-container {
  position: relative;
  overflow: hidden;
}

.image-lazy {
  opacity: 0;
  transition: opacity 0.3s ease;
}

.image-lazy.loaded {
  opacity: 1;
}

/* GPU 加速 */
.gpu-accelerated {
  transform: translateZ(0);
  will-change: transform, opacity;
}

/* 虚拟滚动容器 */
.virtual-scroll {
  height: 400px;
  overflow-y: auto;
  position: relative;
}

.virtual-item {
  position: absolute;
  width: 100%;
  left: 0;
}
```

### 10.2 JavaScript 性能

```javascript
// 防抖和节流
const debounce = (func, wait) => {
  let timeout;
  return function executedFunction(...args) {
    const later = () => {
      clearTimeout(timeout);
      func(...args);
    };
    clearTimeout(timeout);
    timeout = setTimeout(later, wait);
  };
};

// 虚拟滚动实现
class VirtualScroll {
  constructor(container, itemHeight, renderItem) {
    this.container = container;
    this.itemHeight = itemHeight;
    this.renderItem = renderItem;
    this.visibleStart = 0;
    this.visibleEnd = 0;
    this.init();
  }
  
  init() {
    this.container.addEventListener('scroll', 
      debounce(() => this.updateVisibleItems(), 16)
    );
  }
  
  updateVisibleItems() {
    const scrollTop = this.container.scrollTop;
    const containerHeight = this.container.clientHeight;
    
    this.visibleStart = Math.floor(scrollTop / this.itemHeight);
    this.visibleEnd = Math.min(
      this.visibleStart + Math.ceil(containerHeight / this.itemHeight) + 1,
      this.data.length
    );
    
    this.render();
  }
}

// 图片懒加载
const imageObserver = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      const img = entry.target;
      img.src = img.dataset.src;
      img.classList.add('loaded');
      imageObserver.unobserve(img);
    }
  });
});

document.querySelectorAll('.image-lazy').forEach(img => {
  imageObserver.observe(img);
});
```

---

这份UI设计规范提供了完整的设计系统，包括颜色、字体、组件、布局、页面设计等各个方面，确保整个平台具有一致的视觉风格和良好的用户体验。设计采用现代扁平化风格，以橙色为主色调，支持响应式设计，适配各种设备屏幕。