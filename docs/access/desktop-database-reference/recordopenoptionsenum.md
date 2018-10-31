---
title: RecordOpenOptionsEnum
TOCTitle: RecordOpenOptionsEnum
ms:assetid: 44a69719-0789-a084-fb96-21468e270205
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249207(v=office.15)
ms:contentKeyID: 48544534
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 54499cc9c8b45e411b4121963d1a571100b7e0e5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860946"
---
# <a name="recordopenoptionsenum"></a><span data-ttu-id="488ca-102">RecordOpenOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="488ca-102">RecordOpenOptionsEnum</span></span>


<span data-ttu-id="488ca-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="488ca-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="488ca-p101">Gibt Optionen zum Öffnen eines [Datensatzes](record-object-ado.md) an. Diese Werte können mit OR kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="488ca-p101">Specifies options for opening a [Record](record-object-ado.md). These values may be combined by using OR.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="488ca-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="488ca-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="488ca-107">Wert</span><span class="sxs-lookup"><span data-stu-id="488ca-107">Value</span></span></p></th>
<th><p><span data-ttu-id="488ca-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="488ca-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="488ca-109"><strong>adDelayFetchFields</strong></span><span class="sxs-lookup"><span data-stu-id="488ca-109"><strong>adDelayFetchFields</strong></span></span></p></td>
<td><p><span data-ttu-id="488ca-110">0 x 8000</span><span class="sxs-lookup"><span data-stu-id="488ca-110">0x8000</span></span></p></td>
<td><p><span data-ttu-id="488ca-111">Der Anbieter zeigt, dass die Felder, die dem <strong>Eintrag</strong> zugeordnete zunächst nicht abgerufen werden müssen, aber beim ersten Versuch Zugriff auf das Feld abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="488ca-111">Indicates to the provider that the fields associated with the <strong>Record</strong> need not be retrieved initially, but can be retrieved at the first attempt to access the field.</span></span> <span data-ttu-id="488ca-112">Das Standardverhalten, durch die Abwesenheit dieses Flags ist die <strong>Datensatz</strong> -Objektfelder abgerufen.</span><span class="sxs-lookup"><span data-stu-id="488ca-112">The default behavior, indicated by the absence of this flag, is to retrieve all the <strong>Record</strong> object fields.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="488ca-113"><strong>adDelayFetchStream</strong></span><span class="sxs-lookup"><span data-stu-id="488ca-113"><strong>adDelayFetchStream</strong></span></span></p></td>
<td><p><span data-ttu-id="488ca-114">0x4000</span><span class="sxs-lookup"><span data-stu-id="488ca-114">0x4000</span></span></p></td>
<td><p><span data-ttu-id="488ca-115">Der Anbieter zeigt, dass der dem <strong>Eintrag</strong> zugeordnete Standarddatenstrom zunächst nicht abgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="488ca-115">Indicates to the provider that the default stream associated with the <strong>Record</strong> need not be retrieved initially.</span></span> <span data-ttu-id="488ca-116">Das Standardverhalten, durch die Abwesenheit dieses Flags ist abzurufenden den Standarddatenstrom das <strong>Record</strong> -Objekt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="488ca-116">The default behavior, indicated by the absence of this flag, is to retrieve the default stream associated with the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="488ca-117"><strong>adOpenAsync</strong></span><span class="sxs-lookup"><span data-stu-id="488ca-117"><strong>adOpenAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="488ca-118">0x1000</span><span class="sxs-lookup"><span data-stu-id="488ca-118">0x1000</span></span></p></td>
<td><p><span data-ttu-id="488ca-119">Gibt an, dass das <strong>Record</strong>-Objekt im asynchronen Modus geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="488ca-119">Indicates that the <strong>Record</strong> object is opened in asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="488ca-120"><strong>adOpenExecuteCommand</strong></span><span class="sxs-lookup"><span data-stu-id="488ca-120"><strong>adOpenExecuteCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="488ca-121">0 x 10000</span><span class="sxs-lookup"><span data-stu-id="488ca-121">0x10000</span></span></p></td>
<td><p><span data-ttu-id="488ca-p104">Gibt an, dass die Quellzeichenfolge Befehlstext enthält, der ausgeführt werden sollte. Dieser Wert entspricht der <strong>adCmdText</strong>-Option von <strong>Recordset.Open</strong>.</span><span class="sxs-lookup"><span data-stu-id="488ca-p104">Indicates that the Source string contains command text that should be executed. This value is equivalent to the <strong>adCmdText</strong> option on <strong>Recordset.Open</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="488ca-124"><strong>adOpenRecordUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="488ca-124"><strong>adOpenRecordUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="488ca-125">-1</span><span class="sxs-lookup"><span data-stu-id="488ca-125">-1</span></span></p></td>
<td><p><span data-ttu-id="488ca-p105">Standardwert. Gibt an, dass keine Optionen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="488ca-p105">Default. Indicates no options are specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="488ca-128"><strong>adOpenOutput</strong></span><span class="sxs-lookup"><span data-stu-id="488ca-128"><strong>adOpenOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="488ca-129">0 x 800000</span><span class="sxs-lookup"><span data-stu-id="488ca-129">0x800000</span></span></p></td>
<td><p><span data-ttu-id="488ca-130">Gibt an, dass, wenn die Datenquelle an einen Knoten verweist, der ein ausführbares Skript enthält (z. B. ein. ASP-Seite), und klicken Sie dann die geöffnete <strong>Datensatz</strong> die Ergebnisse des ausgeführten Skripts enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="488ca-130">Indicates that if the source points to a node that contains an executable script (such as an .ASP page), then the opened <strong>Record</strong> will contain the results of the executed script.</span></span> <span data-ttu-id="488ca-131">Dieser Wert ist nur gültig, wenn nicht der Auflistung Datensätze.</span><span class="sxs-lookup"><span data-stu-id="488ca-131">This value is only valid with non-collection records.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="488ca-132">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="488ca-132">ADO/WFC equivalent</span></span>

<span data-ttu-id="488ca-133">Diese Konstanten haben keine ADO/WFC-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="488ca-133">These constants do not have ADO/WFC equivalents.</span></span>

