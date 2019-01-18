---
title: AbsolutePosition-Eigenschaft (ADO)
TOCTitle: AbsolutePosition property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b5e25e014c6e93d35e3621bb9b5b3c21d5e77f9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702376"
---
# <a name="absoluteposition-property-ado"></a>AbsolutePosition-Eigenschaft (ADO)

**Betrifft**: Access 2013, Office 2013

Gibt die Position des aktuellen Datensatzes eines [Recordset](recordset-object-ado.md)-Objekts an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** zwischen 1 und der Anzahl von Datensätzen im **Recordset**-Objekt ([RecordCount](recordcount-property-ado.md)) zurückgegeben oder festgelegt, oder es wird einer der Werte von [PositionEnum](positionenum.md) zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Zum Festlegen der **AbsolutePosition** -Eigenschaft erfordert ADO, dass der verwendete OLE DB-Anbieter die IRowsetLocate-Schnittstelle implementieren.

Wenn Sie auf die AbsolutePosition-Eigenschaft eines Recordset-Objekts zugreifen, das mit einem Vorwärtscursor oder einem dynamischen Cursor geöffnet wurde, wird der Fehler adErrFeatureNotAvailable ausgelöst. Sofern der Anbieter die IRowsetScroll-Schnittstelle unterstützt, wird bei anderen Cursortypen die richtige Position zurückgegeben. Wird die IRowsetScroll-Schnittstelle nicht vom Anbieter unterstützt, wird die Eigenschaft auf adPosUnknown festgelegt. In der Dokumentation zu Ihrem Anbieter finden Sie Informationen dazu, ob IRowsetScroll unterstützt wird.

Verwenden Sie die **AbsolutePosition** -Eigenschaft, um zu einem Datensatz entsprechend der Ordnungsposition zu navigieren, die er im **Recordset** -Objekt einnimmt, oder um die Ordnungsposition des aktuellen Datensatzes zu ermitteln. Die entsprechende Funktionalität muss vom Anbieter unterstützt werden, damit diese Eigenschaft verfügbar ist.

[AbsolutePosition](absolutepage-property-ado.md) ist wie die **AbsolutePage** -Eigenschaft 1-basiert und entspricht 1, wenn der aktuelle Datensatz der erste Datensatz im **Recordset** -Objekt ist. Sie können die Gesamtanzahl von Datensätzen im **Recordset** -Objekt mit der [RecordCount](recordcount-property-ado.md)-Eigenschaft abrufen.

Wenn Sie die **AbsolutePosition** -Eigenschaft festlegen, selbst wenn es zu einem Datensatz im aktuellen Cache wird, lädt ADO den Cache mit einer neuen Gruppe von Datensätzen, beginnend mit dem Datensatz, den Sie angegeben. Die [CacheSize](cachesize-property-ado.md) -Eigenschaft bestimmt die Größe dieser Gruppe.


> [!NOTE]
> [!HINWEIS] Sie sollten die **AbsolutePosition** -Eigenschaft nicht als Ersatz-Datensatznummer verwenden. Die Position eines Datensatzes wird geändert, wenn Sie einen vorausgehenden Datensatz löschen. Außerdem gibt es keine Gewähr, dass ein bestimmter Datensatz den gleichen Wert für **AbsolutePosition** aufweist, wenn das **Recordset** -Objekt erneut abgefragt oder geöffnet wird. Lesezeichen sind weiterhin die empfohlene Methode zurückzukehren, um eine bestimmte Position und sind die einzige Möglichkeit der Positionierung für alle Typen von **Recordset** -Objekten.


