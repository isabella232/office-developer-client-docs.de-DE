---
title: ReadyState-Eigenschaft (RDS)
TOCTitle: ReadyState property (RDS)
ms:assetid: e7b62205-a604-ef43-2f5d-9b51b46d2b5a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250175(v=office.15)
ms:contentKeyID: 48548412
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 71dd674e90e2438c616f0973c4f9948f1b20b1f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300819"
---
# <a name="readystate-property-rds"></a><span data-ttu-id="23ec5-102">ReadyState-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="23ec5-102">ReadyState property (RDS)</span></span>

<span data-ttu-id="23ec5-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="23ec5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="23ec5-104">Gibt den Status eines [DataControl](datacontrol-object-rds.md)-Objekts beim Abrufen von Daten in dessen [Recordset](recordset-object-ado.md)-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="23ec5-104">Indicates the progress of a [DataControl](datacontrol-object-rds.md) object as it retrieves data into its [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="23ec5-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="23ec5-105">Settings and return values</span></span>

<span data-ttu-id="23ec5-106">Legt einen der folgenden Werte fest oder gibt ihn zurück.</span><span class="sxs-lookup"><span data-stu-id="23ec5-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="23ec5-107">Wert</span><span class="sxs-lookup"><span data-stu-id="23ec5-107">Value</span></span></p></th>
<th><p><span data-ttu-id="23ec5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23ec5-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23ec5-109"><strong>adcReadyStateLoaded</strong></span><span class="sxs-lookup"><span data-stu-id="23ec5-109"><strong>adcReadyStateLoaded</strong></span></span></p></td>
<td><p><span data-ttu-id="23ec5-110">Die aktuelle Abfrage wird noch ausgeführt, und es wurden noch keine Zeilen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="23ec5-110">The current query is still executing and no rows have been fetched.</span></span> <span data-ttu-id="23ec5-111">Das <strong>Recordset</strong>-Objekt des <strong>DataControl</strong>-Objekts ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="23ec5-111">The <strong>DataControl</strong> object's <strong>Recordset</strong> is not available for use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23ec5-112"><strong>adcReadyStateInteractive</strong></span><span class="sxs-lookup"><span data-stu-id="23ec5-112"><strong>adcReadyStateInteractive</strong></span></span></p></td>
<td><p><span data-ttu-id="23ec5-p102">Eine erste von der aktuellen Abfrage abgerufene Datensatzgruppe wurde im <strong>Recordset</strong>-Objekt des <strong>DataControl</strong>-Objekts gespeichert und ist verfügbar. Die übrigen Zeilen werden noch abgerufen.</span><span class="sxs-lookup"><span data-stu-id="23ec5-p102">An initial set of rows retrieved by the current query has been stored in the <strong>DataControl</strong> object's <strong>Recordset</strong> and are available for use. The remaining rows are still being fetched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23ec5-115"><strong>adcReadyStateComplete</strong></span><span class="sxs-lookup"><span data-stu-id="23ec5-115"><strong>adcReadyStateComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="23ec5-116">Alle von der aktuellen Abfrage abgerufenen Zeilen wurden im <strong>Recordset</strong>-Objekt des <strong>DataControl</strong>-Objekts gespeichert und sind verfügbar.</span><span class="sxs-lookup"><span data-stu-id="23ec5-116">All rows retrieved by the current query have been stored in the <strong>DataControl</strong> object's <strong>Recordset</strong> and are available for use.</span></span> <span data-ttu-id="23ec5-117">Dieser Status ist auch vorhanden, wenn eine Operation aufgrund eines Fehlers abgebrochen wurde oder wenn das <strong>Recordset</strong>-Objekt nicht initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="23ec5-117">This state will also exist if an operation aborted due to an error, or if the <strong>Recordset</strong> object is not initialized.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="23ec5-p104">Each client-side executable file that uses these constants must provide declarations for them. You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span><span class="sxs-lookup"><span data-stu-id="23ec5-p104">Each client-side executable file that uses these constants must provide declarations for them. You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="23ec5-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23ec5-120">Remarks</span></span>

<span data-ttu-id="23ec5-p105">Verwenden Sie das [onReadyStateChange](onreadystatechange-event-rds.md)-Ereignis, um Änderungen in der **ReadyState**-Eigenschaft während einer asynchronen Abfrageoperation zu überwachen. Das ist effizienter, als den Wert der Eigenschaft regelmäßig zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="23ec5-p105">Use the [onReadyStateChange](onreadystatechange-event-rds.md) event to monitor changes in the **ReadyState** property during an asynchronous query operation. This is more efficient than periodically checking the value of the property.</span></span>

<span data-ttu-id="23ec5-123">Wenn während eines asynchronen Vorgangs ein Fehler auftritt, ändert sich die **ReadyState** -Eigenschaft in **AdcReadyStateComplete**, die [State](state-property-ado.md) -Eigenschaft ändert sich von **adStateExecuting** in **adStateClosed**, und das **Recordset** Object [value](value-property-ado.md) -Eigenschaft \*\* bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="23ec5-123">If an error occurs during an asynchronous operation, the **ReadyState** property changes to **adcReadyStateComplete**, the [State](state-property-ado.md) property changes from **adStateExecuting** to **adStateClosed**, and the **Recordset** object [Value](value-property-ado.md) property remains *Nothing*.</span></span>

