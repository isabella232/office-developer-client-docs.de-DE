---
title: CursorLocationEnum (Access Desktop Database Reference)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95e5744d5e19e7c3d40de19e240bbe338b2d5d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295212"
---
# <a name="cursorlocationenum"></a><span data-ttu-id="f05bc-102">CursorLocationEnum</span><span class="sxs-lookup"><span data-stu-id="f05bc-102">CursorLocationEnum</span></span>

<span data-ttu-id="f05bc-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f05bc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f05bc-104">Gibt den Speicherort des Cursordiensts an.</span><span class="sxs-lookup"><span data-stu-id="f05bc-104">Specifies the location of the cursor service.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f05bc-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="f05bc-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="f05bc-106">Wert</span><span class="sxs-lookup"><span data-stu-id="f05bc-106">Value</span></span></p></th>
<th><p><span data-ttu-id="f05bc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f05bc-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f05bc-108"><strong>adUseClient</strong></span><span class="sxs-lookup"><span data-stu-id="f05bc-108"><strong>adUseClient</strong></span></span></p></td>
<td><p><span data-ttu-id="f05bc-109">3</span><span class="sxs-lookup"><span data-stu-id="f05bc-109">3</span></span></p></td>
<td><p><span data-ttu-id="f05bc-110">Verwendet clientseitige Cursor, die von einer lokalen Cursorbibliothek bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f05bc-110">Uses client-side cursors supplied by a local cursor library.</span></span> <span data-ttu-id="f05bc-111">Lokale Cursor Dienste ermöglichen häufig viele Features, die von vom Treiber bereitgestellten Cursorn möglicherweise nicht verwendet werden, sodass die Verwendung dieser Einstellung für Features, die aktiviert werden, einen Vorteil bieten kann.</span><span class="sxs-lookup"><span data-stu-id="f05bc-111">Local cursor services often will allow many features that driver-supplied cursors may not, so using this setting may provide an advantage with respect to features that will be enabled.</span></span> <span data-ttu-id="f05bc-112">Aus Gründen der Abwärtskompatibilität wird auch das Synonym <strong>adUseClientBatch</strong> unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f05bc-112">For backward compatibility, the synonym <strong>adUseClientBatch</strong> is also supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f05bc-113"><strong>adUseNone</strong></span><span class="sxs-lookup"><span data-stu-id="f05bc-113"><strong>adUseNone</strong></span></span></p></td>
<td><p><span data-ttu-id="f05bc-114">1</span><span class="sxs-lookup"><span data-stu-id="f05bc-114">1</span></span></p></td>
<td><p><span data-ttu-id="f05bc-p102">Verwendet keine Cursordienste. (Diese Konstante ist veraltet und wird ausschließlich zur Abwärtskompatibilität angezeigt.)</span><span class="sxs-lookup"><span data-stu-id="f05bc-p102">Does not use cursor services. (This constant is obsolete and appears solely for the sake of backward compatibility.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f05bc-117"><strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="f05bc-117"><strong>adUseServer</strong></span></span></p></td>
<td><p><span data-ttu-id="f05bc-118">2</span><span class="sxs-lookup"><span data-stu-id="f05bc-118">2</span></span></p></td>
<td><p><span data-ttu-id="f05bc-119">Standardwert.</span><span class="sxs-lookup"><span data-stu-id="f05bc-119">Default.</span></span> <span data-ttu-id="f05bc-120">Verwendet Datenanbieter oder vom Treiber bereitgestellte Cursor.</span><span class="sxs-lookup"><span data-stu-id="f05bc-120">Uses data-provider or driver-supplied cursors.</span></span> <span data-ttu-id="f05bc-121">Diese Cursor sind manchmal sehr flexibel und ermöglichen eine zusätzliche Vertraulichkeit für andere Änderungen an der Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="f05bc-121">These cursors are sometimes very flexible and allow for additional sensitivity to changes others make to the data source.</span></span> <span data-ttu-id="f05bc-122">Einige Features des <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor-Diensts für OLE DB</a> (beispielsweise nicht zugeordnete <a href="recordset-object-ado.md">Recordset</a> -Objekte) können jedoch nicht mit serverseitigen Cursorn simuliert werden, und diese Funktionen sind bei dieser Einstellung nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f05bc-122">However, some features of the <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> (such as disassociated <a href="recordset-object-ado.md">Recordset</a> objects) cannot be simulated with server-side cursors, and these features will be unavailable with this setting.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="f05bc-123">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="f05bc-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="f05bc-124">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="f05bc-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f05bc-125">Konstante</span><span class="sxs-lookup"><span data-stu-id="f05bc-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f05bc-126">AdoEnums. CursorLocation. CLIENT</span><span class="sxs-lookup"><span data-stu-id="f05bc-126">AdoEnums.CursorLocation.CLIENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f05bc-127">AdoEnums. CursorLocation. NONE</span><span class="sxs-lookup"><span data-stu-id="f05bc-127">AdoEnums.CursorLocation.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f05bc-128">AdoEnums. CursorLocation. SERVER</span><span class="sxs-lookup"><span data-stu-id="f05bc-128">AdoEnums.CursorLocation.SERVER</span></span></p></td>
</tr>
</tbody>
</table>

