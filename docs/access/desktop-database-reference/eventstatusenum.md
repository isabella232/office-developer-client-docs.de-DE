---
title: EventStatusEnum (Access PC-Datenbank-Referenz)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 654d2a485c9273072d1daa61321e73418a15e969
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712582"
---
# <a name="eventstatusenum"></a><span data-ttu-id="f37dd-102">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="f37dd-102">EventStatusEnum</span></span>

<span data-ttu-id="f37dd-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f37dd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f37dd-104">Gibt den aktuellen Status der Ausführung eines Ereignisses an.</span><span class="sxs-lookup"><span data-stu-id="f37dd-104">Specifies the current status of the execution of an event.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f37dd-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="f37dd-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="f37dd-106">Wert</span><span class="sxs-lookup"><span data-stu-id="f37dd-106">Value</span></span></p></th>
<th><p><span data-ttu-id="f37dd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f37dd-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f37dd-108"><strong>adStatusCancel fest</strong></span><span class="sxs-lookup"><span data-stu-id="f37dd-108"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="f37dd-109">4</span><span class="sxs-lookup"><span data-stu-id="f37dd-109">4</span></span></p></td>
<td><p><span data-ttu-id="f37dd-110">Fordert den Abbruch des Vorgangs an, der zum Ereignis führte.</span><span class="sxs-lookup"><span data-stu-id="f37dd-110">Requests cancellation of the operation that caused the event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f37dd-111"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="f37dd-111"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="f37dd-112">3</span><span class="sxs-lookup"><span data-stu-id="f37dd-112">3</span></span></p></td>
<td><p><span data-ttu-id="f37dd-113">Gibt an, dass der Vorgang keinen Abbruch der ausstehenden Operation anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="f37dd-113">Indicates that the operation cannot request cancellation of the pending operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f37dd-114"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="f37dd-114"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="f37dd-115">2</span><span class="sxs-lookup"><span data-stu-id="f37dd-115">2</span></span></p></td>
<td><p><span data-ttu-id="f37dd-116">Gibt an, dass der Vorgang, der das Ereignis verursachte, aufgrund eines Fehlers oder mehrerer Fehler fehlschlug.</span><span class="sxs-lookup"><span data-stu-id="f37dd-116">Indicates that the operation that caused the event failed due to an error or errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f37dd-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="f37dd-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="f37dd-118">1</span><span class="sxs-lookup"><span data-stu-id="f37dd-118">1</span></span></p></td>
<td><p><span data-ttu-id="f37dd-119">Gibt an, dass der Vorgang, der das Ereignis verursachte, erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="f37dd-119">Indicates that the operation that caused the event was successful.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f37dd-120"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="f37dd-120"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="f37dd-121">5</span><span class="sxs-lookup"><span data-stu-id="f37dd-121">5</span></span></p></td>
<td><p><span data-ttu-id="f37dd-122">Verhindert nachfolgende Benachrichtigungen, bevor die Ereignismethode die Ausführung beendet hat.</span><span class="sxs-lookup"><span data-stu-id="f37dd-122">Prevents subsequent notifications before the event method has finished executing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="f37dd-123">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f37dd-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="f37dd-124">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="f37dd-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f37dd-125">Konstante</span><span class="sxs-lookup"><span data-stu-id="f37dd-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f37dd-126">AdoEnums.EventStatus.CANCEL</span><span class="sxs-lookup"><span data-stu-id="f37dd-126">AdoEnums.EventStatus.CANCEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f37dd-127">AdoEnums.EventStatus.CANTDENY</span><span class="sxs-lookup"><span data-stu-id="f37dd-127">AdoEnums.EventStatus.CANTDENY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f37dd-128">AdoEnums.EventStatus.ERRORSOCCURRED</span><span class="sxs-lookup"><span data-stu-id="f37dd-128">AdoEnums.EventStatus.ERRORSOCCURRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f37dd-129">AdoEnums.EventStatus.OK</span><span class="sxs-lookup"><span data-stu-id="f37dd-129">AdoEnums.EventStatus.OK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f37dd-130">AdoEnums.EventStatus.UNWANTEDEVENT</span><span class="sxs-lookup"><span data-stu-id="f37dd-130">AdoEnums.EventStatus.UNWANTEDEVENT</span></span></p></td>
</tr>
</tbody>
</table>

