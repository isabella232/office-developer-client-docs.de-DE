---
title: CommandTimeout-Eigenschaft (ADO)
TOCTitle: CommandTimeout property (ADO)
ms:assetid: a0b6209c-9feb-08ae-002a-15d1d20734a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249739(v=office.15)
ms:contentKeyID: 48546714
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231124
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9d44bc8fae0143b183ef54120cdaaf91337f36f8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700115"
---
# <a name="commandtimeout-property-ado"></a><span data-ttu-id="e6a9f-102">CommandTimeout-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="e6a9f-102">CommandTimeout property (ADO)</span></span>


<span data-ttu-id="e6a9f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e6a9f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e6a9f-104">Gibt an, wie lange beim Ausführen eines Befehls gewartet wird, bis der Versuch beendet und ein Fehler generiert wird.</span><span class="sxs-lookup"><span data-stu-id="e6a9f-104">Indicates how long to wait while executing a command before terminating the attempt and generating an error.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="e6a9f-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e6a9f-105">Settings and return values</span></span>

<span data-ttu-id="e6a9f-p101">Mit dieser Eigenschaft wird ein Wert vom Datentyp Long festgelegt oder zurückgegeben, der angibt, wie lange in Sekunden gewartet werden soll, bis ein Befehl ausgeführt wird. Der Standard ist 30.</span><span class="sxs-lookup"><span data-stu-id="e6a9f-p101">Sets or returns a **Long** value that indicates, in seconds, how long to wait for a command to execute. Default is 30.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6a9f-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e6a9f-108">Remarks</span></span>

<span data-ttu-id="e6a9f-109">Verwenden Sie die **CommandTimeout** -Eigenschaft in einem [Connection](connection-object-ado.md) -Objekt oder ein [Command](command-object-ado.md) -Objekt, um den Abbruch des einen Aufruf der [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) -Methode, aufgrund Verzögerungen aus Netzwerkverkehrs oder fett Server Nutzung zu erlauben.</span><span class="sxs-lookup"><span data-stu-id="e6a9f-109">Use the **CommandTimeout** property on a [Connection](connection-object-ado.md) object or [Command](command-object-ado.md) object to allow the cancellation of an [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method call, due to delays from network traffic or heavy server use.</span></span> <span data-ttu-id="e6a9f-110">Wenn das Intervall, in der **CommandTimeout** -Eigenschaft verstreicht, bevor der Befehl abgeschlossen wurde, tritt ein Fehler auf, und ADO bricht den Befehl ab.</span><span class="sxs-lookup"><span data-stu-id="e6a9f-110">If the interval set in the **CommandTimeout** property elapses before the command completes execution, an error occurs and ADO cancels the command.</span></span> <span data-ttu-id="e6a9f-111">Wenn Sie die Eigenschaft auf 0 (null) festlegen, wartet ADO unbegrenzt, bis die Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="e6a9f-111">If you set the property to zero, ADO will wait indefinitely until the execution is complete.</span></span> <span data-ttu-id="e6a9f-112">Vergewissern Sie sich die Anbieter- und Datenquellen, die Sie Code Unterstützung die **CommandTimeout** -Funktionalität schreiben.</span><span class="sxs-lookup"><span data-stu-id="e6a9f-112">Make sure the provider and data source to which you are writing code support the **CommandTimeout** functionality.</span></span>

<span data-ttu-id="e6a9f-113">Die Einstellung von **CommandTimeout** in einem **Connection** -Objekt hat keine Auswirkung auf die Einstellung von **CommandTimeout** in einem **Command** -Objekt im gleichen **Connection** -Objekt. Das heißt, die **CommandTimeout** -Eigenschaft eines **Command** -Objekts erbt den Wert der **CommandTimeout** -Eigenschaft des **Connection** -Objekts nicht.</span><span class="sxs-lookup"><span data-stu-id="e6a9f-113">The **CommandTimeout** setting on a **Connection** object has no effect on the **CommandTimeout** setting on a **Command** object on the same **Connection**; that is, the **Command** object's **CommandTimeout** property does not inherit the value of the **Connection** object's **CommandTimeout** value.</span></span>

<span data-ttu-id="e6a9f-114">In einem **Connection** -Objekt behält die **CommandTimeout** -Eigenschaft nach dem Öffnen des **Connection** -Objekts Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e6a9f-114">On a **Connection** object, the **CommandTimeout** property remains read/write after the **Connection** is opened.</span></span>

