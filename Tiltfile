docker_build('loops', \
'src', dockerfile = 'src/Dockerfile.local', \
ignore=["bin", "obj"], \
live_update=[sync('./src', '/src')]
)

k8s_yaml("loops.yaml")
k8s_resource('loops', port_forwards=["5555:80","9999:22"])

