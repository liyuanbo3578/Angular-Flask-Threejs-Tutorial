这是一个基于Angular前端框架、Flask后端API和Three.js三维图形库的现代化Web应用程序。项目结合了动态数据交互与三维可视化，为用户提供丰富的交互体验和视觉效果。

## 🌟 功能特点

-   **三维可视化**: 使用Three.js创建交互式3D场景和对象
    
-   **动态数据交互**: Angular前端与Flask后端实时数据通信
    
-   **响应式设计**: 适配各种屏幕尺寸和设备
    
-   **模块化架构**: 清晰的前后端分离设计
    
-   **现代化UI**: 直观美观的用户界面
    

## 🛠 技术栈

### 前端 (Angular)

-   **Angular 15+**: 前端框架
    
-   **TypeScript**: 编程语言
    
-   **Three.js**: 3D图形库
    
-   **RxJS**: 响应式编程
    
-   **Angular Material**: UI组件库
    

### 后端 (Flask)

-   **Flask 2.0+**: Python Web框架
    
-   **Flask-CORS**: 跨域资源共享
    
-   **Flask-RESTful**: RESTful API支持
    
-   **SQLAlchemy**: 数据库ORM (可选)
    

### 开发工具

-   **Node.js 18+**: JavaScript运行时
    
-   **Python 3.8+**: Python环境
    
-   **npm/yarn**: 包管理器
    
-   **Git**: 版本控制
    

## 🚀 快速开始

### 前置要求

1.  **Node.js 18+** 和 **npm/yarn**
    
2.  **Python 3.8+** 和 **pip**
    
3.  **Git** (用于版本控制)
    

### 安装步骤

#### 1. 克隆项目

bash

git clone <repository-url>
cd three-angular-flask-app

#### 2. 设置后端环境

bash

# 进入后端目录
cd backend

# 创建虚拟环境（推荐）
python -m venv venv

# 激活虚拟环境
# Windows:
venv\Scripts\activate
# Mac/Linux:
source venv/bin/activate

# 安装依赖
pip install -r requirements.txt

#### 3. 设置前端环境

bash

# 返回项目根目录
cd ../frontend

# 安装依赖
npm install
# 或使用yarn
yarn install

#### 4. 配置环境变量

**后端配置** (`backend/.env`):

env

FLASK_APP=run.py
FLASK_ENV=development
SECRET_KEY=your-secret-key
DATABASE_URL=sqlite:///app.db  # 或使用其他数据库

**前端配置** (`frontend/src/environments/environment.ts`):

typescript

export const environment = {
  production: false,
  apiUrl: 'http://localhost:5000/api'
};

### 启动应用

#### 启动后端服务

bash

cd backend
python run.py
# 服务运行在 http://localhost:5000

#### 启动前端服务

bash

cd frontend
ng serve
# 应用运行在 http://localhost:4200

#### 同时启动前后端（开发模式）

bash

# 项目根目录下
npm run dev
# 需要先在package.json中配置脚本

## 📖 使用指南

### 开发工作流

1.  **创建新的Three.js组件**:
    

bash

cd frontend
ng generate component three-scene/new-component

2.  **添加新的API端点**:
    
    -   在 `backend/app/routes/` 中创建新路由模块
        
    -   在 `backend/app/__init__.py` 中注册路由
        
3.  **添加前端服务**:
    

bash

cd frontend
ng generate service services/new-service

### Three.js集成示例

查看 `frontend/src/app/components/three-scene/` 中的示例组件了解如何：

-   创建3D场景
    
-   添加几何体、材质和光源
    
-   实现用户交互
    
-   与后端API交互更新3D内容
    

### API开发

后端API遵循RESTful设计原则，使用JSON格式进行数据交换。

示例端点:

-   `GET /api/scenes` - 获取场景列表
    
-   `GET /api/scenes/:id` - 获取特定场景
    
-   `POST /api/scenes` - 创建新场景
    
-   `PUT /api/scenes/:id` - 更新场景
    
-   `DELETE /api/scenes/:id` - 删除场景
    

## 🧪 测试

### 运行前端测试

bash

cd frontend
npm test
# 或
ng test

### 运行后端测试

bash

cd backend
python -m pytest

### 端到端测试

bash

cd frontend
npm run e2e

## 🐛 故障排除

### 常见问题

1.  **CORS错误**:
    
    -   确保Flask-CORS已正确配置
        
    -   检查后端允许的前端域名
        
2.  **Three.js导入错误**:
    
    -   确保Three.js类型定义已安装: `npm install @types/three`
        
3.  **端口冲突**:
    
    -   修改端口: `ng serve --port 4300` 或 Flask `app.run(port=5001)`
        
4.  **Python依赖问题**:
    
    -   确保使用正确的Python版本
        
    -   尝试重新安装依赖: `pip install -r requirements.txt`
        

### 调试技巧

-   使用浏览器开发者工具检查网络请求和3D渲染
    
-   启用Flask调试模式: `FLASK_ENV=development`
    
-   使用Angular开发工具进行状态管理调试
    

## 📚 学习资源

-   [Angular官方文档](https://angular.io/docs)
    
-   [Flask官方文档](https://flask.palletsprojects.com/)
    
-   [Three.js官方文档](https://threejs.org/docs/)
    
-   [TypeScript手册](https://www.typescriptlang.org/docs/)
    

## 🤝 贡献指南

1.  Fork项目仓库
    
2.  创建功能分支: `git checkout -b feature/新功能`
    
3.  提交更改: `git commit -m '添加新功能'`  
4.  推送到分支: `git push origin feature/新功能` 
5.  提交Pull Request
请确保代码遵循现有风格，并包含适当的测试。
## 📞 支持
如有问题或建议，请：
1.  查看 [Issues](https://github.com/your-repo/issues) 页面
2.  创建新的Issue描述问题
3.  通过邮箱联系 lyb3578@163.com
