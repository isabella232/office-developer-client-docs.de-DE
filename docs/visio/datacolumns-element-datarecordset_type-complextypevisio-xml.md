---
title: DataColumns-Element (DataRecordSet_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: Enthält alle DataColumn-Elemente in einem Datenrecordset.
ms.openlocfilehash: b90b6cb18fc2bd1edc393d58a9d761cfb36ea220
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796783"
---
# <a name="datacolumns-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="472ac-103">DataColumns-Element (DataRecordSet_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="472ac-103">DataColumns element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="472ac-104">Enthält alle **DataColumn** -Elemente in einem Datenrecordset.</span><span class="sxs-lookup"><span data-stu-id="472ac-104">Contains all the **DataColumn** elements in a data recordset.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="472ac-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="472ac-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="472ac-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="472ac-106">**Element type**</span></span> <br/> |[<span data-ttu-id="472ac-107">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="472ac-107">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="472ac-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="472ac-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="472ac-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="472ac-109">**Schema file**</span></span> <br/> |<span data-ttu-id="472ac-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="472ac-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="472ac-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="472ac-111">**Document parts**</span></span> <br/> |<span data-ttu-id="472ac-112">Recordsets.Xml</span><span class="sxs-lookup"><span data-stu-id="472ac-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="472ac-113">Definition</span><span class="sxs-lookup"><span data-stu-id="472ac-113">Definition</span></span>

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="472ac-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="472ac-114">Elements and attributes</span></span>

<span data-ttu-id="472ac-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="472ac-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="472ac-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="472ac-116">Parent elements</span></span>

|<span data-ttu-id="472ac-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="472ac-117">**Element**</span></span>|<span data-ttu-id="472ac-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="472ac-118">**Type**</span></span>|<span data-ttu-id="472ac-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="472ac-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="472ac-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="472ac-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="472ac-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="472ac-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="472ac-122">Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.</span><span class="sxs-lookup"><span data-stu-id="472ac-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="472ac-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="472ac-123">Child elements</span></span>

|<span data-ttu-id="472ac-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="472ac-124">**Element**</span></span>|<span data-ttu-id="472ac-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="472ac-125">**Type**</span></span>|<span data-ttu-id="472ac-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="472ac-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="472ac-127">DataColumn</span><span class="sxs-lookup"><span data-stu-id="472ac-127">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="472ac-128">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="472ac-128">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="472ac-129">Definiert, wie eine Datenspalte im Fenster **Externe Daten** in der Visio-Benutzeroberfläche angezeigt und berechtigt ist die Daten in der Spalte Datentyp zu definieren und die Formatierung.</span><span class="sxs-lookup"><span data-stu-id="472ac-129">Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="472ac-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="472ac-130">Attributes</span></span>

|<span data-ttu-id="472ac-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="472ac-131">**Attribute**</span></span>|<span data-ttu-id="472ac-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="472ac-132">**Type**</span></span>|<span data-ttu-id="472ac-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="472ac-133">**Required**</span></span>|<span data-ttu-id="472ac-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="472ac-134">**Description**</span></span>|<span data-ttu-id="472ac-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="472ac-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="472ac-136">SortAsc</span><span class="sxs-lookup"><span data-stu-id="472ac-136">SortAsc</span></span>  <br/> |<span data-ttu-id="472ac-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="472ac-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="472ac-138">Optional</span><span class="sxs-lookup"><span data-stu-id="472ac-138">optional</span></span>  <br/> |<span data-ttu-id="472ac-139">Die Spalte, auf dem die Daten sortiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="472ac-139">The column on which to sort the data.</span></span>  <br/> |<span data-ttu-id="472ac-140">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="472ac-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="472ac-141">SortColumn</span><span class="sxs-lookup"><span data-stu-id="472ac-141">SortColumn</span></span>  <br/> |<span data-ttu-id="472ac-142">XSD: String</span><span class="sxs-lookup"><span data-stu-id="472ac-142">xsd:string</span></span>  <br/> |<span data-ttu-id="472ac-143">Optional</span><span class="sxs-lookup"><span data-stu-id="472ac-143">optional</span></span>  <br/> |<span data-ttu-id="472ac-144">An, ob die Spalte **SortColumn** in aufsteigender (1) oder absteigender Reihenfolge (0) sortiert.</span><span class="sxs-lookup"><span data-stu-id="472ac-144">Whether to sort the **SortColumn** column in ascending (1) or descending (0) order.</span></span>  <br/> |<span data-ttu-id="472ac-145">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="472ac-145">Values of the xsd:string type.</span></span>  <br/> |
   

