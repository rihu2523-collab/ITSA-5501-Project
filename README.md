# ITSA 5501 Project - Milestone 1
Initial structure.

## Contributing
Follow branch/PR workflow.

HEAD
# ITSA 5501 Project - Milestone 1

This project demonstrates how to organize a DevOps project using Git and GitHub.  
It includes Docker, Kubernetes, and Infrastructure as Code examples.

- docker/Dockerfile.example → Example Dockerfile added in experiment branch


 experiment
 # ITSA-5501 Project

## Repository Structure


---

## Git Workflow

We follow a **Git workflow** that ensures organized collaboration:

1. **Branches**
   - `main`: The stable branch with production-ready code.
   - `experiment` / feature branches: For new features, experiments, or fixes.

2. **Merging**
   - Changes from feature branches are merged into `main` using pull requests.
   - Conflicts are resolved locally before committing.

3. **Pull Requests (PRs)**
   - Create a PR when a feature branch is ready to merge.
   - PRs are reviewed, approved, and then merged into `main`.

4. **Tagging**
   - Tags are created for major releases or milestones.
   - Example:
     ```bash
     git tag v1.0
     git push origin v1.0
     ```

---

## Tools Used

- **VS Code** – Code editor
- **Git & GitHub** – Version control and repository hosting
- **Docker** – Containerization
- **Kubernetes (k8s)** – Orchestration
- **Infrastructure as Code (IaC)** tools as needed

---

## Instructions for Future Contributions

1. **Clone the repository**
   ```bash
   git clone https://github.com/rihu2523-collab/ITSA-5501-Project.git
   cd ITSA-5501-Project
---

## Milestone 2 — Containerization and Service Deployment

This milestone demonstrates deploying and managing a multi-container environment using **Docker Compose**.  
The project integrates multiple services for a simulated full-stack system.

###  Container Services Configured
| Service | Technology | Purpose |
|----------|-------------|----------|
| **frontend** | NGINX (Alpine) | Serves a static website (`index.html`) about a vacation destination |
| **user-db** | MongoDB | Stores user-related data |
| **product-db** | PostgreSQL | Stores product-related data |
| **cache** | Redis | Provides caching functionality |
| **prometheus** | Prometheus | Monitors the environment on port `9091` |

---

###  Docker Compose Operations
1. Created a `docker-compose.yml` file defining all 5 services.
2. Configured persistent volumes:
   - `user_data` for MongoDB
   - `product_data` for PostgreSQL
3. Defined a shared network `app-network` for inter-container communication.
4. Verified all containers running using:
   ```bash
   docker ps

   ---

### Outcome
All containers successfully deployed and verified:
- Frontend accessible on [http://localhost:9090](http://localhost:9090)
- Prometheus monitoring available on [http://localhost:9091](http://localhost:9091)
- Databases and cache running within the shared Docker network

All updates committed and pushed to GitHub.

