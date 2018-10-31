---
title: CursorLocationEnum (Access PC-Datenbank-Referenz)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 7f8eedd1245be16d87a2d3b2cd2b9121853529c5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863631"
---
# <a name="cursorlocationenum"></a><span data-ttu-id="15d49-102">CursorLocationEnum</span><span class="sxs-lookup"><span data-stu-id="15d49-102">CursorLocationEnum</span></span>

<span data-ttu-id="15d49-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="15d49-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="15d49-104">Gibt den Speicherort des Cursordiensts an.</span><span class="sxs-lookup"><span data-stu-id="15d49-104">Specifies the location of the cursor service.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="15d49-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="15d49-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="15d49-106">Wert</span><span class="sxs-lookup"><span data-stu-id="15d49-106">Value</span></span></p></th>
<th><p><span data-ttu-id="15d49-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15d49-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15d49-108"><strong>adUseClient</strong></span><span class="sxs-lookup"><span data-stu-id="15d49-108"><strong>adUseClient</strong></span></span></p></td>
<td><p><span data-ttu-id="15d49-109">3</span><span class="sxs-lookup"><span data-stu-id="15d49-109">3</span></span></p></td>
<td><p><span data-ttu-id="15d49-110">Clientseitige Cursor von einer lokalen Cursorbibliothek bereitgestellt wird, verwendet.</span><span class="sxs-lookup"><span data-stu-id="15d49-110">Uses client-side cursors supplied by a local cursor library.</span></span> <span data-ttu-id="15d49-111">Lokale Cursor Services ermöglichen häufig viele Funktionen, die Treiber bereitgestellten Cursor möglicherweise nicht so mit dieser Einstellung Vorteil in Bezug auf Funktionen bereitstellen kann, die aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="15d49-111">Local cursor services often will allow many features that driver-supplied cursors may not, so using this setting may provide an advantage with respect to features that will be enabled.</span></span> <span data-ttu-id="15d49-112">Für die Abwärtskompatibilität wird das Synonym <strong>AdUseClientBatch</strong> ebenfalls unterstützt.</span><span class="sxs-lookup"><span data-stu-id="15d49-112">For backward compatibility, the synonym <strong>adUseClientBatch</strong> is also supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15d49-113"><strong>adUseNone</strong></span><span class="sxs-lookup"><span data-stu-id="15d49-113"><strong>adUseNone</strong></span></span></p></td>
<td><p><span data-ttu-id="15d49-114">1</span><span class="sxs-lookup"><span data-stu-id="15d49-114">1</span></span></p></td>
<td><p><span data-ttu-id="15d49-p102">Verwendet keine Cursordienste. (Diese Konstante ist veraltet und wird ausschließlich zur Abwärtskompatibilität angezeigt.)</span><span class="sxs-lookup"><span data-stu-id="15d49-p102">Does not use cursor services. (This constant is obsolete and appears solely for the sake of backward compatibility.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15d49-117"><strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="15d49-117"><strong>adUseServer</strong></span></span></p></td>
<td><p><span data-ttu-id="15d49-118">2</span><span class="sxs-lookup"><span data-stu-id="15d49-118">2</span></span></p></td>
<td><p><span data-ttu-id="15d49-119">Standard.</span><span class="sxs-lookup"><span data-stu-id="15d49-119">Default.</span></span> <span data-ttu-id="15d49-120">Verwendet vom Datenanbieter oder Treiber bereitgestellte Cursor.</span><span class="sxs-lookup"><span data-stu-id="15d49-120">Uses data-provider or driver-supplied cursors.</span></span> <span data-ttu-id="15d49-121">Diese Cursor sind in einigen Fällen sehr flexibel und zusätzliche Empfindlichkeit gegenüber Änderungen, die andere Personen an der Datenquelle ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="15d49-121">These cursors are sometimes very flexible and allow for additional sensitivity to changes others make to the data source.</span></span> <span data-ttu-id="15d49-122">Jedoch einige Features des <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service für OLE DB</a> (beispielsweise nicht verbundenes <a href="recordset-object-ado.md">Recordset</a> -Objekte) können nicht mit serverseitigen Cursorn simuliert werden, und diese Funktionen werden mit dieser Einstellung nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="15d49-122">However, some features of the <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> (such as disassociated <a href="recordset-object-ado.md">Recordset</a> objects) cannot be simulated with server-side cursors, and these features will be unavailable with this setting.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="15d49-123">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="15d49-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="15d49-124">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="15d49-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="15d49-125">Konstante</span><span class="sxs-lookup"><span data-stu-id="15d49-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15d49-126">AdoEnums.CursorLocation.CLIENT</span><span class="sxs-lookup"><span data-stu-id="15d49-126">AdoEnums.CursorLocation.CLIENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15d49-127">AdoEnums.CursorLocation.NONE</span><span class="sxs-lookup"><span data-stu-id="15d49-127">AdoEnums.CursorLocation.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15d49-128">AdoEnums.CursorLocation.SERVER</span><span class="sxs-lookup"><span data-stu-id="15d49-128">AdoEnums.CursorLocation.SERVER</span></span></p></td>
</tr>
</tbody>
</table>

