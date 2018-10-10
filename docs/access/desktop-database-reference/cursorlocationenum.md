---
title: CursorLocationEnum (Access PC-Datenbank-Referenz)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 90226413579a8fac7586cbd5ef08510a36a42959
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474012"
---
# <a name="cursorlocationenum"></a><span data-ttu-id="11fd0-102">CursorLocationEnum</span><span class="sxs-lookup"><span data-stu-id="11fd0-102">CursorLocationEnum</span></span>


<span data-ttu-id="11fd0-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="11fd0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="11fd0-104">Gibt den Speicherort des Cursordiensts an.</span><span class="sxs-lookup"><span data-stu-id="11fd0-104">Specifies the location of the cursor service.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="11fd0-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="11fd0-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="11fd0-106">Wert</span><span class="sxs-lookup"><span data-stu-id="11fd0-106">Value</span></span></p></th>
<th><p><span data-ttu-id="11fd0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11fd0-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="11fd0-108"><strong>adUseClient</strong></span><span class="sxs-lookup"><span data-stu-id="11fd0-108"><strong>adUseClient</strong></span></span></p></td>
<td><p><span data-ttu-id="11fd0-109">3</span><span class="sxs-lookup"><span data-stu-id="11fd0-109">3</span></span></p></td>
<td><p><span data-ttu-id="11fd0-110">Clientseitige Cursor von einer lokalen Cursorbibliothek bereitgestellt wird, verwendet.</span><span class="sxs-lookup"><span data-stu-id="11fd0-110">Uses client-side cursors supplied by a local cursor library.</span></span> <span data-ttu-id="11fd0-111">Lokale Cursor Services ermöglichen häufig viele Funktionen, die Treiber bereitgestellten Cursor möglicherweise nicht so mit dieser Einstellung Vorteil in Bezug auf Funktionen bereitstellen kann, die aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="11fd0-111">Local cursor services often will allow many features that driver-supplied cursors may not, so using this setting may provide an advantage with respect to features that will be enabled.</span></span> <span data-ttu-id="11fd0-112">Für die Abwärtskompatibilität wird das Synonym <strong>AdUseClientBatch</strong> ebenfalls unterstützt.</span><span class="sxs-lookup"><span data-stu-id="11fd0-112">For backward compatibility, the synonym <strong>adUseClientBatch</strong> is also supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fd0-113"><strong>adUseNone</strong></span><span class="sxs-lookup"><span data-stu-id="11fd0-113"><strong>adUseNone</strong></span></span></p></td>
<td><p><span data-ttu-id="11fd0-114">1</span><span class="sxs-lookup"><span data-stu-id="11fd0-114">1</span></span></p></td>
<td><p><span data-ttu-id="11fd0-p102">Verwendet keine Cursordienste. (Diese Konstante ist veraltet und wird ausschließlich zur Abwärtskompatibilität angezeigt.)</span><span class="sxs-lookup"><span data-stu-id="11fd0-p102">Does not use cursor services. (This constant is obsolete and appears solely for the sake of backward compatibility.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fd0-117"><strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="11fd0-117"><strong>adUseServer</strong></span></span></p></td>
<td><p><span data-ttu-id="11fd0-118">2</span><span class="sxs-lookup"><span data-stu-id="11fd0-118">2</span></span></p></td>
<td><p><span data-ttu-id="11fd0-p103">Standardwert. Verwendet Datenanbieter- oder treiberbasierte Cursor. Diese Cursor sind manchmal sehr flexibel und ermöglichen eine zusätzliche Unterscheidung von Änderungen, die andere Personen an der Datenquelle vornehmen. Andere Features des <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service für OLE DB</a> (wie z. B. entkoppelte <a href="recordset-object-ado.md">Recordset</a>-Objekte) können nicht mit serverseitigen Cursorn simuliert werden. Diese Features stehen mit dieser Einstellung nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="11fd0-p103">Default. Uses data-provider or driver-supplied cursors. These cursors are sometimes very flexible and allow for additional sensitivity to changes others make to the data source. However, some features of the <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> (such as disassociated <a href="recordset-object-ado.md">Recordset</a> objects) cannot be simulated with server-side cursors and these features will be unavailable with this setting.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="11fd0-123">**ADO/WFC-Entsprechung**</span><span class="sxs-lookup"><span data-stu-id="11fd0-123">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="11fd0-124">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="11fd0-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="11fd0-125">Konstante</span><span class="sxs-lookup"><span data-stu-id="11fd0-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="11fd0-126">AdoEnums.CursorLocation.CLIENT</span><span class="sxs-lookup"><span data-stu-id="11fd0-126">AdoEnums.CursorLocation.CLIENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fd0-127">AdoEnums.CursorLocation.NONE</span><span class="sxs-lookup"><span data-stu-id="11fd0-127">AdoEnums.CursorLocation.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fd0-128">AdoEnums.CursorLocation.SERVER</span><span class="sxs-lookup"><span data-stu-id="11fd0-128">AdoEnums.CursorLocation.SERVER</span></span></p></td>
</tr>
</tbody>
</table>

