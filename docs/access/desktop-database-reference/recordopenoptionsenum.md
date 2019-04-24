---
title: RecordOpenOptionsEnum
TOCTitle: RecordOpenOptionsEnum
ms:assetid: 44a69719-0789-a084-fb96-21468e270205
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249207(v=office.15)
ms:contentKeyID: 48544534
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: caaf755ebd63f1805d0c77ef79a0f5863a85050e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300686"
---
# <a name="recordopenoptionsenum"></a><span data-ttu-id="310ea-102">RecordOpenOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="310ea-102">RecordOpenOptionsEnum</span></span>


<span data-ttu-id="310ea-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="310ea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="310ea-104">Gibt Optionen zum Öffnen eines [Datensatzes](record-object-ado.md) an.</span><span class="sxs-lookup"><span data-stu-id="310ea-104">Specifies options for opening a [Record](record-object-ado.md).</span></span> <span data-ttu-id="310ea-105">Diese Werte können mit OR kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="310ea-105">These values may be combined by using OR.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="310ea-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="310ea-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="310ea-107">Wert</span><span class="sxs-lookup"><span data-stu-id="310ea-107">Value</span></span></p></th>
<th><p><span data-ttu-id="310ea-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="310ea-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="310ea-109"><strong>adDelayFetchFields</strong></span><span class="sxs-lookup"><span data-stu-id="310ea-109"><strong>adDelayFetchFields</strong></span></span></p></td>
<td><p><span data-ttu-id="310ea-110">0X8000</span><span class="sxs-lookup"><span data-stu-id="310ea-110">0x8000</span></span></p></td>
<td><p><span data-ttu-id="310ea-111">Gibt an, dass der Anbieter die mit dem <strong>Datensatz</strong> verknüpften Felder nicht anfänglich abgerufen werden muss, aber beim ersten Zugriff auf das Feld abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="310ea-111">Indicates to the provider that the fields associated with the <strong>Record</strong> need not be retrieved initially, but can be retrieved at the first attempt to access the field.</span></span> <span data-ttu-id="310ea-112">Das Standardverhalten, das durch das Fehlen dieses Flags angegeben wird, besteht darin, alle <strong>Record</strong> -Objektfelder abzurufen.</span><span class="sxs-lookup"><span data-stu-id="310ea-112">The default behavior, indicated by the absence of this flag, is to retrieve all the <strong>Record</strong> object fields.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="310ea-113"><strong>adDelayFetchStream</strong></span><span class="sxs-lookup"><span data-stu-id="310ea-113"><strong>adDelayFetchStream</strong></span></span></p></td>
<td><p><span data-ttu-id="310ea-114">0x4000</span><span class="sxs-lookup"><span data-stu-id="310ea-114">0x4000</span></span></p></td>
<td><p><span data-ttu-id="310ea-115">Gibt dem Anbieter an, dass der dem <strong>Datensatz</strong> zugeordnete Standarddatenstrom nicht anfänglich abgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="310ea-115">Indicates to the provider that the default stream associated with the <strong>Record</strong> need not be retrieved initially.</span></span> <span data-ttu-id="310ea-116">Das Standardverhalten, das durch das Fehlen dieses Flags angegeben wird, besteht darin, den Standarddatenstrom abzurufen, der dem <strong>Record</strong> -Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="310ea-116">The default behavior, indicated by the absence of this flag, is to retrieve the default stream associated with the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="310ea-117"><strong>adOpenAsync</strong></span><span class="sxs-lookup"><span data-stu-id="310ea-117"><strong>adOpenAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="310ea-118">0x1000</span><span class="sxs-lookup"><span data-stu-id="310ea-118">0x1000</span></span></p></td>
<td><p><span data-ttu-id="310ea-119">Gibt an, dass das <strong>Record</strong>-Objekt im asynchronen Modus geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="310ea-119">Indicates that the <strong>Record</strong> object is opened in asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="310ea-120"><strong>adOpenExecuteCommand</strong></span><span class="sxs-lookup"><span data-stu-id="310ea-120"><strong>adOpenExecuteCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="310ea-121">0x10000</span><span class="sxs-lookup"><span data-stu-id="310ea-121">0x10000</span></span></p></td>
<td><p><span data-ttu-id="310ea-p104">Gibt an, dass die Quellzeichenfolge Befehlstext enthält, der ausgeführt werden sollte. Dieser Wert entspricht der <strong>adCmdText</strong>-Option von <strong>Recordset.Open</strong>.</span><span class="sxs-lookup"><span data-stu-id="310ea-p104">Indicates that the Source string contains command text that should be executed. This value is equivalent to the <strong>adCmdText</strong> option on <strong>Recordset.Open</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="310ea-124"><strong>adOpenRecordUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="310ea-124"><strong>adOpenRecordUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="310ea-125">-1</span><span class="sxs-lookup"><span data-stu-id="310ea-125">-1</span></span></p></td>
<td><p><span data-ttu-id="310ea-p105">Standardwert. Gibt an, dass keine Optionen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="310ea-p105">Default. Indicates no options are specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="310ea-128"><strong>adOpenOutput</strong></span><span class="sxs-lookup"><span data-stu-id="310ea-128"><strong>adOpenOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="310ea-129">0x800000</span><span class="sxs-lookup"><span data-stu-id="310ea-129">0x800000</span></span></p></td>
<td><p><span data-ttu-id="310ea-p106">Wenn die Quelle auf einen Knoten verweist, der ein ausführbares Skript (z. B. eine ASP-Seite) enthält, dann enthält der geöffnete Datensatz die Ergebnisse des ausgeführten Skripts. Dieser Wert ist nur gültig mit Datensätzen, die nicht der Auflistung angehören.</span><span class="sxs-lookup"><span data-stu-id="310ea-p106">Indicates that if the source points to a node that contains an executable script (such as an .ASP page), then the opened <strong>Record</strong> will contain the results of the executed script. This value is only valid with non-collection records.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="310ea-132">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="310ea-132">ADO/WFC equivalent</span></span>

<span data-ttu-id="310ea-133">Diese Konstanten haben keine ADO/WFC-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="310ea-133">These constants do not have ADO/WFC equivalents.</span></span>

