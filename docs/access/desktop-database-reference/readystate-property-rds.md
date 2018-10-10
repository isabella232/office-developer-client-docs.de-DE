---
title: ReadyState-Eigenschaft (RDS)
TOCTitle: ReadyState Property (RDS)
ms:assetid: e7b62205-a604-ef43-2f5d-9b51b46d2b5a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250175(v=office.15)
ms:contentKeyID: 48548412
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 804a98a6fa7c93617a5b6e165a2a012969c66913
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474738"
---
# <a name="readystate-property-rds"></a><span data-ttu-id="98ed2-102">ReadyState-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="98ed2-102">ReadyState Property (RDS)</span></span>


<span data-ttu-id="98ed2-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="98ed2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="98ed2-104">Gibt den Status eines [DataControl](datacontrol-object-rds.md)-Objekts beim Abrufen von Daten in dessen [Recordset](recordset-object-ado.md)-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="98ed2-104">Indicates the progress of a [DataControl](datacontrol-object-rds.md) object as it retrieves data into its [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="98ed2-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="98ed2-105">Settings and Return Values</span></span>

<span data-ttu-id="98ed2-106">Legt einen der folgenden Werte fest oder gibt ihn zurück.</span><span class="sxs-lookup"><span data-stu-id="98ed2-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="98ed2-107">Wert</span><span class="sxs-lookup"><span data-stu-id="98ed2-107">Value</span></span></p></th>
<th><p><span data-ttu-id="98ed2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="98ed2-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98ed2-109"><strong>adcReadyStateLoaded</strong></span><span class="sxs-lookup"><span data-stu-id="98ed2-109"><strong>adcReadyStateLoaded</strong></span></span></p></td>
<td><p><span data-ttu-id="98ed2-p101">Die aktuelle Abfrage wird noch ausgeführt, und es wurden noch keine Zeilen abgerufen. Das <strong>Recordset</strong>-Objekt des <strong>DataControl</strong>-Objekts ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="98ed2-p101">The current query is still executing and no rows have been fetched. The <strong>DataControl</strong> object's <strong>Recordset</strong> is not available for use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98ed2-112"><strong>adcReadyStateInteractive</strong></span><span class="sxs-lookup"><span data-stu-id="98ed2-112"><strong>adcReadyStateInteractive</strong></span></span></p></td>
<td><p><span data-ttu-id="98ed2-p102">Eine erste von der aktuellen Abfrage abgerufene Datensatzgruppe wurde im <strong>Recordset</strong>-Objekt des <strong>DataControl</strong>-Objekts gespeichert und ist verfügbar. Die übrigen Zeilen werden noch abgerufen.</span><span class="sxs-lookup"><span data-stu-id="98ed2-p102">An initial set of rows retrieved by the current query has been stored in the <strong>DataControl</strong> object's <strong>Recordset</strong> and are available for use. The remaining rows are still being fetched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98ed2-115"><strong>adcReadyStateComplete</strong></span><span class="sxs-lookup"><span data-stu-id="98ed2-115"><strong>adcReadyStateComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="98ed2-116">Alle von der aktuellen Abfrage abgerufenen Zeilen wurden im <strong>Recordset</strong>-Objekt des <strong>DataControl</strong>-Objekts gespeichert und sind verfügbar.
</span><span class="sxs-lookup"><span data-stu-id="98ed2-116">All rows retrieved by the current query have been stored in the <strong>DataControl</strong> object's <strong>Recordset</strong> and are available for use.</span></span> <span data-ttu-id="98ed2-117">Dieser Status ist auch vorhanden, wenn eine Operation aufgrund eines Fehlers abgebrochen wurde oder wenn das <strong>Recordset</strong>-Objekt nicht initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="98ed2-117">This state will also exist if an operation aborted due to an error, or if the <strong>Recordset</strong> object is not initialized.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="98ed2-118">Jede mithilfe der clientseitigen ausführbare Datei, die die folgenden Konstanten verwendet, muss Deklarationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="98ed2-118">Each client-side executable file that uses these constants must provide declarations for them.</span></span> <span data-ttu-id="98ed2-119">Sie können Ausschneiden und Einfügen aus der Datei Datei Adcvbs.inc, befindet sich im Ordner C:\Program Files\Common Dateien\System\MSADC gewünschten Konstantendeklarationen.</span><span class="sxs-lookup"><span data-stu-id="98ed2-119">You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="98ed2-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="98ed2-120">Remarks</span></span>

<span data-ttu-id="98ed2-p105">Verwenden Sie das [onReadyStateChange](onreadystatechange-event-rds.md)-Ereignis, um Änderungen in der **ReadyState** -Eigenschaft während einer asynchronen Abfrageoperation zu überwachen. Das ist effizienter, als den Wert der Eigenschaft regelmäßig zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="98ed2-p105">Use the [onReadyStateChange](onreadystatechange-event-rds.md) event to monitor changes in the **ReadyState** property during an asynchronous query operation. This is more efficient than periodically checking the value of the property.</span></span>

<span data-ttu-id="98ed2-123">Wenn ein Fehler, während einer asynchronen Operation die **ReadyState** -eigenschaftsänderungen zu **AdcReadyStateComplete auftritt**, ändert sich die [State](state-property-ado.md) -Eigenschaft von **AdStateExecuting** in **AdStateClosed**, und das **Recordset-Objekt** Objekt [Value](value-property-ado.md) -Eigenschaft bleibt *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="98ed2-123">If an error occurs during an asynchronous operation, the **ReadyState** property changes to **adcReadyStateComplete**, the [State](state-property-ado.md) property changes from **adStateExecuting** to **adStateClosed**, and the **Recordset** object [Value](value-property-ado.md) property remains *Nothing*.</span></span>

