---
title: Prepared-Eigenschaft (ADO)
TOCTitle: Prepared property (ADO)
ms:assetid: 33becda2-faab-5000-8904-6ffd8c5805f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249105(v=office.15)
ms:contentKeyID: 48544116
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231161
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a9c275cfe16ac2f1b1f9d2a8c0ac857010ed4572
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878751"
---
# <a name="prepared-property-ado"></a><span data-ttu-id="5b4ac-102">Prepared-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="5b4ac-102">Prepared property (ADO)</span></span>


<span data-ttu-id="5b4ac-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5b4ac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5b4ac-104">Gibt an, ob eine kompilierte Version eines Befehls vor dem Ausführen gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b4ac-104">Indicates whether to save a compiled version of a command before execution.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="5b4ac-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="5b4ac-105">Settings and return values</span></span>

<span data-ttu-id="5b4ac-106">Legt einen **Boolean** -Wert fest oder gibt den Wert zurück. Ein Wert **True** gibt an, dass der Befehl vorbereitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b4ac-106">Sets or returns a **Boolean** value that, if set to **True**, indicates that the command should be prepared.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b4ac-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5b4ac-107">Remarks</span></span>

<span data-ttu-id="5b4ac-p101">Verwenden Sie die **Prepared** -Eigenschaft, wenn der Anbieter eine vorbereitete (bzw. kompilierte) Version der in der [CommandText](commandtext-property-ado.md)-Eigenschaft angegebenen Abfrage speichern soll, bevor ein [Command](command-object-ado.md)-Objekt erstmalig ausgeführt wird. Dadurch wird möglicherweise das erste Ausführen des zugehörigen Befehls zwar verlangsamt, aber da der Anbieter nach dem Kompilieren des Befehls die kompilierte Version zum weiteren Ausführen des Befehls verwendet, ergibt sich eine verbesserte Leistung.</span><span class="sxs-lookup"><span data-stu-id="5b4ac-p101">Use the **Prepared** property to have the provider save a prepared (or compiled) version of the query specified in the [CommandText](commandtext-property-ado.md) property before a [Command](command-object-ado.md) object's first execution. This may slow a command's first execution, but once the provider compiles a command, the provider will use the compiled version of the command for any subsequent executions, which will result in improved performance.</span></span>

<span data-ttu-id="5b4ac-110">Ist die Eigenschaft auf **False** festgelegt, führt der Anbieter das **Command** -Objekt direkt aus, ohne eine kompilierte Version zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5b4ac-110">If the property is **False**, the provider will execute the **Command** object directly without creating a compiled version.</span></span>

<span data-ttu-id="5b4ac-p102">Unterstützt der Anbieter die Vorbereitung von Befehlen nicht, wird möglicherweise ein Fehler zurückgegeben, sobald diese Eigenschaft auf **True** festgelegt wird. Wenn kein Fehler zurückgegeben wird, wird die Anforderung zum Vorbereiten des Befehls einfach ignoriert und die **Prepared** -Eigenschaft auf **False** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5b4ac-p102">If the provider does not support command preparation, it may return an error as soon as this property is set to **True**. If it does not return an error, it simply ignores the request to prepare the command and sets the **Prepared** property to **False**.</span></span>

