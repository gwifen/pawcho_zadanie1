# Creation of a builder named zadanie1 using the docker-container driver and setting it as default:
docker buildx create --name zadanie1 --driver docker-container --bootstrap --use
# Building images that will operate on architectures: linux/arm64 and linux/amd64 using the docker-container driver:
docker buildx build -q -t docker.io/gwifen/zadanie1:1 --platform linux/amd64,linux/arm64 --push .
# The command to inspect the manifest for a given image:
docker buildx imagetools inspect docker.io/gwifen/zadanie1:1
