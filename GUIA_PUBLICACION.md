# Sitio de AlquimIA Labs

Sitio estático en castellano para presentar AlquimIA Labs y explicar el uso interno de las apps OAuth rclone y youtube.

## Publicar gratis con GitHub Pages

El hosting de GitHub Pages puede ser gratis con un repositorio público en GitHub Free. Como la cuenta de la empresa todavía no está iniciada en esta PC, estos pasos quedan para la persona responsable de la cuenta alquimia-labs-ar. No hace falta instalar frameworks ni compilar el sitio.

1. Iniciá sesión en GitHub con la cuenta de la empresa alquimia-labs-ar.
2. Creá un repositorio **público** llamado exactamente **alquimia-labs-ar.github.io**.
3. Subí el contenido de esta carpeta al directorio raíz del repositorio: index.html, privacidad.html, condiciones.html y este README.md.
4. En el repositorio, abrí **Settings → Pages**. En **Build and deployment**, elegí **Deploy from a branch**, seleccioná la rama main y la carpeta /(root), y guardá.
5. Esperá a que termine la publicación y comprobá que las tres páginas abran por HTTPS.

GitHub Pages publica el contenido del repositorio en internet. No subas credenciales OAuth, tokens, archivos de respaldo ni ningún otro dato privado al repositorio.

## URLs previstas

Con ese nombre de repositorio, GitHub Pages asigna estas direcciones:

- Página principal: <https://alquimia-labs-ar.github.io/>
- Política de privacidad: <https://alquimia-labs-ar.github.io/privacidad.html>
- Condiciones de uso: <https://alquimia-labs-ar.github.io/condiciones.html>
- Dominio autorizado previsto en Google Auth Platform: alquimia-labs-ar.github.io

Las direcciones serán definitivas cuando se publique el repositorio y GitHub Pages confirme el sitio. En Google Auth Platform, los campos **App domain** deben apuntar a las URLs de página principal, política de privacidad y condiciones de uso indicadas arriba. En **Authorized domains**, ingresá el dominio previsto arriba, sin protocolo, ruta ni URL completa. Configurá también los URI de redirección OAuth que realmente usa cada cliente, por separado; esas direcciones no se deducen de la web estática.

## Verificación del dominio para Google OAuth

Google pide verificar en Google Search Console los dominios vinculados con la página principal, política, condiciones y URI de redirección/orígenes OAuth. La documentación de Google especifica que se verifica el dominio registrable o “top private domain”. En la Public Suffix List, github.io es un sufijo público privado: para este sitio, el dominio previsto es alquimia-labs-ar.github.io, no github.io. No se debe intentar demostrar que la empresa controla el dominio raíz github.io, que pertenece a GitHub.

Después de publicar el sitio, probá verificar la propiedad de la URL-prefix exacta https://alquimia-labs-ar.github.io/ en Search Console, usando la cuenta asociada al proyecto de Google Cloud AlquimIA-Copia. Si elegís el método de archivo HTML, descargá el archivo de verificación que Google genere, colocá ese archivo sin cambios en la raíz del repositorio, publicalo y completá la verificación. Search Console también puede ofrecer la verificación mediante una metaetiqueta. Luego usá en Google Auth Platform el dominio autorizado alquimia-labs-ar.github.io. Google debe aceptar la propiedad del sitio específico; publicar en GitHub Pages por sí solo no la verifica ni garantiza que Google apruebe la revisión OAuth. La cuenta de GitHub controla el espacio de Pages asignado, pero no el sufijo compartido github.io.

Si Search Console o Google Auth Platform no acepta la propiedad/verificación de ese subdominio, la alternativa es usar un dominio propio de la empresa. Si AlquimIA Labs ya controla uno, se puede alojar sin costo adicional en GitHub Pages con un subdominio propio, por ejemplo oauth.su-dominio.ar, y verificar ese dominio en Search Console. Si no existe un dominio propio, no hay garantía de una alternativa gratuita con un hostname compartido: registrar un dominio propio suele tener costo. La web y el hosting pueden seguir siendo gratuitos en Pages, aunque el dominio tenga costo.

La verificación del dominio y la revisión de OAuth son requisitos separados: que una web esté publicada no garantiza que Google apruebe las apps, los scopes solicitados o el acceso a producción. Solicitá solo los permisos necesarios para las funciones descritas en la política.

## Enlaces de referencia

- [Política de Datos del Usuario de los Servicios de las APIs de Google](https://developers.google.com/terms/api-services-user-data-policy)
- [Políticas de OAuth 2.0 de Google](https://developers.google.com/identity/protocols/oauth2/policies)
- [Requisitos de verificación de Google OAuth](https://developers.google.com/identity/protocols/oauth2/production-readiness/brand-verification)
- [Verificar la propiedad de un sitio en Search Console](https://support.google.com/webmasters/answer/9008080)
- [Publicar GitHub Pages desde una rama](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
