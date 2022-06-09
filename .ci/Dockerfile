FROM ghcr.io/sosiristseng/docker-juliabook:1.7.3.4

ENV LC_ALL C.UTF-8

WORKDIR /usr/src/app

# Python deps (jupyter-book and matplotlib)
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Julia command
CMD ["jupyter-book"]

# If using sysimage
# CMD ["julia", "-Jsysimage.so"]
