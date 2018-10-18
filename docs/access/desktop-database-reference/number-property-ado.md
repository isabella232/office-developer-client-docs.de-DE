---
<<<<<<< HEAD-Titel: Anzahl-Eigenschaft (ADO) TOCTitle: Anzahl-Eigenschaft (ADO) === Titel: Number-Eigenschaft (ADO) TOCTitle: Number-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15) Ms:contentKeyID: 48547243 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="number-property-ado"></a>Number-Eigenschaft (ADO)
=======
# <a name="number-property-ado"></a>Number-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Gibt die Nummer an, durch die ein [Error](error-object-ado.md)-Objekt eindeutig identifiziert wird.

<<<<<<< Kopf
## <a name="return-value"></a>Rückgabewert
=======
## <a name="return-value"></a>Rückgabewert
>>>>>>> master

Gibt einen **Long** -Wert zurück, der einer der [ErrorValueEnum](errorvalueenum.md)-Konstanten entsprechen kann.

## <a name="remarks"></a>Hinweise

Ermitteln Sie mit der **Number** -Eigenschaft, welcher Fehler aufgetreten ist. Der Wert der Eigenschaft ist eine eindeutige Zahl, die der Fehlerbedingung entspricht.

Die [Errors](errors-collection-ado.md) -Auflistung gibt ein HRESULT im Hexadezimal-Format (beispielsweise 0 x 80004005) oder long-Wert (beispielsweise 2147467259) zurück. Diese HRESULT-Werte können von zugrunde liegenden Komponenten wie OLE DB oder direkt von OLE ausgelöst werden. Weitere Informationen zu diesen Nummern finden Sie in Kapitel 16 von der *OLE DB-Programmierreferenz.*

