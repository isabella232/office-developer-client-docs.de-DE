---
title: EventStatusEnum (Access Desktop Database Reference)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 654d2a485c9273072d1daa61321e73418a15e969
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293273"
---
# <a name="eventstatusenum"></a><span data-ttu-id="74899-102">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="74899-102">EventStatusEnum</span></span>

<span data-ttu-id="74899-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="74899-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="74899-104">Gibt den aktuellen Status der Ausführung eines Ereignisses an.</span><span class="sxs-lookup"><span data-stu-id="74899-104">Specifies the current status of the execution of an event.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="74899-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="74899-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="74899-106">Wert</span><span class="sxs-lookup"><span data-stu-id="74899-106">Value</span></span></p></th>
<th><p><span data-ttu-id="74899-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74899-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74899-108"><strong>adStatusCancel fest</strong></span><span class="sxs-lookup"><span data-stu-id="74899-108"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="74899-109">4</span><span class="sxs-lookup"><span data-stu-id="74899-109">4</span></span></p></td>
<td><p><span data-ttu-id="74899-110">Fordert den Abbruch des Vorgangs an, der zum Ereignis führte.</span><span class="sxs-lookup"><span data-stu-id="74899-110">Requests cancellation of the operation that caused the event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74899-111"><strong>adStatusCantDeny festgelegt</strong></span><span class="sxs-lookup"><span data-stu-id="74899-111"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="74899-112">3</span><span class="sxs-lookup"><span data-stu-id="74899-112">3</span></span></p></td>
<td><p><span data-ttu-id="74899-113">Gibt an, dass der Vorgang keinen Abbruch der ausstehenden Operation anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="74899-113">Indicates that the operation cannot request cancellation of the pending operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74899-114"><strong>adStatusErrorsOccurred festgelegt</strong></span><span class="sxs-lookup"><span data-stu-id="74899-114"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="74899-115">2</span><span class="sxs-lookup"><span data-stu-id="74899-115">2</span></span></p></td>
<td><p><span data-ttu-id="74899-116">Gibt an, dass der Vorgang, der das Ereignis verursachte, aufgrund eines Fehlers oder mehrerer Fehler fehlschlug.</span><span class="sxs-lookup"><span data-stu-id="74899-116">Indicates that the operation that caused the event failed due to an error or errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74899-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="74899-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="74899-118">1</span><span class="sxs-lookup"><span data-stu-id="74899-118">1</span></span></p></td>
<td><p><span data-ttu-id="74899-119">Gibt an, dass der Vorgang, der das Ereignis verursachte, erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="74899-119">Indicates that the operation that caused the event was successful.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74899-120"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="74899-120"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="74899-121">5</span><span class="sxs-lookup"><span data-stu-id="74899-121">5</span></span></p></td>
<td><p><span data-ttu-id="74899-122">Verhindert nachfolgende Benachrichtigungen, bevor die Ereignismethode die Ausführung beendet hat.</span><span class="sxs-lookup"><span data-stu-id="74899-122">Prevents subsequent notifications before the event method has finished executing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="74899-123">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="74899-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="74899-124">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="74899-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="74899-125">Konstante</span><span class="sxs-lookup"><span data-stu-id="74899-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74899-126">AdoEnums. EventStatus. CANCEL</span><span class="sxs-lookup"><span data-stu-id="74899-126">AdoEnums.EventStatus.CANCEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74899-127">AdoEnums. EventStatus. CANTDENY</span><span class="sxs-lookup"><span data-stu-id="74899-127">AdoEnums.EventStatus.CANTDENY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74899-128">AdoEnums. EventStatus. ERRORSOCCURRED</span><span class="sxs-lookup"><span data-stu-id="74899-128">AdoEnums.EventStatus.ERRORSOCCURRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74899-129">AdoEnums. EventStatus. OK</span><span class="sxs-lookup"><span data-stu-id="74899-129">AdoEnums.EventStatus.OK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74899-130">AdoEnums. EventStatus. UNWANTEDEVENT</span><span class="sxs-lookup"><span data-stu-id="74899-130">AdoEnums.EventStatus.UNWANTEDEVENT</span></span></p></td>
</tr>
</tbody>
</table>

