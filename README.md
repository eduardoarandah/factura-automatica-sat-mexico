# factura-automatica-sat-mexico
Generación de CFDI para el portal del SAT México (hacienda)

# Avance

```js
var rfc='AQUIELRFC';
var nombre='NOMBRE APELLIDO';
var producto='CONCEPTO';
var monto='10';
var folio='435';
var forma_de_pago='02 Cheque Nominativo';
var metodo_de_pago='PUE Pago en una sola exhibición';
var regimen_fiscal='612 Personas Físicas con Actividades Empresariales y Profesionales';
var tipo_comprobante='I Ingreso';
var usocfdi='G03 Gastos en general';
var moneda='MXN Peso Mexicano';
var clave_producto='81111800 Servicios de sistemas y administración de componentes de sistemas';
var clave_unidad='';
var codigo_postal_expedicion='91190';
var traslados_impuesto='002 IVA';
var traslados_tipofactor='Tasa';
var traslados_tasaocuota='0.16';

// Emisor/Receptor
$('#Emisor_RegimenFiscal').val(regimen_fiscal).trigger('change');
$('#Emisor_TipoComprobante').val(tipo_comprobante).trigger('change');
$('#Receptor_RfcCargado').val('Otro ').trigger('change');
$('#Receptor_Rfc').val(rfc).trigger('change').trigger('blur');
$('#Receptor_Nombre').val(nombre).trigger('change');
$('#Receptor_UsoCFDIMoral').val(usocfdi).trigger('change');

// Botón siguiente
clickTab($('ul#tabsComprobante.nav-tabs li.active').next()[0].id); autoguardado(this);

// Comprobante
$('#LugarExpedicion').val(codigo_postal_expedicion).trigger('change').trigger('blur');
$('#MonedaLookUp').val(moneda).trigger('change');
$('#FormaPagoLookUp').val(forma_de_pago).trigger('change');
$('#MetodoPagoLookUp').val(metodo_de_pago).trigger('change');
$('#Folio').val(folio).trigger('change').trigger('blur');

//botón nuevo concepto
$('#btnMuestraConcepto').trigger('click');



( Manualmente agregar concepto )

$('#Descripcion').val(producto).trigger('change').trigger('blur');
$('#ValorUnitario').val(monto).trigger('change').trigger('blur');

```
