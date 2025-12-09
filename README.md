# Installing `youtubei.js` in n8n (Docker)

This guide explains how to manually install the [`youtubei.js`](https://www.npmjs.com/package/youtubei.js) library inside an n8n container running via Docker Compose.

> ⚠️ Note: Manual installation is **not persistent**. For permanent installation, use a custom Docker image (see below).

---

## Connect with Coolify

```bash
ssh root@5.161.90.237
```

## 📦 Manual Installation (Non-Persistent)

1. **Find the container name**

   ```bash
   docker ps
   ```

2. **Access the n8n container**

   ```bash
   docker exec -it --user root <container_name> sh
   ```

3. **Install `youtubei.js` globally inside the container**

   ```sh
   npm install -g youtubei.js
   exit
   ```

4. **Rerun the container**

   ```sh
   docker restart <container_name>
   ```
