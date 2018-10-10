---
title: Parameter-Objekt (ADO)
TOCTitle: Parameter Object (ADO)
ms:assetid: 7577598e-3d0c-30c6-5f24-1cfe98791798
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249481(v=office.15)
ms:contentKeyID: 48545676
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7667828d2ebfdc554a7120bf495374bc50e51cfc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473467"
---
# <a name="parameter-object-ado"></a><span data-ttu-id="53ba9-102">Parameter-Objekt (ADO)</span><span class="sxs-lookup"><span data-stu-id="53ba9-102">Parameter Object (ADO)</span></span>


<span data-ttu-id="53ba9-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="53ba9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="53ba9-104">Stellt einen Parameter oder ein Argument dar, der bzw. das einem [Command](command-object-ado.md)-Objekt zugeordnet ist, das auf einer parametrisierten Abfrage oder einer gespeicherten Prozedur basiert.</span><span class="sxs-lookup"><span data-stu-id="53ba9-104">Represents a parameter or argument associated with a [Command](command-object-ado.md) object based on a parameterized query or stored procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="53ba9-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="53ba9-105">Remarks</span></span>

<span data-ttu-id="53ba9-p101">Zahlreiche Anbieter unterstützen parametrisierte Befehle. Dies sind Befehle, in denen die gewünschte Aktion einmal definiert wird, aber Variablen (oder Parameter) verwendet werden, um Details des Befehls zu ändern. Eine SQL SELECT-Anweisung kann z. B. einen Parameter verwenden, um die Übereinstimmungskriterien einer WHERE-Klausel zu definieren, und eine andere, um den Spaltennamen für eine SORT BY-Klausel festzulegen.</span><span class="sxs-lookup"><span data-stu-id="53ba9-p101">Many providers support parameterized commands. These are commands in which the desired action is defined once, but variables (or parameters) are used to alter some details of the command. For example, an SQL SELECT statement could use a parameter to define the matching criteria of a WHERE clause, and another to define the column name for a SORT BY clause.</span></span>

<span data-ttu-id="53ba9-p102">**Parameter** -Objekte stellen Parameter, die parametrisierten Abfragen zugeordnet sind, oder die Ein-/Ausgabeargumente und die Rückgabewerte von gespeicherten Prozeduren dar. Abhängig von der Funktionalität des Anbieters sind verschiedene Aufzählungen, Methoden oder Eigenschaften eines **Parameter** -Objekts möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="53ba9-p102">**Parameter** objects represent parameters associated with parameterized queries, or the in/out arguments and the return values of stored procedures. Depending on the functionality of the provider, some collections, methods, or properties of a **Parameter** object may not be available.</span></span>

<span data-ttu-id="53ba9-111">Die Auflistungen, Methoden und Eigenschaften eines **Parameter** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="53ba9-111">With the collections, methods, and properties of a **Parameter** object, you can do the following:</span></span>

  - <span data-ttu-id="53ba9-112">Festlegen oder Zurückgeben des Namens eines Parameters mit der [Name](name-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="53ba9-112">Set or return the name of a parameter with the [Name](name-property-ado.md) property.</span></span>

  - <span data-ttu-id="53ba9-p103">Festlegen oder Zurückgeben eines Parameterwerts mit der [Value](value-property-ado.md)-Eigenschaft. **Value** ist die Standardeigenschaft des **Parameter** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="53ba9-p103">Set or return the value of a parameter with the [Value](value-property-ado.md) property. **Value** is the default property of the **Parameter** object.</span></span>

  - <span data-ttu-id="53ba9-115">Festlegen oder Zurückgeben von Parametermerkmalen mit den Eigenschaften [Attributes](attributes-property-ado.md), [Direction](direction-property-ado.md), [Precision](precision-property-ado.md), [NumericScale](numericscale-property-ado.md), [Size](size-property-ado.md) und [Type](type-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="53ba9-115">Set or return parameter characteristics with the [Attributes](attributes-property-ado.md), [Direction](direction-property-ado.md), [Precision](precision-property-ado.md), [NumericScale](numericscale-property-ado.md), [Size](size-property-ado.md), and [Type](type-property-ado.md) properties.</span></span>

  - <span data-ttu-id="53ba9-116">Übergeben von langen Binär- oder Zeichendaten an einen Parameter mit der [AppendChunk](appendchunk-method-ado.md)-Methode.</span><span class="sxs-lookup"><span data-stu-id="53ba9-116">Pass long binary or character data to a parameter with the [AppendChunk](appendchunk-method-ado.md) method.</span></span>

  - <span data-ttu-id="53ba9-117">Zugreifen auf anbieterspezifische Attribute für die [Properties](properties-collection-ado.md)-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="53ba9-117">Access provider-specific attributes with the [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="53ba9-p104">Wenn Sie die Namen und Eigenschaften der Parameter kennen, die der aufzurufenden gespeicherten Prozedur oder parametrisierten Abfrage zugeordnet sind, können Sie die [CreateParameter](createparameter-method-ado.md)-Methode verwenden, um **Parameter** -Objekte mit den betreffenden Eigenschaftswerten zu erstellen und sie mit der [Append](append-method-ado.md)-Methode der [Parameters](parameters-collection-ado.md)-Auflistung hinzufügen. Auf diese Weise können Sie Parameterwerte festlegen und zurückgeben, ohne die [Refresh](refresh-method-ado.md)-Methode für die **Parameters** -Auflistung aufzurufen, um die Parameterinformationen des Anbieters abzufragen, einem potenziell ressourcenintensiven Vorgang.</span><span class="sxs-lookup"><span data-stu-id="53ba9-p104">If you know the names and properties of the parameters associated with the stored procedure or parameterized query you wish to call, you can use the [CreateParameter](createparameter-method-ado.md) method to create **Parameter** objects with the appropriate property settings and use the [Append](append-method-ado.md) method to add them to the [Parameters](parameters-collection-ado.md) collection. This lets you set and return parameter values without having to call the [Refresh](refresh-method-ado.md) method on the **Parameters** collection to retrieve the parameter information from the provider, a potentially resource-intensive operation.</span></span>

