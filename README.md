# 🔐 Task: Frontend Auth Flow with Next.js, JWT & shadcn/ui

You're tasked with implementing a **fully functional authentication flow** using our real API and Figma design.

---

## 🔗 Resources

- **API Docs**: [https://em80etvxo4.apidog.io](https://em80etvxo4.apidog.io)
- **Figma UI**: [Vidinfra 2025 - Auth Flow](https://www.figma.com/proto/pZh3GGEKYQ5TjDWnsRWQSm/Vidinfra---2025?node-id=14023-33898&p=f&t=EMs1MG9aYaz8LehR-0)

---

## 📌 API Endpoints

- `POST /auth/register` – Register a new user  
- `POST /auth/login` – Login and receive JWT access & refresh tokens  
- `GET /auth/profiles` – Fetch current authenticated user (requires JWT access token)

---

## 🛠 Tech Stack

Use the following tools:

- ✅ **Next.js** (App Router)
- ✅ **Typescript**
- ✅ **React Hook Form**
- ✅ **shadcn/ui**
- ✅ **TailwindCSS**

---

## ✅ What You Need to Build

### 1. Register Page (`/register`)
- Fields: name, email, password
- Submit to `POST /auth/register`
- On success, redirect to dashboard

### 2. Login Page (`/login`)
- Fields: email, password
- Submit to `POST /auth/login`
- Store `access_token` + `refresh_token`
- On success, redirect to dashboard

### 3. Dashboard Page (`/dashboard`)
- Protected route
- Fetch user info from `GET /auth/profiles`
- Show name + email + logout button

### 4. JWT Token Management
- Store `access_token` (e.g., memory or localStorage for this task)
- Store `refresh_token` securely (mock cookie or memory)
- If access token expires (simulate it), use `refresh_token` to get a new one
- Automatically logout on refresh failure

---

## ✨ Must-Haves

- Use **React Context or Zustand** to manage auth state
- Auto-refresh token if expired when hitting `/auth/profiles`
- Follow **SOLID principles**
- Use **React Hook Form** for form state + validation
- UI must match the [Figma design](https://www.figma.com/proto/pZh3GGEKYQ5TjDWnsRWQSm/Vidinfra---2025?node-id=14023-33898)

---

## 🔁 Git Instructions

- Use `feature/` branches:  
  - `feature/auth-register`  
  - `feature/auth-login`  
  - `feature/token-refresh`
- Use **conventional commits**:  
  - `feat: implement login page`  
  - `chore: set up auth context`
- Push to a **public GitHub repo**
- Include:
  - `.env.example`
  - `README.md` with setup instructions
  - Any assumptions

---

## 🧠 Evaluation Criteria

| Area               | Expectation                          |
|--------------------|--------------------------------------|
| **Code Quality**   | SOLID, reusable, modular             |
| **Token Management** | Secure and auto-refresh             |
| **UI Accuracy**    | Matches Figma                        |
| **Form Handling**  | Clean RHF usage                      |
| **Git Hygiene**    | Proper commits and branching         |
| **Error Handling** | Clear feedback and graceful failures |
