---
title: EditMode-Eigenschaft (ADO)
TOCTitle: EditMode property (ADO)
ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15)
ms:contentKeyID: 48543867
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d7bba0af804df89bf4c8611e184928c9bf12d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293609"
---
# <a name="editmode-property-ado"></a><span data-ttu-id="81a44-102">EditMode-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="81a44-102">EditMode property (ADO)</span></span>


<span data-ttu-id="81a44-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="81a44-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="81a44-104">Gibt den Bearbeitungsstatus des aktuellen Datensatzes an.</span><span class="sxs-lookup"><span data-stu-id="81a44-104">Indicates the editing status of the current record.</span></span>

## <a name="return-value"></a><span data-ttu-id="81a44-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81a44-105">Return value</span></span>

<span data-ttu-id="81a44-106">Gibt einen [EditModeEnum](editmodeenum.md)-Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="81a44-106">Returns an [EditModeEnum](editmodeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81a44-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81a44-107">Remarks</span></span>

<span data-ttu-id="81a44-p101">ADO verwaltet einen Bearbeitungspuffer, der dem aktuellen Datensatz zugeordnet ist. Diese Eigenschaft gibt an, ob Änderungen an diesem Puffer vorgenommen wurden oder ob ein neuer Datensatz erstellt wurde. Verwenden Sie die **EditMode** -Eigenschaft, um den Bearbeitungsstatus des aktuellen Datensatzes zu bestimmen. Sie können testen, ob ausstehende Änderungen vorhanden sind, falls ein Bearbeitungsprozess unterbrochen wurde, und bestimmen, ob die [Update](update-method-ado.md)- oder die [CancelUpdate](cancelupdate-method-ado.md)-Methode zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="81a44-p101">ADO maintains an editing buffer associated with the current record. This property indicates whether changes have been made to this buffer, or whether a new record has been created. Use the **EditMode** property to determine the editing status of the current record. You can test for pending changes if an editing process has been interrupted and determine whether you need to use the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method.</span></span>

<span data-ttu-id="81a44-112">Eine ausführlichere Beschreibung der [EditMode](addnew-method-ado.md) -Eigenschaft unter verschiedenen Bearbeitungsbedingungen finden Sie unter der **AddNew**-Methode.</span><span class="sxs-lookup"><span data-stu-id="81a44-112">See the [AddNew](addnew-method-ado.md) method for a more detailed description of the **EditMode** property under different editing conditions.</span></span>

<span data-ttu-id="81a44-113">Wenn ein Aufruf von [Delete](delete-method-ado-recordset.md) den Datensatz oder die Datensätze in der Datenquelle nicht erfolgreich löscht (beispielsweise aufgrund von Verletzungen der referenziellen Integrität), verbleibt das [Recordset](recordset-object-ado.md) -Objekt im Bearbeitungsmodus (**EditMode** = \*\*adEditInProgress \*\*).</span><span class="sxs-lookup"><span data-stu-id="81a44-113">When a call to [Delete](delete-method-ado-recordset.md) does not successfully delete the record or records in the data source (due to referential integrity violations, for example), the [Recordset](recordset-object-ado.md) will remain in edit mode (**EditMode** = **adEditInProgress**).</span></span> <span data-ttu-id="81a44-114">Dies bedeutet, dass **CancelUpdate** aufgerufen werden muss, bevor Sie den aktuellen Datensatz verlassen (z. B. mit [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md) oder [Close](close-method-ado.md)).</span><span class="sxs-lookup"><span data-stu-id="81a44-114">This means that **CancelUpdate** must be called before moving off the current record (with [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md), or [Close](close-method-ado.md), for example).</span></span>


> [!NOTE]
> <span data-ttu-id="81a44-p103">**EditMode** can return a valid value only if there is a current record. **EditMode** will return an error if [BOF or EOF](bof-eof-properties-ado.md) is true, or if the current record has been deleted.</span><span class="sxs-lookup"><span data-stu-id="81a44-p103">**EditMode** can return a valid value only if there is a current record. **EditMode** will return an error if [BOF or EOF](bof-eof-properties-ado.md) is true, or if the current record has been deleted.</span></span>


