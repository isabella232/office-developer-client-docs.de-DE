---
title: ExecuteOptions-Eigenschaft (RDS)
TOCTitle: ExecuteOptions property (RDS)
ms:assetid: fb244cbd-9a03-9128-1373-694c9061c9da
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250285(v=office.15)
ms:contentKeyID: 48548864
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9cf773090ccb37bf4cad4aff41499ad01f966479
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293252"
---
# <a name="executeoptions-property-rds"></a><span data-ttu-id="7964c-102">ExecuteOptions-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="7964c-102">ExecuteOptions property (RDS)</span></span>


<span data-ttu-id="7964c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7964c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7964c-104">Gibt an, ob die asynchrone Ausführung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7964c-104">Indicates whether asynchronous execution is enabled.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="7964c-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="7964c-105">Settings and return values</span></span>

<span data-ttu-id="7964c-106">Legt einen der folgenden Werte fest oder gibt ihn zurück.</span><span class="sxs-lookup"><span data-stu-id="7964c-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7964c-107">Konstante</span><span class="sxs-lookup"><span data-stu-id="7964c-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="7964c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7964c-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7964c-109"><strong>adcExecSync</strong></span><span class="sxs-lookup"><span data-stu-id="7964c-109"><strong>adcExecSync</strong></span></span></p></td>
<td><p><span data-ttu-id="7964c-110">Führt die nächste Aktualisierung des <a href="recordset-object-ado.md">Recordsets</a> synchron aus.</span><span class="sxs-lookup"><span data-stu-id="7964c-110">Executes the next refresh of the <a href="recordset-object-ado.md">Recordset</a> synchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7964c-111"><strong>adcExecAsync</strong></span><span class="sxs-lookup"><span data-stu-id="7964c-111"><strong>adcExecAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="7964c-112">Standardwert.</span><span class="sxs-lookup"><span data-stu-id="7964c-112">Default.</span></span> <span data-ttu-id="7964c-113">Führt die nächste Aktualisierung des <strong>Recordsets</strong> asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="7964c-113">Executes the next refresh of the <strong>Recordset</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="7964c-p102">Each client-side executable file that uses these constants must provide declarations for them. You can cut and paste the constant declarations that you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span><span class="sxs-lookup"><span data-stu-id="7964c-p102">Each client-side executable file that uses these constants must provide declarations for them. You can cut and paste the constant declarations that you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="7964c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7964c-116">Remarks</span></span>

<span data-ttu-id="7964c-117">Wenn **ExecuteOptions** auf **adcExecAsync** festgelegt ist, wird dadurch der nächste **Refresh**-Aufruf für das **Recordset**-Objekt des [RDS.DataControl](datacontrol-object-rds.md)-Objekts ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7964c-117">If **ExecuteOptions** is set to **adcExecAsync**, then this asynchronously executes the next **Refresh** call on the [RDS.DataControl](datacontrol-object-rds.md) object's **Recordset**.</span></span>

<span data-ttu-id="7964c-118">Ein Fehler tritt auf, wenn Sie versuchen, [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md) oder [Recordset](recordset-sourcerecordset-properties-rds.md) aufzurufen, während eine andere asynchrone Operation ausgeführt wird, die das **Recordset**-Objekt des [RDS.DataControl](datacontrol-object-rds.md)-Objekts möglicherweise ändert.</span><span class="sxs-lookup"><span data-stu-id="7964c-118">If you try to call [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md), or [Recordset](recordset-sourcerecordset-properties-rds.md) while another asynchronous operation that might change the [RDS.DataControl](datacontrol-object-rds.md) object's **Recordset** is executing, an error occurs.</span></span>

<span data-ttu-id="7964c-119">Wenn bei einer asynchronen Operation ein Fehler auftritt, ändert sich der [ReadyState](readystate-property-rds.md)-Wert des **RDS.DataControl**-Objekts von **adcReadyStateLoaded** zu **adcReadyStateComplete**, und der **Recordset**-Eigenschaftswert bleibt *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="7964c-119">If an error occurs during an asynchronous operation, the **RDS.DataControl** object's [ReadyState](readystate-property-rds.md) value changes from **adcReadyStateLoaded** to **adcReadyStateComplete**, and the **Recordset** property value remains *Nothing*.</span></span>

