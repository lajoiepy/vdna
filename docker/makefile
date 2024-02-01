build:
	docker build -f Dockerfile . -t vdna

start:
	docker run -itd --cpuset-cpus="2,6,10,14" --rm --ipc host --net host --pid host -v $(PWD)/../:/root/vdna --name vdna vdna

gpu_start:
	docker run -itd --cpuset-cpus="2,6,10,14" --gpus all -v /dev:/dev -e NVIDIA_DRIVER_CAPABILITIES=all --rm --ipc host --net host --pid host -v $(PWD)/../:/root/vdna --name vdna vdna

stop:
	docker kill vdna

attach:
	docker exec -it vdna bash