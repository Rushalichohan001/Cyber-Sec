Basic Login System
A secure Node.js-based authentication system featuring JWT authentication, password hashing, input validation, and security logging.

📌 Features
✅ User registration & login ✅ bcrypt password hashing ✅ JWT authentication for secure sessions ✅ Validator.js input sanitization ✅ Helmet.js for secure HTTP headers ✅ Winston logging for tracking security events


⚙️ Installation & Setup
bash
git clone https://github.com/tlanedev/basic-login-system.git
cd basic-login-system
npm install
Create a .env file with:

JWT_SECRET=your-secure-key
SESSION_SECRET=your-session-secret
PORT=3000
Run the server:

bash
npm run dev
Visit http://localhost:3000 in your browser.

🔒 Security Enhancements
🚀 Passwords are hashed before storage:

js
const hashedPassword = await bcrypt.hash(req.body.password, 10);
🚀 JWT authentication secures sessions:

js
const token = jwt.sign({ id: user.id, email: user.email }, process.env.JWT_SECRET);
🚀 Helmet protects HTTP headers:

js
app.use(helmet());
📊 Penetration Testing
✅ XSS blocked after validation fixes ✅ SQL Injection prevented with secure queries ✅ OWASP ZAP confirmed security improvements

📜 Final Notes
This project follows best security practices for user authentication. Contributions welcome!

🚀 Clone and secure your applications today! 🔒✨
