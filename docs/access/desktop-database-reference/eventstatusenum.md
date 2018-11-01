---
title: EventStatusEnum (Access PC-Datenbank-Referenz)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 027ecde525d603b15bb7844e99edc2534774bb37
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867615"
---
# <a name="eventstatusenum"></a><span data-ttu-id="f14df-102">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="f14df-102">EventStatusEnum</span></span>

<span data-ttu-id="f14df-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f14df-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f14df-104">Gibt den aktuellen Status der Ausführung eines Ereignisses an.</span><span class="sxs-lookup"><span data-stu-id="f14df-104">Specifies the current status of the execution of an event.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f14df-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="f14df-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="f14df-106">Wert</span><span class="sxs-lookup"><span data-stu-id="f14df-106">Value</span></span></p></th>
<th><p><span data-ttu-id="f14df-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f14df-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f14df-108"><strong>adStatusCancel fest</strong></span><span class="sxs-lookup"><span data-stu-id="f14df-108"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="f14df-109">4</span><span class="sxs-lookup"><span data-stu-id="f14df-109">4</span></span></p></td>
<td><p><span data-ttu-id="f14df-110">Fordert den Abbruch des Vorgangs an, der zum Ereignis führte.</span><span class="sxs-lookup"><span data-stu-id="f14df-110">Requests cancellation of the operation that caused the event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f14df-111"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="f14df-111"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="f14df-112">3</span><span class="sxs-lookup"><span data-stu-id="f14df-112">3</span></span></p></td>
<td><p><span data-ttu-id="f14df-113">Gibt an, dass der Vorgang keinen Abbruch der ausstehenden Operation anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="f14df-113">Indicates that the operation cannot request cancellation of the pending operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f14df-114"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="f14df-114"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="f14df-115">2</span><span class="sxs-lookup"><span data-stu-id="f14df-115">2</span></span></p></td>
<td><p><span data-ttu-id="f14df-116">Gibt an, dass der Vorgang, der das Ereignis verursachte, aufgrund eines Fehlers oder mehrerer Fehler fehlschlug.</span><span class="sxs-lookup"><span data-stu-id="f14df-116">Indicates that the operation that caused the event failed due to an error or errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f14df-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="f14df-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="f14df-118">1</span><span class="sxs-lookup"><span data-stu-id="f14df-118">1</span></span></p></td>
<td><p><span data-ttu-id="f14df-119">Gibt an, dass der Vorgang, der das Ereignis verursachte, erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="f14df-119">Indicates that the operation that caused the event was successful.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f14df-120"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="f14df-120"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="f14df-121">5</span><span class="sxs-lookup"><span data-stu-id="f14df-121">5</span></span></p></td>
<td><p><span data-ttu-id="f14df-122">Verhindert nachfolgende Benachrichtigungen, bevor die Ereignismethode die Ausführung beendet hat.</span><span class="sxs-lookup"><span data-stu-id="f14df-122">Prevents subsequent notifications before the event method has finished executing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="f14df-123">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f14df-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="f14df-124">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="f14df-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f14df-125">Konstante</span><span class="sxs-lookup"><span data-stu-id="f14df-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f14df-126">AdoEnums.EventStatus.CANCEL</span><span class="sxs-lookup"><span data-stu-id="f14df-126">AdoEnums.EventStatus.CANCEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f14df-127">AdoEnums.EventStatus.CANTDENY</span><span class="sxs-lookup"><span data-stu-id="f14df-127">AdoEnums.EventStatus.CANTDENY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f14df-128">AdoEnums.EventStatus.ERRORSOCCURRED</span><span class="sxs-lookup"><span data-stu-id="f14df-128">AdoEnums.EventStatus.ERRORSOCCURRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f14df-129">AdoEnums.EventStatus.OK</span><span class="sxs-lookup"><span data-stu-id="f14df-129">AdoEnums.EventStatus.OK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f14df-130">AdoEnums.EventStatus.UNWANTEDEVENT</span><span class="sxs-lookup"><span data-stu-id="f14df-130">AdoEnums.EventStatus.UNWANTEDEVENT</span></span></p></td>
</tr>
</tbody>
</table>

