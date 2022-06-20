# SASS

## COMO COMPILAR SASS A CCS
* Con el software Prepros (Recomendado)
* Con la extensión live sass compiler (presenta algunas dificultades)
    * Si usas esta opción no olvides de agregar lo siguiente al archivo settings.json en la última parte, si ya se encuentra no es necesaaario agregarlo.
    ```javascript
        "liveSassCompile.settings.formats": [
            {
                "format": "compressed",
                "extensionName": ".css", 
                "savePath": "/src/public/dist",
                "savePathSegmentKeys": null,
                "savePathReplaceSegmentsWith": null
            }
        ]
    ```
    * Si encuentras esta propiedad, debes de comentarlo, ya que el **sourcemap** generado me indica dónde se encuentra el archivo original scss donde se está aplicando todos los cambios, es muy útil cuando abres el sitio web en el navegador xq te indica donde está ubicado el estilo en el scss que aplica a lo que vas seleccionando de la web
    ```javascript
        "liveSassCompile.settings.generateMap": false,
    ``` 
    * **El valor de la propiedad savePath puede variar según tus necesidades**

## COMO ARMAR TUS ARCHIVOS
* Siempre deberás de crear una carpeta src/public, dentro de esta carpeta, creas la carpeta dist, donde contendrás lo archivos bundle.js y bundle.css, y aqui estarán todo los archivos comprimidos o mimificados de las carpetas js/index.js y scss/styles.scss
 