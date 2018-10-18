---
<<<<<<< HEAD-Titel: ActualSize-Eigenschaft (ADO) TOCTitle: ActualSize-Eigenschaft (ADO) Ms:assetid: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a Ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15) Ms:contentKeyID: 48542949 ms.date: 09/18/2015 Mtps_version: V = Office.15
---

# <a name="actualsize-property-ado"></a>ActualSize-Eigenschaft (ADO)
=== Titel: ActualSize-Eigenschaft (ADO) TOCTitle: ActualSize-Eigenschaft (ADO) Ms:assetid: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a Ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15) Ms:contentKeyID: 48542949 ms.date: 10/16/2018 Mtps_version: Office. 15
---

# <a name="actualsize-property-ado"></a>ActualSize-Eigenschaft (ADO)
>>>>>>> master

**Betrifft**: Access 2013 | Office 2013

Gibt die tatsächliche Länge des Werts eines Felds an.

<<<<<<< Kopf
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
=======
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
>>>>>>> master

Gibt einen Wert vom Datentyp Long zurück. Für einige Anbieter kann diese Eigenschaft festgelegt werden, um Speicherplatz für BLOB-Daten zu reservieren. In diesem Fall lautet der Standardwert 0.

## <a name="remarks"></a>Hinweise

Mithilfe der **ActualSize** -Eigenschaft geben Sie die tatsächliche Länge des Werts eines [Field](field-object-ado.md)-Objekts zurück. Die **ActualSize** -Eigenschaft ist für alle Felder schreibgeschützt. Falls ADO die Länge des Werts für das **Field** -Objekt nicht bestimmen kann, wird **adUnknown** von der **ActualSize** -Eigenschaft zurückgegeben.

<<<<<<< HEAD- **ActualSize** und [DefinedSize](definedsize-property-ado.md) Eigenschaften unterscheiden, wie im folgenden Beispiel dargestellt. Ein **Field** -Objekt mit dem deklarierten Typ **AdVarChar** und einer maximalen Länge von 50 Zeichen gibt zurück **DefinedSize** -Eigenschaft den Wert 50, aber des Werts der **ActualSize** -Eigenschaft gibt die Länge des Datenversion, die in das Feld für die Aktueller Datensatz. **Felder** mit einem **DefinedSize** größer als 255 Bytes als Spalten mit variabler Länge behandelt werden.
=== Die Eigenschaften **ActualSize** und [DefinedSize](definedsize-property-ado.md) unterscheiden. Ein **Field** -Objekt mit dem deklarierten Typ **AdVarChar** und einer maximalen Länge von 50 Zeichen gibt zurück **DefinedSize** -Eigenschaft den Wert 50, aber des Werts der **ActualSize** -Eigenschaft gibt die Länge des Datenversion, die in das Feld für die Aktueller Datensatz. **Felder** mit einem **DefinedSize** größer als 255 Bytes als Spalten mit variabler Länge behandelt werden.
>>>>>>> master

