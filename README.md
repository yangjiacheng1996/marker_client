# marker_client
A python script that can post localhost file to remote Marker Server. Transform pdf/docx/ppt/jpg/ into markdown.

# Quick Start
1. check your Nvidia GPU supports cuda12.9
```bash
nvidia-smi
```
2. Docker run the Marker Server.
```bash
docker run -d --name markerserver --gpus all -p 8000:8000 yangjiacheng/marker_server:v1.9.3-cuda129  
```
3. run marker_client.py and send your document to the Marker Server.Then get the markdown file.
```bash
python marker_client.py  -s http://localhost:8000  -p /path/to/your/helloworld.pdf  -o /path/to/your/output/folder/

# see more options
python marker_client.py --help
```
