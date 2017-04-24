The containers generated will store the data under /var/data directory
To create a new data volume container

docker run --name=your_container_name -v path_to_your_data:/var/data aspgems/data-volume

To use the generated container inside other container, you should:

1.- Use volumes-from flag
2.- Use workdir option to be /var/data

docker run --volumes-from=your_data_volumen_container_name --workdir=/var/data aspgems/rubocop .
