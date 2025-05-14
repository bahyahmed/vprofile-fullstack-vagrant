# VProfile Fullstack Infrastructure with Vagrant

This project sets up a complete full-stack development and testing environment for the **VProfile** application using **Vagrant**, **VirtualBox**, and a multi-VM architecture.

It includes provisioning scripts that automatically configure a **Java-based web application** (built with Maven and deployed on Tomcat), a MySQL database, RabbitMQ broker, Memcached caching, and an Nginx reverse proxy. All components run on their own virtual machines and communicate over a private network.

---

## 🚀 Project Overview

- 🔧 Fully automated infrastructure setup using **Vagrant**
- 🐧 Multiple VMs for **database**, **cache**, **app**, **broker**, and **web**
- 🧱 Provisioning with **custom shell scripts**
- ☕ Java web application deployed on **Tomcat**
- 🐘 MySQL initialized from a **DB backup**
- 🧪 Ideal for practicing **DevOps**, **infrastructure as code**, and **environment automation**

---

## 🧰 Tech Stack

- VirtualBox (VM provider)
- Vagrant (provisioning)
- Shell scripting (infra automation)
- Java (app)
- Maven (build tool)
- MySQL (database)
- Memcached (caching)
- RabbitMQ (message broker)
- Tomcat (Java app server)
- Nginx (reverse proxy)

---

## 🖥️ Virtual Machines Setup

| VM Name | Role                | OS             | IP Address     | RAM    |
|---------|---------------------|----------------|----------------|--------|
| `db01`  | MySQL DB            | CentOS Stream  | 192.168.56.15  | 512 MB |
| `mc01`  | Memcached           | CentOS Stream  | 192.168.56.14  | 256 MB |
| `rmq01` | RabbitMQ            | CentOS Stream  | 192.168.56.16  | 512 MB |
| `app01` | Java App (Tomcat)   | CentOS Stream  | 192.168.56.12  | 512 MB |
| `web01` | Nginx Reverse Proxy | Ubuntu 22.04   | 192.168.56.11  | 512 MB |

---

## 🧪 Getting Started

### Prerequisites

- [VirtualBox](https://www.virtualbox.org/)
- [Vagrant](https://www.vagrantup.com/)
- Install required plugin:
  ```bash
  vagrant plugin install vagrant-hostmanager
