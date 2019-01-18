---
title: ConnectionTimeout-Eigenschaft (ADO)
TOCTitle: ConnectionTimeout property (ADO)
ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15)
ms:contentKeyID: 48548589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0526ee6a0d6cf9aa8f9263e8f3d31e66fad7da82
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700934"
---
# <a name="connectiontimeout-property-ado"></a><span data-ttu-id="8cadb-102">ConnectionTimeout-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="8cadb-102">ConnectionTimeout property (ADO)</span></span>


<span data-ttu-id="8cadb-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8cadb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8cadb-104">Gibt an, wie lange beim Einrichten einer Verbindung gewartet wird, bis der Versuch beendet und ein Fehler generiert wird.</span><span class="sxs-lookup"><span data-stu-id="8cadb-104">Indicates how long to wait while establishing a connection before terminating the attempt and generating an error.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="8cadb-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cadb-105">Settings and return values</span></span>

<span data-ttu-id="8cadb-p101">Mit dieser Eigenschaft wird ein Wert vom Datentyp Long festgelegt oder zurückgegeben, der angibt, wie viele Sekunden gewartet werden soll, bis die Verbindung geöffnet wird. Der Standard ist 15.</span><span class="sxs-lookup"><span data-stu-id="8cadb-p101">Sets or returns a **Long** value that indicates, in seconds, how long to wait for the connection to open. Default is 15.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cadb-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8cadb-108">Remarks</span></span>

<span data-ttu-id="8cadb-109">Verwenden Sie die **ConnectionTimeout** -Eigenschaft für ein [Connection](connection-object-ado.md) -Objekt Wenn Verzögerungen von Datenverkehr oder fett Netzwerkserver verwenden es erforderlich machen, einen Verbindungsversuch zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="8cadb-109">Use the **ConnectionTimeout** property on a [Connection](connection-object-ado.md) object if delays from network traffic or heavy server use make it necessary to abandon a connection attempt.</span></span> <span data-ttu-id="8cadb-110">Wenn das von der Einstellung der **ConnectionTimeout** -Eigenschaft vor dem Öffnen der Verbindung verstrichen, tritt ein Fehler auf, und ADO bricht den Versuch ab.</span><span class="sxs-lookup"><span data-stu-id="8cadb-110">If the time from the **ConnectionTimeout** property setting elapses prior to the opening of the connection, an error occurs and ADO cancels the attempt.</span></span> <span data-ttu-id="8cadb-111">Wenn Sie die Eigenschaft auf 0 (null) festlegen, wartet ADO unbegrenzt, bis die Verbindung geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="8cadb-111">If you set the property to zero, ADO will wait indefinitely until the connection is opened.</span></span> <span data-ttu-id="8cadb-112">Stellen Sie sicher, dass der Anbieter, den Sie Code schreiben, die **ConnectionTimeout** -Funktionalität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8cadb-112">Make sure the provider to which you are writing code supports the **ConnectionTimeout** functionality.</span></span>

<span data-ttu-id="8cadb-113">Die **ConnectionTimeout** -Eigenschaft hat Lese-/Schreibzugriff, wenn die Verbindung geschlossen ist. Wenn die Verbindung geöffnet ist, ist sie schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8cadb-113">The **ConnectionTimeout** property is read/write when the connection is closed and read-only when it is open.</span></span>

