# Next.js Docker

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev

# Add deploy script
sftp root@ipAddress
sftp > put deploy.sh

# Convert deploy script to Linux format
apt instal dos2unix
dos2unix deploy.sh
chmod +x deploy.sh

# Add nginx config
sudo nano /etc/nginx/sites-available/nextjs-app
sudo ln -s /etc/nginx/sites-available/nextjs-app /etc/nginx/sites-enabled/
sudo nginx -t
sudo systemctl reload nginx

docker-compose up -d

```
