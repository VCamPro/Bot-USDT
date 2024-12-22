# Telegram Bot for TRX Transactions via USDT on the TRC20 Network  

This project is written in the Go programming language.  
It is provided for reference only and contains numerous errors.  

### Notes to Consider:

1. **Replace Required Parameters**  
   Before using the code, ensure you replace all placeholders starting with `YOUR_` in the code, such as the Telegram Bot Token, Webhook URL, SSL certificate path, listening address, etc.

2. **Install Dependencies**  
   Make sure you have the Go environment installed. Use `go get` to install the required packages:  
   - `github.com/go-redis/redis`  
   - `github.com/go-telegram-bot-api/telegram-bot-api`  

### Compilation Instructions:

1. Save the code into a file named `main.go`.  
2. Run the command `go build -o bot main.go` in the terminal to compile the code and create an executable file named `bot`.  

### Deployment Instructions:

1. Prepare a server and upload the compiled `bot` executable to the server.  
2. Configure the server's SSL certificate and Nginx reverse proxy as needed to ensure the Webhook URL is accessible via HTTPS.  
3. Execute `./bot` on the server to start the program. The program will initiate an HTTP server and listen for Webhook callbacks.  
4. Configure the Webhook in the Telegram Bot Management interface, setting the Webhook URL to your server's address in the format:  
   `https://your-domain.com/your-bot-token`  
   Here, `your-domain.com` is your server's domain name, and `your-bot-token` is your Telegram Bot Token.  

### After Deployment:

Once the deployment is complete, you can send commands to the bot via Telegram to perform USDT transfers and check balances.  
