---
<<<<<<< HEAD-Titel: MaxRecords-Eigenschaft (ADO) TOCTitle: MaxRecords-Eigenschaft (ADO) === Titel: MaxRecords-Eigenschaft (ADO) TOCTitle: MaxRecords-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15) Ms:contentKeyID: 48544475 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="maxrecords-property-ado"></a>MaxRecords-Eigenschaft (ADO)
=======
# <a name="maxrecords-property-ado"></a>MaxRecords-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Gibt die maximale Anzahl von Datensätzen an, die von einer Abfrage an ein [Recordset](recordset-object-ado.md) zurückgegeben werden.

<<<<<<< Kopf
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
=======
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
>>>>>>> master

Legt einen Long-Wert fest, der die maximale Anzahl von zurückgegebenen Datensätzen angibt, oder gibt den Wert zurück. Der Standardwert ist Null (kein Limit).

## <a name="remarks"></a>Hinweise

Verwenden Sie die **MaxRecords** -Eigenschaft zur Begrenzung der Anzahl von Datensätzen, die der Anbieter aus der Datenquelle zurückgibt. Die Standardeinstellung dieser Eigenschaft ist NULL und bedeutet, dass der Anbieter alle angeforderten Datensätze zurückgibt.

Die **MaxRecords** -Eigenschaft ist nicht schreibgeschützt, wenn das **Recordset** -Objekt geschlossen ist, und schreibgeschützt, wenn es geöffnet ist.

