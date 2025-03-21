<code>https://api.ewallet.com</code>
 
 <h2>Endpoints</h2>
 
 <h3>1. User Registration</h3>
 <p><strong>Endpoint:</strong> <code>POST /register</code></p>
 <p><strong>Description:</strong> Mendaftarkan pengguna baru.</p>
 <pre>{ "name": "John Doe", "email": "john@example.com", "password": "password123" }</pre>
 <pre>{ "status": "success", "message": "User registered successfully" }</pre>
 
 <h3>2. User Login</h3>
 <p><strong>Endpoint:</strong> <code>POST /login</code></p>
 <p><strong>Description:</strong> Melakukan autentikasi pengguna.</p>
 <pre>{ "email": "john@example.com", "password": "password123" }</pre>
 <pre>{ "status": "success", "token": "YOUR_ACCESS_TOKEN" }</pre>
 
 <h3>3. Get User Balance</h3>
 <p><strong>Endpoint:</strong> <code>GET /balance</code></p>
 <p><strong>Description:</strong> Mengambil saldo pengguna.</p>
 <pre>{ "status": "success", "data": { "user_id": 1, "balance": 100000 } }</pre>
 
 <h3>4. Top Up Balance</h3>
 <p><strong>Endpoint:</strong> <code>POST /topup</code></p>
 <p><strong>Description:</strong> Menambahkan saldo ke akun pengguna.</p>
 <pre>{ "amount": 50000 }</pre>
 <pre>{ "status": "success", "message": "Balance topped up successfully", "data": { "new_balance": 150000 } }</pre>
 
 <h3>5. Transfer Balance</h3>
 <p><strong>Endpoint:</strong> <code>POST /transfer</code></p>
 <p><strong>Description:</strong> Mentransfer saldo ke pengguna lain.</p>
 <pre>{ "receiver_id": 2, "amount": 30000 }</pre>
 <pre>{ "status": "success", "message": "Transfer successful", "data": { "sender_balance": 120000, "receiver_balance": 80000 } }</pre>
 
 <h3>6. Transaction History</h3>
 <p><strong>Endpoint:</strong> <code>GET /transactions</code></p>
 <p><strong>Description:</strong> Mengambil riwayat transaksi pengguna.</p>
 <pre>{ "status": "success", "data": [ { "transaction_id": 101, "type": "topup", "amount": 50000, "timestamp": "2025-03-21T10:00:00Z" }, { "transaction_id": 102, "type": "transfer", "amount": 30000, "receiver_id": 2, "timestamp": "2025-03-21T12:00:00Z" } ] }</pre>
 
 <h2>Authentication</h2>
 <p>Semua endpoint memerlukan autentikasi menggunakan <strong>Bearer Token</strong>:</p>
 <pre>{ "id": 1, "name": "John Doe", "email": "john@example.com" }</pre>
 
 <h2>Error Handling</h2>
 <table>
     <tr>
         <th>Status Code</th>
         <th>Meaning</th>
     </tr>
     <tr>
         <td>200</td>
         <td>OK</td>
     </tr>
     <tr>
         <td>201</td>
         <td>Created</td>
     </tr>
     <tr>
         <td>400</td>
         <td>Bad Request</td>
     </tr>
     <tr>
         <td>401</td>
         <td>Unauthorized</td>
     </tr>
     <tr>
         <td>404</td>
         <td>Not Found</td>
     </tr>
     <tr>
         <td>500</td>
         <td>Internal Server Error</td>
     </tr>
 </table>
 
 <h2>Contact</h2>
 <p>Jika ada pertanyaan lebih lanjut, silakan hubungi <strong>support@ewallet.com</strong>.</p>