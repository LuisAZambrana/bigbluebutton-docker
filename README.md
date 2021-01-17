# BigBlueButton Docker
# Agradecimiento a alangecker por su gran trabajo!


- Mira el siguiente Link https://luiszambrana.com.ar/2021/01/17/buscas-un-software-de-codigo-abierto-para-dar-clases-big-blue-button-es-la-opcion/
- Instalación muy facil
- Se incluye Greenlight
- Certificados HTTPS
- Funciona en la distribuciones como Debian, Ubuntu, CentOS.
- Soporte IPv4 IPv6

## Instalación
1. Deben contacto con Docker instalado. Necesitan saber como les muesto en https://luiszambrana.com.ar/2020/05/14/instalar-docker-sobre-ubuntu-20-04/
2. Es aconsejable que el BBB se utilice en un servidor aparte y no en el mismo en el que esta tu web funcionando.
3. Es aconsejable tener configurado un dominio tipo https/bbb.tudominio.com ya que es solicitado al momento de la instalación
4. Clona este repositorio
   $ git clone --recurse-submodules https://github.com/LuisAZambrana/bigbluebutton-docker.git bbb-docker
   $ cd bbb-docker
   ```
5. Ejecutamos el setup:
   ```bash
   $ ./scripts/setup
   ```
6. Iniciamos containers:
    ```bash
    $ ./scripts/compose up -d
    ```
7. Si utiizas greenlight, debers crear una cuenta de administdor:
    ```bash
    $ ./scripts/compose exec greenlight bundle exec rake admin:create
    ```
8. Luego de creada la cuenta adminsitración ya puedes ingrsar con tu usuario, crear canales invitar amigos alumnos etc.
