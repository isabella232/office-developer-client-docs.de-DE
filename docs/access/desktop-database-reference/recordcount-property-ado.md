---
title: RecordCount-Eigenschaft (ADO)
TOCTitle: RecordCount property (ADO)
ms:assetid: e3072d10-5bf7-02a8-027e-a9d9a34e3f27
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250155(v=office.15)
ms:contentKeyID: 48548304
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41fb9d8bdcb626fefe2e98fe4c1849554a73a6c3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876162"
---
# <a name="recordcount-property-ado"></a><span data-ttu-id="f17e3-102">RecordCount-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="f17e3-102">RecordCount property (ADO)</span></span>


<span data-ttu-id="f17e3-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f17e3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f17e3-104">Gibt die Anzahl von Datensätzen in einem [Recordset](recordset-object-ado.md)-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f17e3-104">Indicates the number of records in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="f17e3-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f17e3-105">Return value</span></span>

<span data-ttu-id="f17e3-106">Gibt einen **Long** -Wert zurück, der die Anzahl von Datensätzen im **Recordset** -Objekt angibt.</span><span class="sxs-lookup"><span data-stu-id="f17e3-106">Returns a **Long** value that indicates the number of records in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f17e3-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f17e3-107">Remarks</span></span>

<span data-ttu-id="f17e3-p101">Ermitteln Sie mit der **RecordCount** -Eigenschaft die Anzahl von Datensätzen in einem **Recordset** -Objekt. Die Eigenschaft gibt -1 zurück, wenn ADO die Anzahl von Datensätzen nicht bestimmen kann oder wenn der Anbieter- oder Cursortyp **RecordCount** nicht unterstützt. Das Lesen der **RecordCount** -Eigenschaft für ein geschlossenes **Recordset** -Objekt verursacht einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="f17e3-p101">Use the **RecordCount** property to find out how many records are in a **Recordset** object. The property returns -1 when ADO cannot determine the number of records or if the provider or cursor type does not support **RecordCount**. Reading the **RecordCount** property on a closed **Recordset** causes an error.</span></span>

<span data-ttu-id="f17e3-p102">Wenn das **Recordset** -Objekt eine ungefähre Positionierung von Textmarken zulässt (d. h. **Supports (adApproxPosition)** oder **Supports (adBookmark)** geben jeweils **True** zurück), entspricht dieser Wert genau der Anzahl von Datensätzen im **Recordset** -Objekt, unabhängig davon, ob es vollständig gefüllt ist. Unterstützt das **Recordset** -Objekt keine ungefähre Positionierung, kann diese Eigenschaften die Ressourcen erheblich beeinträchtigen. Denn es müssen alle Datensätze abgerufen und gezählt werden, damit einen präziser **RecordCount** -Wert zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f17e3-p102">If the **Recordset** object supports approximate positioning or bookmarks — that is, **Supports (adApproxPosition)** or **Supports (adBookmark)**, respectively, return **True** — this value will be the exact number of records in the **Recordset**, regardless of whether it has been fully populated. If the **Recordset** object does not support approximate positioning, this property may be a significant drain on resources because all records will have to be retrieved and counted to return an accurate **RecordCount** value.</span></span>

<span data-ttu-id="f17e3-p103">Der Cursortyp des **Recordset** -Objekts beeinflusst die Anzahl von Datensätzen, die ermittelt werden können. Die **RecordCount** -Eigenschaft gibt -1 für einen Vorwärtscursor zurück; die tatsächliche Anzahl für einen statischen oder einen Keyset-Cursor; und je nach Datenquelle entweder -1 oder die tatsächliche Anzahl für einen dynamischen Cursor.</span><span class="sxs-lookup"><span data-stu-id="f17e3-p103">The cursor type of the **Recordset** object affects whether the number of records can be determined. The **RecordCount** property will return -1 for a forward-only cursor; the actual count for a static or keyset cursor; and either -1 or the actual count for a dynamic cursor, depending on the data source.</span></span>

