---
title: Source-Eigenschaft (ADO-Recordset)
TOCTitle: Source property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 26f41181f1233931f24ff091b3009dfa7a5d6ff3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306411"
---
# <a name="source-property-ado-recordset"></a><span data-ttu-id="81234-102">Source-Eigenschaft (ADO-Recordset)</span><span class="sxs-lookup"><span data-stu-id="81234-102">Source property (ADO Recordset)</span></span>


<span data-ttu-id="81234-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="81234-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="81234-104">Gibt die Datenquelle für ein [Recordset](recordset-object-ado.md)-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="81234-104">Indicates the data source for a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="81234-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="81234-105">Settings and return values</span></span>

<span data-ttu-id="81234-106">Legt einen **String**-Wert oder einen [Command](command-object-ado.md)-Objektverweis fest; gibt nur einen **String**-Wert zurück, der die Quelle des **Recordset**-Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="81234-106">Sets a **String** value or [Command](command-object-ado.md) object reference; returns only a **String** value that indicates the source of the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="81234-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81234-107">Remarks</span></span>

<span data-ttu-id="81234-108">Geben Sie mit der **Source**-Eigenschaft die Datenquelle für ein **Recordset**-Objekt an, und verwenden Sie dazu Folgendes: eine **Command**-Objektvariable, eine SQL-Anweisung, eine gespeicherte Prozedur oder einen Tabellennamen.</span><span class="sxs-lookup"><span data-stu-id="81234-108">Use the **Source** property to specify a data source for a **Recordset** object using one of the following: a **Command** object variable, an SQL statement, a stored procedure, or a table name.</span></span>

<span data-ttu-id="81234-p101">Wenn Sie die **Source**-Eigenschaft für ein **Command**-Objekt festlegen, erbt die [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft des **Recordset**-Objekts den Wert der **ActiveConnection**-Eigenschaft, die für das **Command**-Objekt angegeben wurde. Beim Lesen der **Source**-Eigenschaft wird jedoch kein **Command**-Objekt zurückgegeben. Stattdessen wird die [CommandText](commandtext-property-ado.md)-Eigenschaft des **Command**-Objekts zurückgegeben, für die Sie die **Source**-Eigenschaft festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="81234-p101">If you set the **Source** property to a **Command** object, the [ActiveConnection](activeconnection-property-ado.md) property of the **Recordset** object will inherit the value of the **ActiveConnection** property for the specified **Command** object. However, reading the **Source** property does not return a **Command** object; instead, it returns the [CommandText](commandtext-property-ado.md) property of the **Command** object to which you set the **Source** property.</span></span>

<span data-ttu-id="81234-111">Wenn die **Source**-Eigenschaft eine SQL-Anweisung, eine gespeicherte Prozedur oder ein Tabellenname ist, können Sie die Leistung optimieren, indem Sie das entsprechende Argument *Options* durch den [Open](open-method-ado-recordset.md)-Methodenaufruf übergeben.</span><span class="sxs-lookup"><span data-stu-id="81234-111">If the **Source** property is an SQL statement, a stored procedure, or a table name, you can optimize performance by passing the appropriate *Options* argument with the [Open](open-method-ado-recordset.md) method call.</span></span>

<span data-ttu-id="81234-112">Die **Source**-Eigenschaft ist bei geschlossenen **Recordset**-Objekten nicht schreibgeschützt und bei geöffneten **Recordset**-Objekten schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="81234-112">The **Source** property is read/write for closed **Recordset** objects and read-only for open **Recordset** objects.</span></span>

