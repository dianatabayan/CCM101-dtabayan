# MinIO Deployment Documentation

## Docker Command Used

The MinIO server was deployed using Docker with the following command:

```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
  -e "MINIO_ROOT_USER=cloudadmin" \
  -e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
  quay.io/minio/minio server /data --console-address ":9001"
```

The MinIO image was pulled from **Quay.io** (`quay.io/minio/minio`) instead of Docker Hub (`minio/minio`) because the initial Docker Hub pull returned an **"access denied"** error.

## Deployment Details

| Item                 | Value                 |
| -------------------- | --------------------- |
| **Container Name**   | `minio-server`        |
| **API Port**         | `9000`                |
| **Web Console Port** | `9001`                |
| **Bucket Created**   | `client-photos`       |
| **Image Source**     | `quay.io/minio/minio` |

## Deployment Steps

1. Started a **KillerCoda Ubuntu Playground** environment.
2. Executed the Docker command to download and start the MinIO server.
3. Verified that the MinIO container was running using:

   ```bash
   docker ps
   ```
4. Opened **port 9001** through the **Traffic / Ports** tab to access the MinIO web console.
5. Logged in using the administrator credentials configured through the environment variables.
6. Created a bucket named **`client-photos`**.
7. Uploaded a sample file to the `client-photos` bucket to verify that the storage system was working correctly.

## Environment Variables

The `-e` flags in the Docker command are used to pass environment variables into the MinIO container.

* **`MINIO_ROOT_USER=cloudadmin`** — Defines the administrator username used to access the MinIO web console and API.
* **`MINIO_ROOT_PASSWORD=CloudNova2026!`** — Defines the administrator password for the MinIO root account.

MinIO reads these environment variables when the container starts and uses them to configure the initial administrator account. This eliminates the need for additional account setup after deployment.

> **Security Note:** The credentials shown above are intended only for this lab environment. In a production deployment, strong credentials should be stored securely and should not be included directly in command-line documentation or source code.

## Troubleshooting

### Docker Hub Pull Error

The first deployment attempt failed because the `minio/minio` image could not be pulled from Docker Hub and returned an **"access denied"** error.

**Solution:** The image source was changed to:

```text
quay.io/minio/minio
```

The MinIO container was then successfully downloaded and started.

### Container Name Conflict

A subsequent deployment attempt failed because a container named **`minio-server`** already existed.

**Solution:** The existing container was removed using:

```bash
docker rm -f minio-server
```

The Docker command was then executed again, allowing the MinIO server to start successfully.

## Screenshots

The following screenshots document the deployment and storage configuration:

* **`screenshots/minio-deployed.png`** — Shows the MinIO container running successfully.
* **`screenshots/minio-bucket-upload.png`** — Shows the `client-photos` bucket containing an uploaded sample file.

## Result

The MinIO object storage server was successfully deployed in the KillerCoda Ubuntu environment. The MinIO web console was accessible through **port 9001**, while the object storage API was available through **port 9000**. A `client-photos` bucket was created and successfully tested by uploading a sample file.
