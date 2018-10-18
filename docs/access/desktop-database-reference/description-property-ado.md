---
<<<<<<< HEAD-Titel: Description-Eigenschaft (ADO) TOCTitle: Description-Eigenschaft (ADO) === Titel: Description-Eigenschaft (ADO) TOCTitle: Description-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15) Ms:contentKeyID: 48544064 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="description-property-ado"></a>Description-Eigenschaft (ADO)
=======
# <a name="description-property-ado"></a>Description-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Beschreibt ein [Error](error-object-ado.md)-Objekt.

<<<<<<< Kopf
## <a name="return-value"></a>Rückgabewert
=======
## <a name="return-value"></a>Rückgabewert
>>>>>>> master

Gibt einen Wert vom Datentyp **String** zurück, der eine Beschreibung des Fehlers enthält.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **Description** -Eigenschaft, um eine kurze Beschreibung des Fehlers zu erhalten. Zeigen Sie diese Eigenschaft an, um den Benutzer auf einen Fehler hinzuweisen, den Sie nicht behandeln können oder möchten. Die Zeichenfolge stammt aus ADO oder von einem Anbieter.

Die Anbieter sind für das Übergeben eines bestimmten Fehlertexts an ADO verantwortlich. ADO fügt für jeden Anbieterfehler oder jede erhaltene Warnung der [Errors](error-object-ado.md) -Auflistung ein **Error**-Objekt hinzu. Zeigen Sie die **Errors** -Auflistung an, um die vom Anbieter gemeldeten Fehler zu überprüfen.

