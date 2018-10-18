---
<<<<<<< HEAD-Titel: DefaultDatabase-Eigenschaft (ADO) TOCTitle: DefaultDatabase-Eigenschaft (ADO) === Titel: DefaultDatabase-Eigenschaft (ADO) TOCTitle: DefaultDatabase-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: a35c5631-f9d9-e51f-950b-e52169830d94 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249757(v=office.15) Ms:contentKeyID: 48546784 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="defaultdatabase-property-ado"></a>DefaultDatabase-Eigenschaft (ADO)
=======
# <a name="defaultdatabase-property-ado"></a>DefaultDatabase-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Gibt die Standarddatenbank für ein [Connection](connection-object-ado.md)-Objekt an.

<<<<<<< Kopf
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
=======
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
>>>>>>> master

Mit dieser Eigenschaft wird ein **String** -Wert festgelegt oder zurückgegeben, der den Namen einer Datenbank angibt, die über den Anbieter verfügbar ist.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **DefaultDatabase** -Eigenschaft, um den Namen der Standarddatenbank in einem bestimmten **Connection** -Objekt festzulegen oder zurückzugeben.

Wenn eine Standarddatenbank vorhanden ist, verwenden SQL-Zeichenfolgen möglicherweise eine unvollständige Syntax für den Zugriff auf Objekte in dieser Datenbank. Für den Zugriff auf Objekte in einer anderen als der in der **DefaultDatabase** -Eigenschaft angegebenen Datenbank müssen Sie Objektnamen mit dem gewünschten Datenbanknamen qualifizieren. Beim Herstellen der Verbindung schreibt der Anbieter Informationen zur Standarddatenbank in die **DefaultDatabase** -Eigenschaft. Manche Anbieter lassen nur eine Datenbank pro Verbindung zu. In diesem Fall können Sie die **DefaultDatabase** -Eigenschaft nicht ändern.

Möglicherweise unterstützen einige Datenquellen und Anbieter dieses Feature nicht und geben einen Fehler oder eine leere Zeichenfolge zurück.

**Remote Data Service-Verwendung** Diese Eigenschaft ist nicht verfügbar für ein clientseitiges **Connection** -Objekt.

