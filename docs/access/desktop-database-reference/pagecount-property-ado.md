---
<<<<<<< HEAD-Titel: PageCount-Eigenschaft (ADO) TOCTitle: PageCount-Eigenschaft (ADO) === Titel: PageCount-Eigenschaft (ADO) TOCTitle: PageCount-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15) Ms:contentKeyID: 48546609 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="pagecount-property-ado"></a>PageCount-Eigenschaft (ADO)
=======
# <a name="pagecount-property-ado"></a>PageCount-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Gibt an, wie viele Seiten mit Daten das [Recordset](recordset-object-ado.md)-Objekt enthält.

<<<<<<< Kopf
## <a name="return-value"></a>Rückgabewert
=======
## <a name="return-value"></a>Rückgabewert
>>>>>>> master

Gibt einen **Long** -Wert zurück, der die Anzahl von Seiten im **Recordset** -Objekt angibt.

## <a name="remarks"></a>Hinweise

Bestimmen Sie mit der PageCount-Eigenschaft, wie viele Seiten mit Daten in einem Recordset-Objekt enthalten sind. Seiten sind Datensatzgruppen, deren Größe der Einstellung der PageSize-Eigenschaft entspricht. Die letzte Seite wird auch dann als weitere Seite im PageCount-Wert gezählt, wenn sie nicht vollständig ist, weil sie weniger Datensätze enthält als der PageSize-Wert angibt. Wird diese Eigenschaft vom Recordset-Objekt nicht unterstützt, gibt der Wert -1 an, dass PageCount nicht bestimmt werden kann.

Weitere Informationen zur Seitenfunktionalität finden Sie unter den Eigenschaften **PageSize** und [AbsolutePage](absolutepage-property-ado.md).

