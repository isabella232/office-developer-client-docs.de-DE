---
<<<<<<< HEAD-Titel: DataSource-Eigenschaft (ADO) TOCTitle: DataSource-Eigenschaft (ADO) === Titel: DataSource-Eigenschaft (ADO) TOCTitle: DataSource-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15) Ms:contentKeyID: 48545087 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="datasource-property-ado"></a>DataSource-Eigenschaft (ADO)
=======
# <a name="datasource-property-ado"></a>DataSource-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Gibt ein Objekt an, das als [Recordset](recordset-object-ado.md)-Objekt darzustellende Daten enthält.

## <a name="remarks"></a>Hinweise

Mithilfe dieser Eigenschaft werden datengebundene Steuerelemente mit der Datenumgebung erstellt. Die Datenumgebung verwaltet Datensammlungen (Datenquellen), die benannte Objekte (*Datenelemente*) enthalten und als **Recordset**-Objekt dargestellt werden.**

Die Eigenschaften [DataMember](datamember-property-ado.md) und **DataSource** müssen in Kombination verwendet werden.

Das Objekt, auf das verwiesen wird, muss die **IDataSource** -Schnittstelle implementieren und eine **IRowset** -Schnittstelle enthalten.

**Verwendung**

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
