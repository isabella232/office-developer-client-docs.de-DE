---
title: EventStatusEnum (Access PC-Datenbank-Referenz)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 6e8408e2c73a60ae543bc9982de2f2547f54d1d2
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861533"
---
# <a name="eventstatusenum"></a><span data-ttu-id="35757-102">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="35757-102">EventStatusEnum</span></span>

<span data-ttu-id="35757-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="35757-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="35757-104">Gibt den aktuellen Status der Ausführung eines Ereignisses an.</span><span class="sxs-lookup"><span data-stu-id="35757-104">Specifies the current status of the execution of an event.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="35757-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="35757-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="35757-106">Wert</span><span class="sxs-lookup"><span data-stu-id="35757-106">Value</span></span></p></th>
<th><p><span data-ttu-id="35757-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35757-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35757-108"><strong>adStatusCancel fest</strong></span><span class="sxs-lookup"><span data-stu-id="35757-108"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="35757-109">4</span><span class="sxs-lookup"><span data-stu-id="35757-109">4</span></span></p></td>
<td><p><span data-ttu-id="35757-110">Fordert den Abbruch des Vorgangs an, der zum Ereignis führte.</span><span class="sxs-lookup"><span data-stu-id="35757-110">Requests cancellation of the operation that caused the event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35757-111"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="35757-111"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="35757-112">3</span><span class="sxs-lookup"><span data-stu-id="35757-112">3</span></span></p></td>
<td><p><span data-ttu-id="35757-113">Gibt an, dass der Vorgang keinen Abbruch der ausstehenden Operation anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="35757-113">Indicates that the operation cannot request cancellation of the pending operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35757-114"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="35757-114"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="35757-115">2</span><span class="sxs-lookup"><span data-stu-id="35757-115">2</span></span></p></td>
<td><p><span data-ttu-id="35757-116">Gibt an, dass der Vorgang, der das Ereignis verursachte, aufgrund eines Fehlers oder mehrerer Fehler fehlschlug.</span><span class="sxs-lookup"><span data-stu-id="35757-116">Indicates that the operation that caused the event failed due to an error or errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35757-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="35757-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="35757-118">1</span><span class="sxs-lookup"><span data-stu-id="35757-118">1</span></span></p></td>
<td><p><span data-ttu-id="35757-119">Gibt an, dass der Vorgang, der das Ereignis verursachte, erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="35757-119">Indicates that the operation that caused the event was successful.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35757-120"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="35757-120"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="35757-121">5</span><span class="sxs-lookup"><span data-stu-id="35757-121">5</span></span></p></td>
<td><p><span data-ttu-id="35757-122">Verhindert nachfolgende Benachrichtigungen, bevor die Ereignismethode die Ausführung beendet hat.</span><span class="sxs-lookup"><span data-stu-id="35757-122">Prevents subsequent notifications before the event method has finished executing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="35757-123">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="35757-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="35757-124">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="35757-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="35757-125">Konstante</span><span class="sxs-lookup"><span data-stu-id="35757-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35757-126">AdoEnums.EventStatus.CANCEL</span><span class="sxs-lookup"><span data-stu-id="35757-126">AdoEnums.EventStatus.CANCEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35757-127">AdoEnums.EventStatus.CANTDENY</span><span class="sxs-lookup"><span data-stu-id="35757-127">AdoEnums.EventStatus.CANTDENY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35757-128">AdoEnums.EventStatus.ERRORSOCCURRED</span><span class="sxs-lookup"><span data-stu-id="35757-128">AdoEnums.EventStatus.ERRORSOCCURRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35757-129">AdoEnums.EventStatus.OK</span><span class="sxs-lookup"><span data-stu-id="35757-129">AdoEnums.EventStatus.OK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35757-130">AdoEnums.EventStatus.UNWANTEDEVENT</span><span class="sxs-lookup"><span data-stu-id="35757-130">AdoEnums.EventStatus.UNWANTEDEVENT</span></span></p></td>
</tr>
</tbody>
</table>

