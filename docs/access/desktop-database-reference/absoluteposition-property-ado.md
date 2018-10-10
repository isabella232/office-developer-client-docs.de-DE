---
title: AbsolutePosition-Eigenschaft (ADO)
TOCTitle: AbsolutePosition Property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3258ffcab87b16e4931c9881a8e8d1cd2143262f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475587"
---
# <a name="absoluteposition-property-ado"></a>AbsolutePosition-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt die Position des aktuellen Datensatzes eines [Recordset](recordset-object-ado.md)-Objekts an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** zwischen 1 und der Anzahl von Datensätzen im **Recordset**-Objekt ([RecordCount](recordcount-property-ado.md)) zurückgegeben oder festgelegt, oder es wird einer der Werte von [PositionEnum](positionenum.md) zurückgegeben.

## <a name="remarks"></a>Hinweise

Zum Festlegen der AbsolutePosition-Eigenschaft erfordert ADO, dass der verwendete OLE DB-Anbieter die IRowsetLocate-Schnittstelle implementiert.

Wenn Sie auf die AbsolutePosition-Eigenschaft eines Recordset-Objekts zugreifen, das mit einem Vorwärtscursor oder einem dynamischen Cursor geöffnet wurde, wird der Fehler adErrFeatureNotAvailable ausgelöst. Sofern der Anbieter die IRowsetScroll-Schnittstelle unterstützt, wird bei anderen Cursortypen die richtige Position zurückgegeben. Wird die IRowsetScroll-Schnittstelle nicht vom Anbieter unterstützt, wird die Eigenschaft auf adPosUnknown festgelegt. In der Dokumentation zu Ihrem Anbieter finden Sie Informationen dazu, ob IRowsetScroll unterstützt wird.

Verwenden Sie die **AbsolutePosition** -Eigenschaft, um zu einem Datensatz entsprechend der Ordnungsposition zu navigieren, die er im **Recordset** -Objekt einnimmt, oder um die Ordnungsposition des aktuellen Datensatzes zu ermitteln. Die entsprechende Funktionalität muss vom Anbieter unterstützt werden, damit diese Eigenschaft verfügbar ist.

[AbsolutePosition](absolutepage-property-ado.md) ist wie die **AbsolutePage** -Eigenschaft 1-basiert und entspricht 1, wenn der aktuelle Datensatz der erste Datensatz im **Recordset** -Objekt ist. Sie können die Gesamtanzahl von Datensätzen im **Recordset** -Objekt mit der [RecordCount](recordcount-property-ado.md)-Eigenschaft abrufen.

Wenn Sie die **AbsolutePosition** -Eigenschaft festlegen, lädt ADO, selbst wenn Sie diese Eigenschaft auf einen Datensatz im aktuellen Cache festlegen, den Cache erneut mit einer neuen Datensatzgruppe, und zwar beginnend mit dem von Ihnen angegebenen Datensatz. Die [CacheSize](cachesize-property-ado.md)-Eigenschaft bestimmt die Größe dieser Gruppe.


> [!NOTE]
> <P>[!HINWEIS] Sie sollten die <STRONG>AbsolutePosition</STRONG> -Eigenschaft nicht als Ersatz-Datensatznummer verwenden. Die Position eines Datensatzes wird geändert, wenn Sie einen vorausgehenden Datensatz löschen. Außerdem gibt es keine Gewähr, dass ein bestimmter Datensatz den gleichen Wert für <STRONG>AbsolutePosition</STRONG> aufweist, wenn das <STRONG>Recordset</STRONG> -Objekt erneut abgefragt oder geöffnet wird. Textmarken sind weiterhin die empfohlene Methode, um zu einer bestimmten Position zurückzukehren, und sie sind die einzige Methode der Positionierung für alle Typen von <STRONG>Recordset</STRONG> -Objekten.</P>


