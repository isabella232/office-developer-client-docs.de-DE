---
<<<<<<< HEAD-Titel: AbsolutePage-Eigenschaft (ADO) TOCTitle: AbsolutePage-Eigenschaft (ADO) Ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15) Ms:contentKeyID: 48547288 ms.date: 09/18/2015 Mtps_version: V = Office.15
---

# <a name="absolutepage-property-ado"></a>AbsolutePage-Eigenschaft (ADO)

=== Titel: AbsolutePage-Eigenschaft (ADO) TOCTitle: AbsolutePage-Eigenschaft (ADO) Ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15) Ms:contentKeyID: 48547288 ms.date: 10/17/2018 Mtps_version: Office. 15
---

# <a name="absolutepage-property-ado"></a>AbsolutePage-Eigenschaft (ADO)
>>>>>>> master

**Betrifft**: Access 2013 | Office 2013

Gibt an, auf welcher Seite sich der aktuelle Datensatz befindet.

<<<<<<< Kopf
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

<a name="sets-or-returns-a-long-value-from-1-to-the-number-of-pages-in-the-recordsetrecordset-object-adomd-object--pagecountpagecount-property-adomd--or-returns-one-of-the-positionenumpositionenummd-values"></a>Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** zwischen 1 und der Seitenanzahl im [Recordset](recordset-object-ado.md)-Objekt ([PageCount](pagecount-property-ado.md)) zurückgegeben oder festgelegt, oder es wird einer der Werte von [PositionEnum](positionenum.md) zurückgegeben.
=======
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt fest oder gibt einen **Long** -Wert von 1 bis die Anzahl der Seiten im [Recordset](recordset-object-ado.md) -Objekt ([PageCount](pagecount-property-ado.md)) oder einen der Werte [PositionEnum](positionenum.md) zurückgegeben.
>>>>>>> master

## <a name="remarks"></a>Hinweise

Mit dieser Eigenschaft kann die Nummer der Seite identifiziert werden, auf der sich der aktuelle Datensatz befindet. Sie verwendet die [PageSize](pagesize-property-ado.md)-Eigenschaft, um die Gesamtzahl von Rowsets des **Recordset** -Objekts logisch in Seitenblöcke aufzuteilen, die jeweils die Anzahl von Datensätzen gemäß **PageSize** enthalten (außer der letzten Seite, die weniger Datensätze haben kann). Die entsprechende Funktionalität muss vom Anbieter unterstützt werden, damit diese Eigenschaft verfügbar ist.

Beim Abrufen oder Festlegen der **AbsolutePage** -Eigenschaft verwendet ADO die [AbsolutePosition](absoluteposition-property-ado.md)- und die [PageSize](pagesize-property-ado.md)-Eigenschaft wie folgt zusammen:

<<<<<<< Kopf
  - Zum Abrufen von **AbsolutePage** ruft ADO zuerst die **AbsolutePosition** -Eigenschaft ab und dividiert den Wert dann durch die **PageSize** -Eigenschaft.

  - Zum Festlegen von **AbsolutePage** verschiebt ADO die **AbsolutePosition** -Eigenschaft wie folgt: **PageSize** wird mit dem neuen Wert von **AbsolutePage** multipliziert, und dann wird 1 addiert. Die aktuelle Position im **Recordset** -Objekt ist dann nach dem erfolgreichen Festlegen der **AbsolutePage** -Eigenschaft der erste Datensatz auf dieser Seite.
=======
- Zum Abrufen von **AbsolutePage** ruft ADO zuerst die **AbsolutePosition** -Eigenschaft ab und dividiert den Wert dann durch die **PageSize** -Eigenschaft.

- Zum Festlegen von **AbsolutePage** verschiebt ADO die **AbsolutePosition** -Eigenschaft wie folgt: **PageSize** wird mit dem neuen Wert von **AbsolutePage** multipliziert, und dann wird 1 addiert. Daher wird die aktuelle Position im **Recordset-Objekt** nach dem erfolgreichen festlegen **AbsolutePage** der erste Datensatz in dieser Seite.
>>>>>>> master

**AbsolutePage** ist wie die **AbsolutePosition** -Eigenschaft 1-basiert und entspricht 1, wenn der aktuelle Datensatz der erste Datensatz im **Recordset** -Objekt ist. Legen Sie diese Eigenschaft fest, um zum ersten Datensatz einer bestimmten Seite zu navigieren. Die Gesamtseitenanzahl rufen Sie von der **PageCount** -Eigenschaft ab.

