---
<<<<<<< HEAD-Titel: Type-Eigenschaft (ADO) TOCTitle: Type-Eigenschaft (ADO) === Titel: Type-Eigenschaft (ADO) TOCTitle: Type-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c Ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15) Ms:contentKeyID: 48543397 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="type-property-ado"></a>Type-Eigenschaft (ADO)
=======
# <a name="type-property-ado"></a>Type-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Gibt den Funktions- oder Datentyp eines [Parameter](parameter-object-ado.md)-, [Field](field-object-ado.md)- oder [Property](property-object-ado.md)-Objekts an.

<<<<<<< Kopf
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
=======
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
>>>>>>> master

Legt einen [DataTypeEnum](datatypeenum.md)-Wert fest oder gibt den Wert zurück.

## <a name="remarks"></a>Hinweise

Bei **Parameter** -Objekten ist die **Type** -Eigenschaft nicht schreibgeschützt. Bei neuen **Field** -Objekten, die der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, ist **Type** erst schreibgeschützt, nachdem die [Value](value-property-ado.md)-Eigenschaft für das **Field** -Objekt festgelegt wurde und der Datenprovider das neue **Field** -Objekt durch Aufrufen der [Update](update-method-ado.md)-Methode der **Fields** -Auflistung hinzugefügt hat.

Bei allen anderen Objekten ist die **Type** -Eigenschaft schreibgeschützt.

