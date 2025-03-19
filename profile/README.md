# Publiish

**Publiish** empowers users with **data sovereignty** through **decentralized, trustless** storage on the **PantherStorage IPFS Network**. By leveraging **IPFS**, it ensures **censorship-resistant**, immutable, and secure data accessibility - without intermediaries.

![1x1_In_a_world_where_data_sovereignt_3](https://github.com/user-attachments/assets/c7c85917-f72a-408f-85b2-93decfe200ed)

### Prerequisites
Ensure you have **Docker** and **Docker Compose** installed:

```sh
sudo apt install -y docker-compose
sudo usermod -a -G docker $USER
```
Restart your terminal after adding the user to the Docker group.

### Setup & Run
Update your `docker-compose.yml` with your keys:

```yaml
version: '3.7'
services:
  ipfs:
    environment:
      - SWARM_KEY=your-swarm-key
  cluster:
    environment:
      - CLUSTER_SECRET=your-cluster-secret
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
 - We welcome contributions! Feel free to open issues, submit PRs, and help improve **Publiish**.
---
![data_sovereignty](https://github.com/user-attachments/assets/d46511b7-7233-4384-acb3-63efe31db1b7)

### 🔗 Take Control of Your Data  
The future of **data sovereignty** is here. Build, store, and share freely on a **decentralized, trustless network** where your files remain **yours.**  

[Website](https://publiish.io/) • [Community](https://discord.gg/) • [Docs](https://publiish.netlify.app/)
