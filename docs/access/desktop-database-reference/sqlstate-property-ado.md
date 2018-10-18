---
<<<<<<< HEAD-Titel: SQLState-Eigenschaft (ADO) TOCTitle: SQLState-Eigenschaft (ADO) === Titel: SQLState-Eigenschaft (ADO) TOCTitle: SQLState-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15) Ms:contentKeyID: 48547806 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="sqlstate-property-ado"></a>SQLState-Eigenschaft (ADO)
=======
# <a name="sqlstate-property-ado"></a>SQLState-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Gibt den SQL-Status für ein bestimmtes [Error](error-object-ado.md)-Objekt an.

<<<<<<< Kopf
## <a name="return-value"></a>Rückgabewert
=======
## <a name="return-value"></a>Rückgabewert
>>>>>>> master

Gibt einen aus fünf Zeichen bestehenden **String** -Wert zurück, der dem ANSI SQL-Standard entspricht und einen Fehlercode angibt.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **SQLState** -Eigenschaft, um den aus fünf Zeichen bestehenden Fehlercode zu lesen, der vom Anbieter im Falle eines Fehlers bei der Verarbeitung einer SQL-Anweisung zurückgegeben wird. Wenn Sie z. B. den Microsoft OLE DB-Anbieter für ODBC mit einer Microsoft SQL Server-Datenbank verwenden, stammen SQL-Statusfehlercodes von ODBC. Die Codes basieren entweder auf Fehlern, die nur für ODBC gelten, oder auf Fehlern, die von Microsoft SQL Server stammen und dann ODBC-Fehlern zugeordnet wurden. Dieses Fehlercodes sind im ANSI SQL-Standard dokumentiert, sind jedoch in verschiedenen Datenquellen möglicherweise unterschiedlich implementiert.

