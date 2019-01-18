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
# <a name="absoluteposition-property-ado"></a><span data-ttu-id="8545c-102">AbsolutePosition-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="8545c-102">AbsolutePosition property (ADO)</span></span>

<span data-ttu-id="8545c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8545c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8545c-104">Gibt die Position des aktuellen Datensatzes eines [Recordset](recordset-object-ado.md)-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="8545c-104">Indicates the ordinal position of a [Recordset](recordset-object-ado.md) object's current record.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="8545c-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8545c-105">Settings and return values</span></span>

<span data-ttu-id="8545c-106">Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** zwischen 1 und der Anzahl von Datensätzen im **Recordset**-Objekt ([RecordCount](recordcount-property-ado.md)) zurückgegeben oder festgelegt, oder es wird einer der Werte von [PositionEnum](positionenum.md) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8545c-106">Sets or returns a **Long** value from 1 to the number of records in the **Recordset** object ([RecordCount](recordcount-property-ado.md)), or returns one of the [PositionEnum](positionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="8545c-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8545c-107">Remarks</span></span>

<span data-ttu-id="8545c-108">Zum Festlegen der **AbsolutePosition** -Eigenschaft erfordert ADO, dass der verwendete OLE DB-Anbieter die IRowsetLocate-Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="8545c-108">To set the **AbsolutePosition** property, ADO requires that the OLE DB provider you are using implement the IRowsetLocate interface.</span></span>

<span data-ttu-id="8545c-p101">Wenn Sie auf die AbsolutePosition-Eigenschaft eines Recordset-Objekts zugreifen, das mit einem Vorwärtscursor oder einem dynamischen Cursor geöffnet wurde, wird der Fehler adErrFeatureNotAvailable ausgelöst. Sofern der Anbieter die IRowsetScroll-Schnittstelle unterstützt, wird bei anderen Cursortypen die richtige Position zurückgegeben. Wird die IRowsetScroll-Schnittstelle nicht vom Anbieter unterstützt, wird die Eigenschaft auf adPosUnknown festgelegt. In der Dokumentation zu Ihrem Anbieter finden Sie Informationen dazu, ob IRowsetScroll unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8545c-p101">Accessing the **AbsolutePosition** property of a **Recordset** that was opened with either a forward-only or dynamic cursor raises the error **adErrFeatureNotAvailable**. With other cursor types, the correct position will be returned as long as the provider supports the IRowsetScroll interface. If the provider does not support the *IRowsetScroll* interface, the property is set to **adPosUnknown**. See the documentation for your provider to determine whether it supports *IRowsetScroll*.</span></span>

<span data-ttu-id="8545c-p102">Verwenden Sie die **AbsolutePosition** -Eigenschaft, um zu einem Datensatz entsprechend der Ordnungsposition zu navigieren, die er im **Recordset** -Objekt einnimmt, oder um die Ordnungsposition des aktuellen Datensatzes zu ermitteln. Die entsprechende Funktionalität muss vom Anbieter unterstützt werden, damit diese Eigenschaft verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8545c-p102">Use the **AbsolutePosition** property to move to a record based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record. The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="8545c-p103">[AbsolutePosition](absolutepage-property-ado.md) ist wie die **AbsolutePage** -Eigenschaft 1-basiert und entspricht 1, wenn der aktuelle Datensatz der erste Datensatz im **Recordset** -Objekt ist. Sie können die Gesamtanzahl von Datensätzen im **Recordset** -Objekt mit der [RecordCount](recordcount-property-ado.md)-Eigenschaft abrufen.</span><span class="sxs-lookup"><span data-stu-id="8545c-p103">Like the [AbsolutePage](absolutepage-property-ado.md) property, **AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**. You can obtain the total number of records in the **Recordset** object from the [RecordCount](recordcount-property-ado.md) property.</span></span>

<span data-ttu-id="8545c-117">Wenn Sie die **AbsolutePosition** -Eigenschaft festlegen, selbst wenn es zu einem Datensatz im aktuellen Cache wird, lädt ADO den Cache mit einer neuen Gruppe von Datensätzen, beginnend mit dem Datensatz, den Sie angegeben.</span><span class="sxs-lookup"><span data-stu-id="8545c-117">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record that you specified.</span></span> <span data-ttu-id="8545c-118">Die [CacheSize](cachesize-property-ado.md) -Eigenschaft bestimmt die Größe dieser Gruppe.</span><span class="sxs-lookup"><span data-stu-id="8545c-118">The [CacheSize](cachesize-property-ado.md) property determines the size of this group.</span></span>


> [!NOTE]
> <span data-ttu-id="8545c-119">[!HINWEIS] Sie sollten die **AbsolutePosition** -Eigenschaft nicht als Ersatz-Datensatznummer verwenden.</span><span class="sxs-lookup"><span data-stu-id="8545c-119">You should not use the **AbsolutePosition** property as a surrogate record number.</span></span> <span data-ttu-id="8545c-120">Die Position eines Datensatzes wird geändert, wenn Sie einen vorausgehenden Datensatz löschen.</span><span class="sxs-lookup"><span data-stu-id="8545c-120">The position of a given record changes when you delete a preceding record.</span></span> <span data-ttu-id="8545c-121">Außerdem gibt es keine Gewähr, dass ein bestimmter Datensatz den gleichen Wert für **AbsolutePosition** aufweist, wenn das **Recordset** -Objekt erneut abgefragt oder geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="8545c-121">There is also no assurance that a given record will have the same **AbsolutePosition** if the **Recordset** object is requeried or reopened.</span></span> <span data-ttu-id="8545c-122">Lesezeichen sind weiterhin die empfohlene Methode zurückzukehren, um eine bestimmte Position und sind die einzige Möglichkeit der Positionierung für alle Typen von **Recordset** -Objekten.</span><span class="sxs-lookup"><span data-stu-id="8545c-122">Bookmarks are still the recommended way of retaining and returning to a given position, and are the only way of positioning across all types of **Recordset** objects.</span></span>


