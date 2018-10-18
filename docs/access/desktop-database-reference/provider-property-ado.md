---
<<<<<<< HEAD-Titel: Provider-Eigenschaft (ADO) TOCTitle: Provider-Eigenschaft (ADO) === Titel: Provider-Eigenschaft (ADO) TOCTitle: Provider-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a Ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15) Ms:contentKeyID: 48543543 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="provider-property-ado"></a>Provider-Eigenschaft (ADO)
=======
# <a name="provider-property-ado"></a>Provider-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Gibt den Namen des Anbieters für ein [Connection](connection-object-ado.md)-Objekt an.

<<<<<<< Kopf
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
=======
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
>>>>>>> master

Legt einen **String** -Wert fest, der den Namen des Anbieters angibt, oder gibt den Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie die Provider-Eigenschaft, um den Namen des Anbieters für eine Verbindung festzulegen oder zurückzugeben. Diese Eigenschaft kann mit dem Inhalt der ConnectionString-Eigenschaft oder dem Argument ConnectionString der Open-Methode festgelegt werden. Wenn Sie jedoch einen Anbieter an mehreren Stellen angeben und die Open-Methode aufrufen, kann das zu unerwarteten Ergebnissen führen. Wird kein Anbieter angegeben, gilt der Standardwert MSDASQL für diese Eigenschaft (Microsoft OLE DB-Anbieter für ODBC).

Die **Provider** -Eigenschaft ist nicht schreibgeschützt, wenn die Verbindung geschlossen ist, und schreibgeschützt, wenn sie geöffnet ist. Die Einstellung wird erst wirksam, wenn Sie das **Connection** -Objekt öffnen oder auf die [Properties](properties-collection-ado.md)-Auflistung des **Connection** -Objekts zugreifen. Ist die Einstellung nicht gültig, tritt ein Fehler auf.

