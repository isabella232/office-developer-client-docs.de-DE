---
title: Direction-Eigenschaft (ADO)
TOCTitle: Direction property (ADO)
ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15)
ms:contentKeyID: 48544823
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b9e34522a69b2e79f8ef44b912e2c0648c5b813d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881293"
---
# <a name="direction-property-ado"></a><span data-ttu-id="f62fb-102">Direction-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="f62fb-102">Direction property (ADO)</span></span>


<span data-ttu-id="f62fb-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f62fb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f62fb-104">Gibt an, ob der [Parameter](parameter-object-ado.md) einen Eingabeparameter, einen Ausgabeparameter oder einen Ein- und Ausgabeparameter darstellt, oder ob der Parameter der Rückgabewert aus einer gespeicherten Prozedur ist.</span><span class="sxs-lookup"><span data-stu-id="f62fb-104">Indicates whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, an input and an output parameter, or if the parameter is the return value from a stored procedure.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="f62fb-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f62fb-105">Settings and return values</span></span>

<span data-ttu-id="f62fb-106">Mit dieser Eigenschaft wird ein [ParameterDirectionEnum](parameterdirectionenum.md)-Wert festgelegt oder zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f62fb-106">Sets or returns a [ParameterDirectionEnum](parameterdirectionenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f62fb-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f62fb-107">Remarks</span></span>

<span data-ttu-id="f62fb-p101">Mit der **Direction** -Eigenschaft geben Sie an, wie ein Parameter an eine oder aus einer Prozedur übergeben wird. Die **Direction** -Eigenschaft bietet Lese-/Schreibzugriff. Dadurch können Sie Anbieter verwenden, die diese Informationen nicht zurückgeben, oder Sie können diese Informationen festlegen, wenn ADO den Anbieter nicht extra aufrufen soll, um Parameterinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f62fb-p101">Use the **Direction** property to specify how a parameter is passed to or from a procedure. The **Direction** property is read/write; this allows you to work with providers that don't return this information or to set this information when you don't want ADO to make an extra call to the provider to retrieve parameter information.</span></span>

<span data-ttu-id="f62fb-p102">Nicht alle Anbieter können die Richtung von Parametern in ihren gespeicherten Prozeduren bestimmen. In diesen Fällen müssen Sie die **Direction** -Eigenschaft festlegen, bevor Sie die Abfrage ausführen.</span><span class="sxs-lookup"><span data-stu-id="f62fb-p102">Not all providers can determine the direction of parameters in their stored procedures. In these cases, you must set the **Direction** property before you execute the query.</span></span>

