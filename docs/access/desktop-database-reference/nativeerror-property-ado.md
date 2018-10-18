---
<<<<<<< HEAD-Titel: NativeError-Eigenschaft (ADO) TOCTitle: NativeError-Eigenschaft (ADO) === Titel: NativeError-Eigenschaft (ADO) TOCTitle: NativeError-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15) Ms:contentKeyID: 48546685 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="nativeerror-property-ado"></a>NativeError-Eigenschaft (ADO)
=======
# <a name="nativeerror-property-ado"></a>NativeError-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Gibt den anbieterspezifischen Fehlercode für ein bestimmtes [Error](error-object-ado.md)-Objekt an.

<<<<<<< Kopf
## <a name="return-value"></a>Rückgabewert
=======
## <a name="return-value"></a>Rückgabewert
>>>>>>> master

Gibt einen **Long** -Wert zurück, der den Fehlercode angibt.

## <a name="remarks"></a>Hinweise

Rufen Sie mit der **NativeError** -Eigenschaft die datenbankspezifische Fehlerinformation für ein bestimmtes **Error** -Objekt ab. Wenn z. B. der Microsoft OLE DB-Anbieter für ODBC mit einer Microsoft SQL Server-Datenbank verwendet wird, werden systemeigene Fehlercodes, die aus SQL Server stammen, über ODBC und den ODBC-Anbieter an die **NativeError** -Eigenschaft übergeben.

