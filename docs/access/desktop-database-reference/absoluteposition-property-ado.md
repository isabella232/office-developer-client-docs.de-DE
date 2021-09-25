---
title: AbsolutePosition-Eigenschaft (ADO)
TOCTitle: AbsolutePosition property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 10/17/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 10c88c26e80cf7a9102d2101e9cc048d45843164
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586348"
---
# <a name="absoluteposition-property-ado"></a>AbsolutePosition-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013

Gibt die Position des aktuellen Datensatzes eines [Recordset](recordset-object-ado.md)-Objekts an.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** zwischen 1 und der Anzahl von Datensätzen im **Recordset**-Objekt ([RecordCount](recordcount-property-ado.md)) zurückgegeben oder festgelegt, oder es wird einer der Werte von [PositionEnum](positionenum.md) zurückgegeben.

## <a name="remarks"></a>HinwBemerkungeneise

Zum Festlegen der **AbsolutePosition-Eigenschaft** erfordert ADO, dass der von Ihnen verwendete OLE DB-Anbieter die IRowsetLocate-Schnittstelle implementiert.

Accessing the **AbsolutePosition** property of a **Recordset** that was opened with either a forward-only or dynamic cursor raises the error **adErrFeatureNotAvailable**. With other cursor types, the correct position will be returned as long as the provider supports the IRowsetScroll interface. Wenn der Anbieter die *IRowsetScroll-Schnittstelle* nicht unterstützt, wird die Eigenschaft auf **adPosUnknown** festgelegt. In der Dokumentation ihres Anbieters finden Sie Informationen dazu, ob *IRowsetScroll* unterstützt wird.

Verwenden Sie die **AbsolutePosition** -Eigenschaft, um zu einem Datensatz entsprechend der Ordnungsposition zu navigieren, die er im **Recordset** -Objekt einnimmt, oder um die Ordnungsposition des aktuellen Datensatzes zu ermitteln. Die entsprechende Funktionalität muss vom Anbieter unterstützt werden, damit diese Eigenschaft verfügbar ist.

[AbsolutePosition](absolutepage-property-ado.md) ist wie die **AbsolutePage** -Eigenschaft 1-basiert und entspricht 1, wenn der aktuelle Datensatz der erste Datensatz im **Recordset** -Objekt ist. Sie können die Gesamtanzahl von Datensätzen im **Recordset** -Objekt mit der [RecordCount](recordcount-property-ado.md)-Eigenschaft abrufen.

Wenn Sie die **AbsolutePosition-Eigenschaft** festlegen, lädt ADO den Cache mit einer neuen Datensatzgruppe neu, die mit dem angegebenen Datensatz beginnt, selbst wenn es sich um einen Datensatz im aktuellen Cache handelt. Die [CacheSize](cachesize-property-ado.md)-Eigenschaft bestimmt die Größe dieser Gruppe.


> [!NOTE]
> [!HINWEIS] Sie sollten die **AbsolutePosition** -Eigenschaft nicht als Ersatz-Datensatznummer verwenden. Die Position eines Datensatzes wird geändert, wenn Sie einen vorausgehenden Datensatz löschen. Außerdem gibt es keine Gewähr, dass ein bestimmter Datensatz den gleichen Wert für **AbsolutePosition** aufweist, wenn das **Recordset**-Objekt erneut abgefragt oder geöffnet wird. Lesezeichen sind nach wie vor die empfohlene Methode zum Beibehalten und Kehren zu einer bestimmten Position und stellen die einzige Möglichkeit zur Positionierung über alle Arten von **Recordset-Objekten** hinweg dar.


