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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295702"
---
# <a name="connectiontimeout-property-ado"></a><span data-ttu-id="9807f-102">ConnectionTimeout-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="9807f-102">ConnectionTimeout property (ADO)</span></span>


<span data-ttu-id="9807f-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9807f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9807f-104">Gibt an, wie lange beim Einrichten einer Verbindung gewartet wird, bis der Versuch beendet und ein Fehler generiert wird.</span><span class="sxs-lookup"><span data-stu-id="9807f-104">Indicates how long to wait while establishing a connection before terminating the attempt and generating an error.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="9807f-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="9807f-105">Settings and return values</span></span>

<span data-ttu-id="9807f-106">Sets or returns a **Long** value that indicates, in seconds, how long to wait for the connection to open.</span><span class="sxs-lookup"><span data-stu-id="9807f-106">Sets or returns a **Long** value that indicates, in seconds, how long to wait for the connection to open.</span></span> <span data-ttu-id="9807f-107">Default is 15.</span><span class="sxs-lookup"><span data-stu-id="9807f-107">Default is 15.</span></span>

## <a name="remarks"></a><span data-ttu-id="9807f-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9807f-108">Remarks</span></span>

<span data-ttu-id="9807f-p102">Use the **ConnectionTimeout** property on a [Connection](connection-object-ado.md) object if delays from network traffic or heavy server use make it necessary to abandon a connection attempt. If the time from the **ConnectionTimeout** property setting elapses prior to the opening of the connection, an error occurs and ADO cancels the attempt. If you set the property to zero, ADO will wait indefinitely until the connection is opened. Make sure the provider to which you are writing code supports the **ConnectionTimeout** functionality.</span><span class="sxs-lookup"><span data-stu-id="9807f-p102">Use the **ConnectionTimeout** property on a [Connection](connection-object-ado.md) object if delays from network traffic or heavy server use make it necessary to abandon a connection attempt. If the time from the **ConnectionTimeout** property setting elapses prior to the opening of the connection, an error occurs and ADO cancels the attempt. If you set the property to zero, ADO will wait indefinitely until the connection is opened. Make sure the provider to which you are writing code supports the **ConnectionTimeout** functionality.</span></span>

<span data-ttu-id="9807f-113">Die **ConnectionTimeout** -Eigenschaft hat Lese-/Schreibzugriff, wenn die Verbindung geschlossen ist. Wenn die Verbindung geöffnet ist, ist sie schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9807f-113">The **ConnectionTimeout** property is read/write when the connection is closed and read-only when it is open.</span></span>

