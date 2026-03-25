# Smart Home AI
Nền tảng Smart Home AI cung cấp các thiết bị nhà thông minh tích hợp trí tuệ nhân tạo, cho phép người dùng quản lý, giám sát và tự động hóa hệ sinh thái thiết bị trong ngôi nhà của mình.

Hệ thống bao gồm:

🌍 Website Global: Trang giới thiệu sản phẩm Smart Home cho khách hàng
🏢 ERP Internal System: Hệ thống nội bộ quản lý hàng hóa, kho và vận hành
⚙️ API Platform: Hệ thống backend phục vụ Web, Mobile và các dịch vụ tích hợp
🚀 Tech Stack

Hệ thống được xây dựng theo kiến trúc Modern Cloud Native Architecture

Frontend
Next.js (React Framework)
TypeScript
TailwindCSS
GraphQL Client / REST Client
Backend
NestJS
TypeScript
RESTful API
GraphQL API
Database
PostgreSQL
Prisma ORM
Message Queue & Cache
Redis (Cache, Session, Rate Limiting)
RabbitMQ (Event Driven Architecture)
Infrastructure
Docker
Kubernetes (K8s)
CI/CD Pipeline
🏗️ System Architecture
                 ┌────────────────────┐
                 │     NextJS Web     │
                 │  Global Website    │
                 └─────────▲──────────┘
                           │
                           │
                 ┌─────────┴──────────┐
                 │      API Gateway    │
                 │       NestJS        │
                 └─────────▲──────────┘
                           │
        ┌──────────────────┼──────────────────┐
        │                  │                  │
 ┌──────────────┐  ┌──────────────┐  ┌──────────────┐
 │ Auth Service │  │ Product API  │  │ ERP Service  │
 │  NestJS      │  │ NestJS       │  │ NestJS       │
 └──────▲───────┘  └──────▲───────┘  └──────▲───────┘
        │                 │                 │
        │                 │                 │
     Redis             PostgreSQL        RabbitMQ
        │
     Prisma ORM
📦 Project Structure
smart-home-ai/
│
├── apps/
│   ├── web-global/        # NextJS Global Website
│   ├── erp-dashboard/     # ERP Internal System
│   └── api-gateway/       # NestJS API Gateway
│
├── services/
│   ├── auth-service
│   ├── product-service
│   ├── inventory-service
│   └── order-service
│
├── packages/
│   ├── prisma
│   ├── shared-types
│   └── utils
│
├── infrastructure/
│   ├── docker
│   ├── kubernetes
│   └── ci-cd
│
└── README.md
🌍 Global Website Features

Trang web dành cho khách hàng toàn cầu.

Features
Giới thiệu hệ sinh thái Smart Home AI
Danh sách sản phẩm
Chi tiết sản phẩm
So sánh thiết bị
Blog / News
Contact / Support
Example Products
AI Camera
Smart Door Lock
Smart Lighting
Smart Sensors
Smart Hub
🏢 ERP Internal System

Hệ thống nội bộ dùng cho quản lý doanh nghiệp.

ERP Features
Quản lý sản phẩm
Quản lý tồn kho
Nhập hàng
Xuất hàng
Quản lý đơn hàng
Thống kê doanh thu
Quản lý nhân viên
🔌 API Architecture

Backend cung cấp RESTful API và GraphQL API

REST API Example
GET /api/products
GET /api/products/:id
POST /api/orders
POST /api/auth/login
GraphQL Example
query {
  products {
    id
    name
    price
    stock
  }
}
🧠 Smart Home AI Vision

Mục tiêu của nền tảng:

Tự động hóa ngôi nhà
Tích hợp AI vào thiết bị
Phân tích hành vi người dùng
Điều khiển thiết bị bằng AI

Ví dụ:

AI tự động bật đèn khi phát hiện chuyển động
Camera AI nhận diện người lạ
Tối ưu năng lượng trong nhà
🐳 Docker Setup

Build toàn bộ hệ thống bằng Docker

docker-compose up --build

Services:

NextJS
NestJS
PostgreSQL
Redis
RabbitMQ
☸️ Kubernetes Deployment

Deploy hệ thống lên Kubernetes.

kubectl apply -f infrastructure/kubernetes

Bao gồm:

Deployment
Service
Ingress
ConfigMap
Secret
⚡ Development Setup
Install dependencies
npm install
Run development

Frontend

npm run dev:web

Backend

npm run dev:api
🔐 Security

Các cơ chế bảo mật:

JWT Authentication
RBAC Authorization
Rate Limiting
API Validation
Secure Environment Variables
📈 Future Roadmap
Mobile App (React Native)
AI Device Control
IoT Device Integration
AI Voice Assistant
Smart Energy Monitoring
👨‍💻 Author

Developed by Smart Home AI Team

📄 License

MIT License