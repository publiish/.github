# Publiish - PantherStorage IPFS Network

**Publiish** empowers users with **data sovereignty** through **decentralized, trustless** storage on the **PantherStorage IPFS Network**. By leveraging **IPFS**, it ensures **censorship-resistant**, immutable, and secure data accessibility - without intermediaries.

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
We welcome contributions! Feel free to open issues, submit PRs, and help improve **Publiish**.

---

### 🔗 Take Control of Your Data  
The future of **data sovereignty** is here. Build, store, and share freely on a **decentralized, trustless network** where your files remain **yours.**  

[Website](https://publiish.io/) • [Community](https://discord.gg/) • [Docs](https://publiish.netlify.app/)
