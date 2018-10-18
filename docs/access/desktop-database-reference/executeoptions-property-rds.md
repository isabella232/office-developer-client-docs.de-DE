---
title: ExecuteOptions-Eigenschaft (RDS)
TOCTitle: ExecuteOptions Property (RDS)
ms:assetid: fb244cbd-9a03-9128-1373-694c9061c9da
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250285(v=office.15)
ms:contentKeyID: 48548864
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e5a91d3941db0b7daa61b506c136dab59f24ed0
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603588"
---
# <a name="executeoptions-property-rds"></a><span data-ttu-id="b0f14-102">ExecuteOptions-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="b0f14-102">ExecuteOptions Property (RDS)</span></span>


<span data-ttu-id="b0f14-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0f14-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b0f14-104">Gibt an, ob die asynchrone Ausführung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b0f14-104">Indicates whether asynchronous execution is enabled.</span></span>

<span data-ttu-id="b0f14-105"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="b0f14-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="b0f14-106">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b0f14-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="b0f14-107">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b0f14-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="b0f14-108">master</span><span class="sxs-lookup"><span data-stu-id="b0f14-108">master</span></span>

<span data-ttu-id="b0f14-109">Legt einen der folgenden Werte fest oder gibt ihn zurück.</span><span class="sxs-lookup"><span data-stu-id="b0f14-109">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0f14-110">Konstante</span><span class="sxs-lookup"><span data-stu-id="b0f14-110">Constant</span></span></p></th>
<th><p><span data-ttu-id="b0f14-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0f14-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0f14-112"><strong>adcExecSync</strong></span><span class="sxs-lookup"><span data-stu-id="b0f14-112"><strong>adcExecSync</strong></span></span></p></td>
<td><p><span data-ttu-id="b0f14-113">Führt die nächste Aktualisierung des <a href="recordset-object-ado.md">Recordsets</a> synchron aus.</span><span class="sxs-lookup"><span data-stu-id="b0f14-113">Executes the next refresh of the <a href="recordset-object-ado.md">Recordset</a> synchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0f14-114"><strong>adcExecAsync</strong></span><span class="sxs-lookup"><span data-stu-id="b0f14-114"><strong>adcExecAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="b0f14-p101">Standard. Führt die nächste Aktualisierung des <strong>Recordsets</strong> asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="b0f14-p101">Default. Executes the next refresh of the <strong>Recordset</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="b0f14-117">Jede mithilfe der clientseitigen ausführbare Datei, die die folgenden Konstanten verwendet, muss Deklarationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b0f14-117">Each client-side executable file that uses these constants must provide declarations for them.</span></span> <span data-ttu-id="b0f14-118">Sie können Ausschneiden und Einfügen die Konstantendeklarationen auf, denen Sie aus der Datei Datei Adcvbs.inc, befindet sich im Ordner C:\Program Files\Common Dateien\System\MSADC möchten.</span><span class="sxs-lookup"><span data-stu-id="b0f14-118">You can cut and paste the constant declarations that you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="b0f14-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b0f14-119">Remarks</span></span>

<span data-ttu-id="b0f14-120">Wenn **ExecuteOptions** auf **adcExecAsync** festgelegt ist, wird dadurch der nächste **Refresh** -Aufruf für das [Recordset](datacontrol-object-rds.md) -Objekt des **RDS.DataControl**-Objekts ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b0f14-120">If **ExecuteOptions** is set to **adcExecAsync**, then this asynchronously executes the next **Refresh** call on the [RDS.DataControl](datacontrol-object-rds.md) object's **Recordset**.</span></span>

<span data-ttu-id="b0f14-121">Ein Fehler tritt auf, wenn Sie versuchen, [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md) oder [Recordset](recordset-sourcerecordset-properties-rds.md) aufzurufen, während eine andere asynchrone Operation ausgeführt wird, die das [Recordset](datacontrol-object-rds.md) -Objekt des **RDS.DataControl**-Objekts möglicherweise ändert.</span><span class="sxs-lookup"><span data-stu-id="b0f14-121">If you try to call [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md), or [Recordset](recordset-sourcerecordset-properties-rds.md) while another asynchronous operation that might change the [RDS.DataControl](datacontrol-object-rds.md) object's **Recordset** is executing, an error occurs.</span></span>

<span data-ttu-id="b0f14-122">Wenn bei einer asynchronen Operation ein Fehler auftritt, ändert sich der [ReadyState](readystate-property-rds.md)-Wert des **RDS.DataControl**-Objekts von **adcReadyStateLoaded** zu **adcReadyStateComplete**, und der **Recordset**-Eigenschaftswert bleibt *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="b0f14-122">If an error occurs during an asynchronous operation, the **RDS.DataControl** object's [ReadyState](readystate-property-rds.md) value changes from **adcReadyStateLoaded** to **adcReadyStateComplete**, and the **Recordset** property value remains *Nothing*.</span></span>

