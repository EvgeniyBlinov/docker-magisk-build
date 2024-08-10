[![MIT License][license-image]][license-url]

# docker-magisk-build

Dockerfile for https://github.com/topjohnwu/Magisk building from source.

Tested versions:

- v27.0

Tested commands:

- `./build.py -v ndk`
- `./build.py -v all`



### Usage

```bash
## Clone Magisk with submodules
git clone --recurse-submodules https://github.com/topjohnwu/Magisk.git

## Build container
docker build -t magisk:latest .

## Run container for Magisk building
docker run \
    --rm \
    -v "$PWD/Magisk":/home/gradle/Magisk \
    -w /home/gradle/Magisk \
    magisk:latest \
   bash -c './build.py -v ndk && ./build.py -v all'
```


## License

[![MIT License][license-image]][license-url]

## Author

- [Blinov Evgeniy](mailto:evgeniy_blinov@mail.ru) ([https://evgeniyblinov.ru/](https://evgeniyblinov.ru/))

[license-image]: http://img.shields.io/badge/license-MIT-blue.svg?style=flat
[license-url]: LICENSE
