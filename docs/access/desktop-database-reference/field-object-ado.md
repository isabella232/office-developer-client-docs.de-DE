---
title: Field-Objekt - ActiveX Data Objects (ADO)
TOCTitle: Field object (ADO)
ms:assetid: 1dbd535e-48ad-a5c8-a1b2-6776c1e3e19d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248968(v=office.15)
ms:contentKeyID: 48543600
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a2bf17029a706ad6902a8a01a14e73183f94d7a4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715215"
---
# <a name="field-object-ado"></a><span data-ttu-id="09d65-102">Field-Objekt (ADO)</span><span class="sxs-lookup"><span data-stu-id="09d65-102">Field object (ADO)</span></span>


<span data-ttu-id="09d65-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="09d65-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="09d65-104">Stellt Daten mit einem gemeinsamen Datentyp in einer Spalte dar.</span><span class="sxs-lookup"><span data-stu-id="09d65-104">Represents a column of data with a common data type.</span></span>

## <a name="remarks"></a><span data-ttu-id="09d65-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="09d65-105">Remarks</span></span>

<span data-ttu-id="09d65-p101">Jedes **Field** -Objekt entspricht einer Spalte im [Recordset](recordset-object-ado.md)-Objekt. Mit der [Value](value-property-ado.md)-Eigenschaft von **Field** -Objekten können Sie Daten für den aktuellen Datensatz festlegen oder zurückgeben. Abhängig von der vom Anbieter unterstützten Funktionalität sind bestimmte Auflistungen, Methoden oder Eigenschaften eines **Field** -Objekts möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="09d65-p101">Each **Field** object corresponds to a column in the [Recordset](recordset-object-ado.md). You use the [Value](value-property-ado.md) property of **Field** objects to set or return data for the current record. Depending on the functionality the provider exposes, some collections, methods, or properties of a **Field** object may not be available.</span></span>

<span data-ttu-id="09d65-109">Die Auflistungen, Methoden und Eigenschaften eines **Field** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="09d65-109">With the collections, methods, and properties of a **Field** object, you can do the following:</span></span>

  - <span data-ttu-id="09d65-110">Zurückgeben des Namens eines Felds mit der [Name](name-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="09d65-110">Return the name of a field with the [Name](name-property-ado.md) property.</span></span>

  - <span data-ttu-id="09d65-p102">Anzeigen oder Ändern der Daten im Feld mithilfe der **Value** -Eigenschaft. **Value** ist die Standardeigenschaft des **Field** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="09d65-p102">View or change the data in the field with the **Value** property. **Value** is the default property of the **Field** object.</span></span>

  - <span data-ttu-id="09d65-113">Zurückgeben der grundlegenden Merkmale eines Felds mithilfe der Eigenschaften [Type](type-property-ado.md), [Precision](precision-property-ado.md) und [NumericScale](numericscale-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="09d65-113">Return the basic characteristics of a field with the [Type](type-property-ado.md), [Precision](precision-property-ado.md), and [NumericScale](numericscale-property-ado.md) properties.</span></span>

  - <span data-ttu-id="09d65-114">Zurückgeben der deklarierten Größe eines Felds mit der [DefinedSize](definedsize-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="09d65-114">Return the declared size of a field with the [DefinedSize](definedsize-property-ado.md) property.</span></span>

  - <span data-ttu-id="09d65-115">Zurückgeben der tatsächlichen Größe der Daten in einem bestimmten Feld mit der [ActualSize](actualsize-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="09d65-115">Return the actual size of the data in a given field with the [ActualSize](actualsize-property-ado.md) property.</span></span>

  - <span data-ttu-id="09d65-116">Bestimmen der für ein bestimmtes Feld unterstützten Funktionalitätstypen mithilfe der [Attributes](attributes-property-ado.md)-Eigenschaft und der [Properties](properties-collection-ado.md)-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="09d65-116">Determine what types of functionality are supported for a given field with the [Attributes](attributes-property-ado.md) property and [Properties](properties-collection-ado.md) collection.</span></span>

  - <span data-ttu-id="09d65-117">Bearbeiten der Daten von Feldern, die lange Binär- oder Zeichendaten enthalten, mit den Methoden [AppendChunk](appendchunk-method-ado.md) und [GetChunk](getchunk-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="09d65-117">Manipulate the values of fields containing long binary or long character data with the [AppendChunk](appendchunk-method-ado.md) and [GetChunk](getchunk-method-ado.md) methods.</span></span>

  - <span data-ttu-id="09d65-118">Auflösen von Diskrepanzen in Feldwerten während der Batchaktualisierung mit den Eigenschaften [OriginalValue](originalvalue-property-ado.md) und [UnderlyingValue](underlyingvalue-property-ado.md), sofern der Anbieter Batchaktualisierungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="09d65-118">If the provider supports batch updates, resolve discrepancies in field values during batch updating with the [OriginalValue](originalvalue-property-ado.md) and [UnderlyingValue](underlyingvalue-property-ado.md) properties.</span></span>

<span data-ttu-id="09d65-p103">Alle Metadateneigenschaften (**Name**, **Type**, **DefinedSize**, **Precision** und **NumericScale**) sind vor dem Öffnen des **Recordset**-Objekts des **Field**-Objekts verfügbar. Für die dynamische Erstellung von Formularen ist es nützlich, diese Eigenschaften zu diesem Zeitpunkt festzulegen.</span><span class="sxs-lookup"><span data-stu-id="09d65-p103">All of the metadata properties (**Name**, **Type**, **DefinedSize**, **Precision**, and **NumericScale**) are available before opening the **Field** object's **Recordset**. Setting them at that time is useful for dynamically constructing forms.</span></span>

