# AppFirmador

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 12.2.5.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.


## CODIGO HTML
<div style="height:600px">
    <form class="bit4id-sign" action="4identity/Signing" method="post">

    <div class="bit4id-signReq" style="display: none;">

        <div class="bit4id-localFile">YES</div>
        <div class="bit4id-document">http://localhost:81/pdfs/ejemplo.pdf</div>
        <div class="bit4id-documentID">documentID</div>
        <div class="bit4id-preview">YES</div>
        <div class="bit4id-editpagepos">YES</div>
        
        <div class="bit4id-subjectFilterExpr">.*71811264.*</div>
        <div class="bit4id-documentName">TEST PDF DOCUMENT.pdf</div>
        <div class="bit4id-signatureType">PAdES</div>
        <div class="bit4id-signingAlgorithm">RSASHA256</div>

        <div class="bit4id-image">http://localhost/firmador/logomuni.png</div>
        <div class="bit4id-reason">Revisado</div>	
        <div class="bit4id-location">Cercado de Lima</div>

        <div class="bit4id-certInfo">CN</div>

        <div class="bit4id-paragraphFormat">[{ "font" :
            ["Times-BoldItalic",7], "align":"right",
            "data_format":{"timezone":"America/Lima",
            "strtime":"%d.%m.%Y  %H:%M:%S%z"}, 
            "format": ["Firmado Digitalmente bajo resolucion por :",
            "$(CN)s",
            "Proveedor: $(Issuer)s",
            "Local: Cercado de Lima", 
            "Localizacion: $(Location)s", 
            "Motivo: $(Reason)s", 
            "Fecha: $(date)s", ]}]</div>

    </div>

    <div>
        <fieldset>
            <div><h3>DOCUMENTO PARA FIRMA</h3></div>
            <div><p><strong>Esta seguro de continuar?</strong></p></div>
            <div id="bit4id-status"></div>
            <div><input type="submit" value="Firmar" name="cmd" disabled></div>
        </fieldset>
    </div>
    </form>
    <script type="text/javascript" src="http://p.munimoyobamba.gob.pe:10001/smartengine/bit4id-sign.min.js"></script>
</div>






<!-- 
<?php
//$_FILE["attach"]=Información del documento firmado.
//$_POST["documentID"]=Identificador que hemos marcado en index.php.
 
if (!empty($_FILES["attach"])) { 
    $myFile = $_FILES["attach"];
 
    if ($myFile["error"] !== UPLOAD_ERR_OK) {
        echo "<p>Ha ocurrido un error en la subida del fichero.</p>";
        exit;
    }
 
    $name = preg_replace("/[^A-Z0-9._-]/i", "_", $myFile["name"]);
 
    $parts = pathinfo($name);
	$name=$parts["filename"]."-".$_POST["documentID"].".".$parts["extension"];
	/*
		Aquí se puede indicar donde guardar el documento firmado. 
		Tal y como está configurado se guardará en la misma carpeta donde estan los PHP.
	*/
    $success = move_uploaded_file($myFile["tmp_name"],$name);
    if (!$success) {
        echo "<p>No puede guardar el archivo.</p>";
        exit;
    }
    header("Location: sign-end-ok.php?file=".$name); /* Redireción del navegador */
    exit();
} else {
    header("Location: sign-end-error.php"); /* Redireción del navegador */
    exit();
}

?> -->
