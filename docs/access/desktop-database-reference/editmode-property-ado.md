---
title: EditMode-Eigenschaft (ADO)
TOCTitle: EditMode Property (ADO)
ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15)
ms:contentKeyID: 48543867
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a6c8377e0fa0fc2db1ec2d376ee3c8b9f16e8c99
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473354"
---
# <a name="editmode-property-ado"></a><span data-ttu-id="5c1b5-102">EditMode-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="5c1b5-102">EditMode Property (ADO)</span></span>


<span data-ttu-id="5c1b5-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5c1b5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5c1b5-104">Gibt den Bearbeitungsstatus des aktuellen Datensatzes an.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-104">Indicates the editing status of the current record.</span></span>

## <a name="return-value"></a><span data-ttu-id="5c1b5-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c1b5-105">Return Value</span></span>

<span data-ttu-id="5c1b5-106">Gibt einen [EditModeEnum](editmodeenum.md)-Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-106">Returns an [EditModeEnum](editmodeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c1b5-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5c1b5-107">Remarks</span></span>

<span data-ttu-id="5c1b5-p101">ADO verwaltet einen Bearbeitungspuffer, der dem aktuellen Datensatz zugeordnet ist. Diese Eigenschaft gibt an, ob Änderungen an diesem Puffer vorgenommen wurden oder ob ein neuer Datensatz erstellt wurde. Verwenden Sie die **EditMode** -Eigenschaft, um den Bearbeitungsstatus des aktuellen Datensatzes zu bestimmen. Sie können testen, ob ausstehende Änderungen vorhanden sind, falls ein Bearbeitungsprozess unterbrochen wurde, und bestimmen, ob die [Update](update-method-ado.md)- oder die [CancelUpdate](cancelupdate-method-ado.md)-Methode zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-p101">ADO maintains an editing buffer associated with the current record. This property indicates whether changes have been made to this buffer, or whether a new record has been created. Use the **EditMode** property to determine the editing status of the current record. You can test for pending changes if an editing process has been interrupted and determine whether you need to use the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method.</span></span>

<span data-ttu-id="5c1b5-112">Eine ausführlichere Beschreibung der [EditMode](addnew-method-ado.md) -Eigenschaft unter verschiedenen Bearbeitungsbedingungen finden Sie unter der **AddNew**-Methode.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-112">See the [AddNew](addnew-method-ado.md) method for a more detailed description of the **EditMode** property under different editing conditions.</span></span>

<span data-ttu-id="5c1b5-113">Wenn ein Anruf an [Löschen](delete-method-ado-recordset.md) löscht den Datensatz nicht erfolgreich oder Datensätze in der Datenquelle (aufgrund von referenzielle Integrität Verstöße, beispielsweise), das [Recordset-Objekt](recordset-object-ado.md) im Bearbeitungsmodus bleiben (**EditMode** = \*\*AdEditInProgress \*\*).</span><span class="sxs-lookup"><span data-stu-id="5c1b5-113">When a call to [Delete](delete-method-ado-recordset.md) does not successfully delete the record or records in the data source (due to referential integrity violations, for example), the [Recordset](recordset-object-ado.md) will remain in edit mode (**EditMode** = **adEditInProgress**).</span></span> <span data-ttu-id="5c1b5-114">Dies bedeutet, dass **CancelUpdate** muss, bevor Sie fortfahren aufgerufen werden deaktiviert den aktuellen Datensatz (mit [Verschieben](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md)oder [Schließen](close-method-ado.md), beispielsweise).</span><span class="sxs-lookup"><span data-stu-id="5c1b5-114">This means that **CancelUpdate** must be called before moving off the current record (with [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md), or [Close](close-method-ado.md), for example).</span></span>


> [!NOTE]
> <P><span data-ttu-id="5c1b5-115"><STRONG>EditMode</STRONG> kann nur einen gültigen Wert zurückgeben, wenn ein aktueller Datensatz vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-115"><STRONG>EditMode</STRONG> can return a valid value only if there is a current record.</span></span> <span data-ttu-id="5c1b5-116"><STRONG>EditMode</STRONG> gibt einen Fehler zurück, wenn <A href="bof-eof-properties-ado.md">BOF oder EOF</A> true ist, oder wenn der aktuelle Datensatz gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-116"><STRONG>EditMode</STRONG> will return an error if <A href="bof-eof-properties-ado.md">BOF or EOF</A> is true, or if the current record has been deleted.</span></span></P>


