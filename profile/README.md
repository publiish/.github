# Publiish - PantherStorage IPFS Network

**Publiish** empowers users with **data sovereignty** through **decentralized, trustless** storage on the **PantherStorage IPFS Network**. By leveraging **IPFS**, it ensures **censorship-resistant**, immutable, and secure data accessibility - without intermediaries.

![data_sovereignty](https://github.com/user-attachments/assets/4f370568-3dc7-4be6-a5e3-f34a3f582071)

## Features
🛡 **Data Sovereignty & Trustlessness** – Full control over your data with no intermediaries.  
🔒 **Encrypted Private Storage** – Secure, end-to-end encrypted files only accessible by authorized users.  
🌍 **Decentralized IPFS Network** – Peer-to-peer storage ensuring resilience and redundancy.  
⚖ **Censorship-Resistant Access** – Content remains accessible globally, free from centralized control.  
⚡ **Immutable & Verifiable** – Content-addressable storage guarantees authenticity and integrity.  
🏢 **Enterprise-Ready Security** – Custom access policies for organizations and developers.  

## Getting Started

### Prerequisites
Ensure you have **Docker** and **Docker Compose** installed:

```sh
sudo apt install -y docker-compose
sudo usermod -a -G docker $USER
```
Restart your terminal after adding the user to the Docker group.

### Unlock Your Access to PantherStorage
Unlock **sovereign, censorship-resistant storage** by obtaining **your unique access keys** to the **PantherStorage IPFS Network**.

📧 **Email**: support@pantherstorage.io  
🌍 **Website**: [https://pantherstorage.io/contact](https://pantherstorage.io/contact)  
💬 **Community**: Discord/Telegram support  

You will receive:  
- **SWARM_KEY** - IPFS network security key  
- **CLUSTER_SECRET** - Cluster authentication key  

### Setup & Run
Update your `docker-compose.yml` with your keys:

```yaml
version: '3.7'
services:
  ipfs:
    environment:
      - SWARM_KEY=your-received-swarm-key
  cluster:
    environment:
      - CLUSTER_SECRET=your-received-cluster-secret
```

Start the node:
```sh
docker-compose up -d --build
```

Check cluster status:
```sh
docker container exec cluster0 ipfs-cluster-ctl peers ls
```

## Troubleshooting
- **Node not appearing in the cluster?**  
  - Verify **SWARM_KEY** and **CLUSTER_SECRET** are correct.  
  - Restart services: `docker-compose restart`  
  - Check logs: `docker logs cluster0`  

## Contributing
We welcome contributions! Feel free to open issues, submit PRs, and help improve **Publiish - PantherStorage IPFS Network**.

## License
This project is licensed under the **MIT License**. See `LICENSE` for details.

---
![1x1_In_a_world_where_data_sovereignt_3](https://github.com/user-attachments/assets/c7a5e99e-d68a-42df-88e5-eac8d28c013e)

### 🔗 Take Control of Your Data - Join the PantherStorage IPFS clusters  
The future of **data sovereignty** is here. Build, store, and share freely on a **decentralized, trustless network** where your files remain **yours, forever.**  

[Website](https://pantherstorage.io) • [Community](https://discord.gg/) • [Docs](https://docs.pantherstorage.io)
