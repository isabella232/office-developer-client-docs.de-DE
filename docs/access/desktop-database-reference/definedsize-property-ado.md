---
<<<<<<< HEAD-Titel: DefinedSize-Eigenschaft (ADO) TOCTitle: DefinedSize-Eigenschaft (ADO) === Titel: DefinedSize-Eigenschaft (ADO) TOCTitle: DefinedSize-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15) Ms:contentKeyID: 48546257 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="definedsize-property-ado"></a>DefinedSize-Eigenschaft (ADO)
=======
# <a name="definedsize-property-ado"></a>DefinedSize-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Gibt die Datenkapazität eines [Field](field-object-ado.md)-Objekts an.

<<<<<<< Kopf
## <a name="return-value"></a>Rückgabewert
=======
## <a name="return-value"></a>Rückgabewert
>>>>>>> master

Gibt einen Wert vom Datentyp **Long** zurück, der die definierte Größe eines Felds als eine Anzahl von Bytes wiedergibt.

## <a name="remarks"></a>Hinweise

Mithilfe der **DefinedSize** -Eigenschaft bestimmen Sie die Datenkapazität eines **Field** -Objekts.

Die Eigenschaften **DefinedSize** und [ActualSize](actualsize-property-ado.md) unterscheiden sich voneinander. Angenommen, ein **Field** -Objekt mit dem deklarierten Typ **adVarChar** und einer **DefinedSize** -Eigenschaft von 50 enthält ein einzelnes Zeichen. Für die **ActualSize** -Eigenschaft wird als Wert die Länge in Bytes dieses Einzelzeichens zurückgegeben.

