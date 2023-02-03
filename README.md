## Run the commands:
- **Make Dockerfile executable**
```ruby
chmod +x Dockerfile
```
- **Build docker image**
Remove<>
```ruby
gcloud builds submit --tag gcr.io/<project_id>/<tag of image> eg: helloyoutube
```
- **Deploy normally using gcloud**
Remove<>
```ruby
gcloud run deploy --image gcr.io/<project_id>/<tag of image>eg: helloyoutube
```
- **Create a cluster**
```ruby
gcloud container clusters create hello-youtube-gke-cluster --num-nodes 1 --no-enable-basic-auth --issue-client-certificate --zone us-central1-a
```
**If it doesn't work**
```ruby
gcloud services enable container.googleapis.com
```
- **Get Nodes**
```ruby
kubectl get nodes
```
- **Make deployment.yaml executable**
```ruby
chmod +x deployment.yaml
```
- **Apply deployment.yaml**
```ruby
kubectl apply -f deployment.yaml
```
- **Check pods**
```ruby
kubectl get pods
```
- **Apply services.yaml**
```ruby
kubectl apply -f services.yaml
```
- **Check services**
```ruby
kubectl get services
```