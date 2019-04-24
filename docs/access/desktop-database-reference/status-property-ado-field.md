---
title: Status-Eigenschaft (ADO-Feld)
TOCTitle: Status property (ADO Field)
ms:assetid: 7a7b45e8-2934-2e8e-77fa-a4f38272548d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249507(v=office.15)
ms:contentKeyID: 48545795
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9c5f9d73a1081bb27c88541ac99307165222ab65
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306321"
---
# <a name="status-property-ado-field"></a><span data-ttu-id="29914-102">Status-Eigenschaft (ADO-Feld)</span><span class="sxs-lookup"><span data-stu-id="29914-102">Status property (ADO Field)</span></span>


<span data-ttu-id="29914-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="29914-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="29914-104">Gibt den Status eines [Field](field-object-ado.md)-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="29914-104">Indicates the status of a [Field](field-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="29914-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29914-105">Return value</span></span>

<span data-ttu-id="29914-106">Gibt einen [FieldStatusEnum](fieldstatusenum.md)-Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="29914-106">Returns a [FieldStatusEnum](fieldstatusenum.md) value.</span></span> <span data-ttu-id="29914-107">Der Standardwert lautet **AdFieldOK**.</span><span class="sxs-lookup"><span data-stu-id="29914-107">The default value is **adFieldOK**.</span></span>

## <a name="remarks"></a><span data-ttu-id="29914-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29914-108">Remarks</span></span>

<span data-ttu-id="29914-109">Diese Eigenschaft gibt für Felder eines [Recordset](recordset-object-ado.md)-Objekts stets **adFieldOK** zurück.</span><span class="sxs-lookup"><span data-stu-id="29914-109">This property always returns **adFieldOK** for fields of a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="29914-p102">Ergänzungen oder Löschungen in den [Fields](fields-collection-ado.md)-Auflistungen des [Record](record-object-ado.md)-Objekts werden bis zum Aufrufen der [Update](update-method-ado.md)-Methode zwischengespeichert. Mithilfe der **Status** -Eigenschaft können Sie die Felder ermitteln, die erfolgreich hinzugefügt oder gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="29914-p102">Additions and deletions to the [Fields](fields-collection-ado.md) collections of the [Record](record-object-ado.md) object are cached until the [Update](update-method-ado.md) method is called. The **Status** property enables you to determine which fields have been successfully added or deleted.</span></span>

<span data-ttu-id="29914-112">To enhance performance, schema changes are cached until **Update** is called, and then the changes are made in a batch optimistic update.</span><span class="sxs-lookup"><span data-stu-id="29914-112">To enhance performance, schema changes are cached until **Update** is called, and then the changes are made in a batch optimistic update.</span></span> <span data-ttu-id="29914-113">If the **Update** method is not called, the server is not updated.</span><span class="sxs-lookup"><span data-stu-id="29914-113">If the **Update** method is not called, the server is not updated.</span></span> <span data-ttu-id="29914-114">If any updates fail then an error is returned and the **Status** property indicates the combined values of the operation and error status code.</span><span class="sxs-lookup"><span data-stu-id="29914-114">If any updates fail then an error is returned and the **Status** property indicates the combined values of the operation and error status code.</span></span> <span data-ttu-id="29914-115">For example, **adFieldPendingInsert** **OR** **adFieldPermissionDenied**.</span><span class="sxs-lookup"><span data-stu-id="29914-115">For example, **adFieldPendingInsert** **OR** **adFieldPermissionDenied**.</span></span> <span data-ttu-id="29914-116">The **Status** property for each **Field** can be used to determine why the **Field** was not added, modified, or deleted.</span><span class="sxs-lookup"><span data-stu-id="29914-116">The **Status** property for each **Field** can be used to determine why the **Field** was not added, modified, or deleted.</span></span> <span data-ttu-id="29914-117">Der **Status** wird nur für den **Datensatz**sinnvoll angezeigt. **Fields** -Auflistung und nicht das **Recordset**-Objekt. **Fields** -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="29914-117">**Status** is only meaningfully exposed on the **Record**.**Fields** collection and not the **Recordset**.**Fields** collection.</span></span>

<span data-ttu-id="29914-p104">Two problems can arise when adding, modifying, or deleting a **Field**. If the user deletes a **Field**, it is marked for deletion from the **Fields** collection. If the subsequent **Update** returns an error because the user tried to delete a **Field** for which they do not have permission, the **Field** will have a status of **adFieldPermissionDenied** **OR** **adFieldPendingDelete**. Calling the [CancelUpdate](cancelupdate-method-ado.md) method restores original values and sets the **Status** to **adFieldOK**. Similarly, the **Update** method may return an error because a new **Field** was added and given an inappropriate value. In that case the new **Field** will be in the **Fields** collection and have a status of **adFieldPendingInsert** and perhaps **adFieldCantCreate**. You can supply an appropriate value for the new **Field** and call **Update** again. Note that calling **Resync** instead requeries the provider.</span><span class="sxs-lookup"><span data-stu-id="29914-p104">Two problems can arise when adding, modifying, or deleting a **Field**. If the user deletes a **Field**, it is marked for deletion from the **Fields** collection. If the subsequent **Update** returns an error because the user tried to delete a **Field** for which they do not have permission, the **Field** will have a status of **adFieldPermissionDenied** **OR** **adFieldPendingDelete**. Calling the [CancelUpdate](cancelupdate-method-ado.md) method restores original values and sets the **Status** to **adFieldOK**. Similarly, the **Update** method may return an error because a new **Field** was added and given an inappropriate value. In that case the new **Field** will be in the **Fields** collection and have a status of **adFieldPendingInsert** and perhaps **adFieldCantCreate**. You can supply an appropriate value for the new **Field** and call **Update** again. Note that calling **Resync** instead requeries the provider.</span></span>

