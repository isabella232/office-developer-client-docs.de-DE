---
title: CommandType-Eigenschaft (ADO)
TOCTitle: CommandType property (ADO)
ms:assetid: c8d4fc1c-502b-11f3-af9d-605a03b6f056
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15)
ms:contentKeyID: 48547663
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231125
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 89264889281070b8a477c3a04b8f6f5735efdf3e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880236"
---
# <a name="commandtype-property-ado"></a><span data-ttu-id="0d25c-102">CommandType-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="0d25c-102">CommandType property (ADO)</span></span>


<span data-ttu-id="0d25c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d25c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0d25c-104">Gibt den Typ eines [Command](command-object-ado.md)-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="0d25c-104">Indicates the type of a [Command](command-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="0d25c-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="0d25c-105">Settings and return values</span></span>

<span data-ttu-id="0d25c-106">Mit dieser Eigenschaft wird mindestens ein [CommandTypeEnum](commandtypeenum.md)-Wert festgelegt oder zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0d25c-106">Sets or returns one or more [CommandTypeEnum](commandtypeenum.md) values.</span></span>

> [!NOTE]
> <span data-ttu-id="0d25c-p101">[!HINWEIS] Verwenden Sie die **CommandTypeEnum** -Werte von **adCmdFile** oder **adCmdTableDirect** nicht zusammen mit **CommandType**. Diese Werte können nur als Optionen für die Methoden [Open](open-method-ado-recordset.md) und [Requery](requery-method-ado.md) eines [Recordset](recordset-object-ado.md)-Objekts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d25c-p101">Do not use the **CommandTypeEnum** values of **adCmdFile** or **adCmdTableDirect** with **CommandType**. These values can only be used as options with the [Open](open-method-ado-recordset.md) and [Requery](requery-method-ado.md) methods of a [Recordset](recordset-object-ado.md).</span></span>


## <a name="remarks"></a><span data-ttu-id="0d25c-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0d25c-109">Remarks</span></span>

<span data-ttu-id="0d25c-110">Verwenden Sie die **CommandType** -Eigenschaft zum Optimieren der Evaluierung der [CommandText](commandtext-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0d25c-110">Use the **CommandType** property to optimize evaluation of the [CommandText](commandtext-property-ado.md) property.</span></span>

<span data-ttu-id="0d25c-p102">Wenn der Wert der **CommandType** -Eigenschaft gleich **adCmdUnknown** ist (Standardwert), kann die Leistung beeinträchtigt sein. ADO muss dann nämlich den Anbieter aufrufen, um zu ermitteln, ob es sich bei der **CommandText** -Eigenschaft um eine SQL-Anweisung, eine gespeicherte Prozedur oder einen Tabellennamen handelt. Falls Sie wissen, welchen Befehlstyp Sie verwenden, wird ADO durch Festlegen der **CommandType** -Eigenschaft angewiesen, direkt zum entsprechenden Code zu wechseln. Wenn die **CommandType** -Eigenschaft nicht mit dem Befehlstyp in der **CommandText** -Eigenschaft übereinstimmt, tritt beim Aufrufen der [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)-Methode ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="0d25c-p102">If the **CommandType** property value equals **adCmdUnknown** (the default value), you may experience diminished performance because ADO must make calls to the provider to determine if the **CommandText** property is an SQL statement, a stored procedure, or a table name. If you know what type of command you're using, setting the **CommandType** property instructs ADO to go directly to the relevant code. If the **CommandType** property does not match the type of command in the **CommandText** property, an error occurs when you call the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method.</span></span>

