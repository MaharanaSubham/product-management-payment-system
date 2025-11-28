<h1 align="center">Product Management & Payment System</h1>

<p align="center">
  A full-stack Product Management and Payment System built with 
  <strong>ASP.NET Core Web API</strong> (Clean Architecture),
  <strong>Angular</strong>, and <strong>SQL Server</strong>. 
  Includes product catalog, categories, shopping cart, orders, authentication,
  and integrated payment gateway support (Stripe/Razorpay).
</p>

<hr />

<h2>📦 Project Overview</h2>
<p>
This project is a complete e-commerce product management and payment system built using 
a scalable <strong>4-layer Clean Architecture</strong>:
</p>

<ul>
  <li><strong>Core Layer</strong> – Entities, Interfaces, Domain Models</li>
  <li><strong>Application Layer</strong> – DTOs, Services, Business Logic</li>
  <li><strong>Infrastructure Layer</strong> – EF Core, SQL Server, Repositories, Identity, Payments</li>
  <li><strong>API Layer</strong> – Controllers, JWT Authentication, Endpoints, Swagger</li>
</ul>

<p>The frontend is developed using <strong>Angular</strong> and communicates with the backend via REST APIs.</p>

<hr />

<h2>🛠 Tech Stack</h2>

<ul>
  <li><strong>.NET 8</strong> – ASP.NET Core Web API</li>
  <li><strong>Entity Framework Core</strong> – Code First</li>
  <li><strong>Angular</strong> – Frontend Framework</li>
  <li><strong>SQL Server</strong> – Database</li>
  <li><strong>JWT Authentication</strong> – Secure login system</li>
  <li><strong>Stripe / Razorpay</strong> – Payment Gateway Integration</li>
</ul>

<hr />

<h2>🚀 Features</h2>

<ul>
  <li><strong>User Authentication</strong> (JWT based)</li>
  <li><strong>Product Management</strong> (CRUD)</li>
  <li><strong>Category Module</strong></li>
  <li><strong>Shopping Cart</strong></li>
  <li><strong>Checkout & Order Processing</strong></li>
  <li><strong>Payment Gateway</strong> (Stripe/Razorpay)</li>
  <li><strong>Admin Panel</strong> for managing products & categories</li>
  <li><strong>Clean Architecture</strong> for scalability</li>
  <li><strong>SQL Database</strong> using EF Core Migrations</li>
</ul>

<hr />

<h2>📂 Project Structure</h2>

<pre>
ProductManagement.PaymentSystem.sln
│
├── ProductManagement.PaymentSystem.Core
│     └── Entities, Interfaces, Enums
│
├── ProductManagement.PaymentSystem.Application
│     └── DTOs, Services, Mapping, Validators
│
├── ProductManagement.PaymentSystem.Infrastructure
│     └── DbContext, Identity, Repositories, Payments
│
└── ProductManagement.PaymentSystem.API
      └── Controllers, Auth, Swagger, Middlewares
</pre>

<hr />

<h2>🔧 Setup Instructions</h2>

<h3>1️⃣ Clone the repository</h3>
<pre>
git clone https://github.com/your-username/product-management-payment-system.git
</pre>

<h3>2️⃣ Navigate to the solution directory</h3>
<pre>
cd product-management-payment-system
</pre>

<h3>3️⃣ Restore dependencies</h3>
<pre>
dotnet restore
</pre>

<h3>4️⃣ Update database</h3>
<pre>
dotnet ef database update -p ProductManagement.PaymentSystem.Infrastructure -s ProductManagement.PaymentSystem.API
</pre>

<h3>5️⃣ Run the API</h3>
<pre>
dotnet run --project ProductManagement.PaymentSystem.API
</pre>

<h3>6️⃣ Run the Angular frontend</h3>
<pre>
cd frontend/angular-app
npm install
ng serve -o
</pre>

<hr />

<h2>🔐 Environment Variables</h2>

<p>Add a file <code>appsettings.Development.json</code> inside API with:</p>

<pre>
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=.;Database=ProductDB;Trusted_Connection=True;"
  },
  "Jwt": {
    "Key": "YOUR_SECRET_KEY"
  },
  "Stripe": {
    "SecretKey": "YOUR_STRIPE_SECRET",
    "PublishableKey": "YOUR_STRIPE_PUBLISHABLE"
  }
}
</pre>

<p><strong>Do not commit secrets to GitHub.</strong></p>

<hr />

<h2>📘 API Endpoints (Examples)</h2>

<h3>Authentication</h3>
<ul>
  <li>POST /api/auth/register</li>
  <li>POST /api/auth/login</li>
</ul>

<h3>Products</h3>
<ul>
  <li>GET /api/products</li>
  <li>GET /api/products/{id}</li>
  <li>POST /api/products</li>
  <li>PUT /api/products/{id}</li>
  <li>DELETE /api/products/{id}</li>
</ul>

<h3>Payments</h3>
<ul>
  <li>POST /api/payments/create-intent</li>
  <li>POST /api/payments/webhook</li>
</ul>



