Project: 💡 Optimizing ELK Stack Costs with S3 & Lifecycle Management 💰



Hey #Cloud #DevOps folks! 👋 Sharing a recent project where we tackled a common challenge: skyrocketing ELK stack costs! 📈

Our client was storing all kinds of logs (application, K8s, infrastructure, Jenkins – you name it!) in their ELK setup, including tons of historical data. This led to overload and a seriously hefty bill. 💸

Our solution? ➡️ We implemented a strategy to offload Jenkins logs to an S3 bucket and applied lifecycle management policies. This meant:

🚚 Moving Jenkins logs from the EC2 instance to S3.

⏳ Automatically transitioning older logs to Glacier/Deep Archive for cost savings.

🗑️ Deleting aged logs based on the defined lifecycle, keeping only the recent data needed.

The results? 🥁 A whopping 50% cost reduction! 🎉

This approach not only slashed expenses but also improved the performance of their ELK stack by reducing the data volume. 🚀

Key steps included:

👉 Installing the AWS CLI on the Jenkins EC2 instance. 💻

👉 Creating a bash script to automate log transfer to S3 daily. ✍️

👉 Configuring S3 lifecycle policies to manage log archiving and deletion.⚙️

