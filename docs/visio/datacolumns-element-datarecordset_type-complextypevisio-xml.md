---
title: DataColumns-Element (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: Enthält alle DataColumn-Elemente in einem Datenrecordset.
ms.openlocfilehash: e42354076c5e3e34c118145e7ec7fcdbd4977372
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541197"
---
# <a name="datacolumns-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="70091-103">DataColumns-Element (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="70091-103">DataColumns element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="70091-104">Enthält alle **DataColumn** -Elemente in einem Datenrecordset.</span><span class="sxs-lookup"><span data-stu-id="70091-104">Contains all the **DataColumn** elements in a data recordset.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="70091-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="70091-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70091-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="70091-106">**Element type**</span></span> <br/> |[<span data-ttu-id="70091-107">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="70091-107">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="70091-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="70091-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="70091-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="70091-109">**Schema file**</span></span> <br/> |<span data-ttu-id="70091-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="70091-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="70091-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="70091-111">**Document parts**</span></span> <br/> |<span data-ttu-id="70091-112">Recordsets. XML</span><span class="sxs-lookup"><span data-stu-id="70091-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="70091-113">Definition</span><span class="sxs-lookup"><span data-stu-id="70091-113">Definition</span></span>

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="70091-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="70091-114">Elements and attributes</span></span>

<span data-ttu-id="70091-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="70091-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="70091-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="70091-116">Parent elements</span></span>

|<span data-ttu-id="70091-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="70091-117">**Element**</span></span>|<span data-ttu-id="70091-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="70091-118">**Type**</span></span>|<span data-ttu-id="70091-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="70091-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="70091-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="70091-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="70091-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="70091-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="70091-122">Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.</span><span class="sxs-lookup"><span data-stu-id="70091-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="70091-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="70091-123">Child elements</span></span>

|<span data-ttu-id="70091-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="70091-124">**Element**</span></span>|<span data-ttu-id="70091-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="70091-125">**Type**</span></span>|<span data-ttu-id="70091-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="70091-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="70091-127">DataColumn</span><span class="sxs-lookup"><span data-stu-id="70091-127">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="70091-128">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="70091-128">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="70091-129">Definiert, wie eine Datenspalte im Fenster **externe Daten** auf der Visio-Benutzeroberfläche angezeigt wird, und qualifiziert die Daten in der Spalte, indem Sie den Datentyp und die Formatierung definiert.</span><span class="sxs-lookup"><span data-stu-id="70091-129">Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="70091-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="70091-130">Attributes</span></span>

|<span data-ttu-id="70091-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="70091-131">**Attribute**</span></span>|<span data-ttu-id="70091-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="70091-132">**Type**</span></span>|<span data-ttu-id="70091-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="70091-133">**Required**</span></span>|<span data-ttu-id="70091-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="70091-134">**Description**</span></span>|<span data-ttu-id="70091-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="70091-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="70091-136">SortAsc</span><span class="sxs-lookup"><span data-stu-id="70091-136">SortAsc</span></span>  <br/> |<span data-ttu-id="70091-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="70091-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="70091-138">Optional</span><span class="sxs-lookup"><span data-stu-id="70091-138">optional</span></span>  <br/> |<span data-ttu-id="70091-139">Die Spalte, für die die Daten sortiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="70091-139">The column on which to sort the data.</span></span>  <br/> |<span data-ttu-id="70091-140">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="70091-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="70091-141">SortColumn</span><span class="sxs-lookup"><span data-stu-id="70091-141">SortColumn</span></span>  <br/> |<span data-ttu-id="70091-142">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="70091-142">xsd:string</span></span>  <br/> |<span data-ttu-id="70091-143">Optional</span><span class="sxs-lookup"><span data-stu-id="70091-143">optional</span></span>  <br/> |<span data-ttu-id="70091-144">Gibt an, ob die **SortColumn** -Spalte in aufsteigender (1) oder absteigender Reihenfolge (0) sortiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="70091-144">Whether to sort the **SortColumn** column in ascending (1) or descending (0) order.</span></span>  <br/> |<span data-ttu-id="70091-145">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="70091-145">Values of the xsd:string type.</span></span>  <br/> |
   

