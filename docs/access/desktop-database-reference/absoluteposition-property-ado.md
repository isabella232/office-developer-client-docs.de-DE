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
# <a name="absoluteposition-property-ado"></a><span data-ttu-id="8d4fb-102">AbsolutePosition-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="8d4fb-102">AbsolutePosition Property (ADO)</span></span>


<span data-ttu-id="8d4fb-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d4fb-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8d4fb-104">Gibt die Position des aktuellen Datensatzes eines [Recordset](recordset-object-ado.md)-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="8d4fb-104">Indicates the ordinal position of a [Recordset](recordset-object-ado.md) object's current record.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="8d4fb-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8d4fb-105">Settings and Return Values</span></span>

<span data-ttu-id="8d4fb-106">Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** zwischen 1 und der Anzahl von Datensätzen im **Recordset**-Objekt ([RecordCount](recordcount-property-ado.md)) zurückgegeben oder festgelegt, oder es wird einer der Werte von [PositionEnum](positionenum.md) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8d4fb-106">Sets or returns a **Long** value from 1 to the number of records in the **Recordset** object ([RecordCount](recordcount-property-ado.md)), or returns one of the [PositionEnum](positionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d4fb-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8d4fb-107">Remarks</span></span>

<span data-ttu-id="8d4fb-108">Zum Festlegen der AbsolutePosition-Eigenschaft erfordert ADO, dass der verwendete OLE DB-Anbieter die IRowsetLocate-Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="8d4fb-108">In order to set the **AbsolutePosition** property, ADO requires that the OLE DB provider you are using implement the IRowsetLocate interface.</span></span>

<span data-ttu-id="8d4fb-p101">Wenn Sie auf die AbsolutePosition-Eigenschaft eines Recordset-Objekts zugreifen, das mit einem Vorwärtscursor oder einem dynamischen Cursor geöffnet wurde, wird der Fehler adErrFeatureNotAvailable ausgelöst. Sofern der Anbieter die IRowsetScroll-Schnittstelle unterstützt, wird bei anderen Cursortypen die richtige Position zurückgegeben. Wird die IRowsetScroll-Schnittstelle nicht vom Anbieter unterstützt, wird die Eigenschaft auf adPosUnknown festgelegt. In der Dokumentation zu Ihrem Anbieter finden Sie Informationen dazu, ob IRowsetScroll unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8d4fb-p101">Accessing the **AbsolutePosition** property of a **Recordset** that was opened with either a forward-only or dynamic cursor raises the error **adErrFeatureNotAvailable**. With other cursor types, the correct position will be returned as long as the provider supports the IRowsetScroll interface. If the provider does not support the *IRowsetScroll* interface, the property is set to **adPosUnknown**. See the documentation for your provider to determine whether it supports *IRowsetScroll*.</span></span>

<span data-ttu-id="8d4fb-p102">Verwenden Sie die **AbsolutePosition** -Eigenschaft, um zu einem Datensatz entsprechend der Ordnungsposition zu navigieren, die er im **Recordset** -Objekt einnimmt, oder um die Ordnungsposition des aktuellen Datensatzes zu ermitteln. Die entsprechende Funktionalität muss vom Anbieter unterstützt werden, damit diese Eigenschaft verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8d4fb-p102">Use the **AbsolutePosition** property to move to a record based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record. The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="8d4fb-p103">[AbsolutePosition](absolutepage-property-ado.md) ist wie die **AbsolutePage** -Eigenschaft 1-basiert und entspricht 1, wenn der aktuelle Datensatz der erste Datensatz im **Recordset** -Objekt ist. Sie können die Gesamtanzahl von Datensätzen im **Recordset** -Objekt mit der [RecordCount](recordcount-property-ado.md)-Eigenschaft abrufen.</span><span class="sxs-lookup"><span data-stu-id="8d4fb-p103">Like the [AbsolutePage](absolutepage-property-ado.md) property, **AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**. You can obtain the total number of records in the **Recordset** object from the [RecordCount](recordcount-property-ado.md) property.</span></span>

<span data-ttu-id="8d4fb-p104">Wenn Sie die **AbsolutePosition** -Eigenschaft festlegen, lädt ADO, selbst wenn Sie diese Eigenschaft auf einen Datensatz im aktuellen Cache festlegen, den Cache erneut mit einer neuen Datensatzgruppe, und zwar beginnend mit dem von Ihnen angegebenen Datensatz. Die [CacheSize](cachesize-property-ado.md)-Eigenschaft bestimmt die Größe dieser Gruppe.</span><span class="sxs-lookup"><span data-stu-id="8d4fb-p104">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record you specified. The [CacheSize](cachesize-property-ado.md) property determines the size of this group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="8d4fb-p105">[!HINWEIS] Sie sollten die <STRONG>AbsolutePosition</STRONG> -Eigenschaft nicht als Ersatz-Datensatznummer verwenden. Die Position eines Datensatzes wird geändert, wenn Sie einen vorausgehenden Datensatz löschen. Außerdem gibt es keine Gewähr, dass ein bestimmter Datensatz den gleichen Wert für <STRONG>AbsolutePosition</STRONG> aufweist, wenn das <STRONG>Recordset</STRONG> -Objekt erneut abgefragt oder geöffnet wird. Textmarken sind weiterhin die empfohlene Methode, um zu einer bestimmten Position zurückzukehren, und sie sind die einzige Methode der Positionierung für alle Typen von <STRONG>Recordset</STRONG> -Objekten.</span><span class="sxs-lookup"><span data-stu-id="8d4fb-p105">You should not use the <STRONG>AbsolutePosition</STRONG> property as a surrogate record number. The position of a given record changes when you delete a preceding record. There is also no assurance that a given record will have the same <STRONG>AbsolutePosition</STRONG> if the <STRONG>Recordset</STRONG> object is requeried or reopened. Bookmarks are still the recommended way of retaining and returning to a given position and are the only way of positioning across all types of <STRONG>Recordset</STRONG> objects.</span></span></P>


