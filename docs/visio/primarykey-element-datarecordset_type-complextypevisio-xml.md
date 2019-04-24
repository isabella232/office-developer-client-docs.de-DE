---
title: Primary-Element (DataRecordSet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: Identifiziert eine oder mehrere Primärschlüsselspalten im Datenrecordset.
ms.openlocfilehash: c001c343c33e65c3990744b885f1c345575b1ab3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355996"
---
# <a name="primarykey-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="2764b-103">Primary-Element (DataRecordSet_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="2764b-103">PrimaryKey element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="2764b-104">Identifiziert eine oder mehrere Primärschlüsselspalten im Datenrecordset.</span><span class="sxs-lookup"><span data-stu-id="2764b-104">Identifies one or more primary-key columns in the data recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2764b-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2764b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2764b-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="2764b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2764b-107">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="2764b-107">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2764b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2764b-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2764b-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="2764b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2764b-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="2764b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2764b-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="2764b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2764b-112">Recordsets. XML</span><span class="sxs-lookup"><span data-stu-id="2764b-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2764b-113">Definition</span><span class="sxs-lookup"><span data-stu-id="2764b-113">Definition</span></span>

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2764b-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="2764b-114">Elements and attributes</span></span>

<span data-ttu-id="2764b-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="2764b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2764b-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2764b-116">Parent elements</span></span>

|<span data-ttu-id="2764b-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="2764b-117">**Element**</span></span>|<span data-ttu-id="2764b-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="2764b-118">**Type**</span></span>|<span data-ttu-id="2764b-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2764b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2764b-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="2764b-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2764b-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="2764b-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2764b-122">Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.</span><span class="sxs-lookup"><span data-stu-id="2764b-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2764b-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2764b-123">Child elements</span></span>

|<span data-ttu-id="2764b-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="2764b-124">**Element**</span></span>|<span data-ttu-id="2764b-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="2764b-125">**Type**</span></span>|<span data-ttu-id="2764b-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2764b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2764b-127">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="2764b-127">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2764b-128">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="2764b-128">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2764b-129">Gibt den Wert dieser Komponente des Primärschlüssels für eine einzelne Zeile eines Recordset-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="2764b-129">Specifies the value of this component of the primary key for an individual row of a recordset.</span></span> <span data-ttu-id="2764b-130">Dieses untergeordnete Element muss mindestens ein Vorkommen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2764b-130">There MUST be at least one occurrence of this child element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="2764b-131">Attribute</span><span class="sxs-lookup"><span data-stu-id="2764b-131">Attributes</span></span>

|<span data-ttu-id="2764b-132">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="2764b-132">**Attribute**</span></span>|<span data-ttu-id="2764b-133">**Typ**</span><span class="sxs-lookup"><span data-stu-id="2764b-133">**Type**</span></span>|<span data-ttu-id="2764b-134">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="2764b-134">**Required**</span></span>|<span data-ttu-id="2764b-135">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2764b-135">**Description**</span></span>|<span data-ttu-id="2764b-136">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="2764b-136">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2764b-137">ColumnName-Nr.</span><span class="sxs-lookup"><span data-stu-id="2764b-137">ColumnNameID</span></span>  <br/> |<span data-ttu-id="2764b-138">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2764b-138">xsd:string</span></span>  <br/> |<span data-ttu-id="2764b-139">Optional</span><span class="sxs-lookup"><span data-stu-id="2764b-139">optional</span></span>  <br/> |<span data-ttu-id="2764b-140">Gibt den Namen eines Felds an, das eine Komponente des Primärschlüssels darstellt.</span><span class="sxs-lookup"><span data-stu-id="2764b-140">Specifies the name of a field that is a component of the primary key.</span></span> <span data-ttu-id="2764b-141">Es muss der Wert des **ColumnName** -Attributs eines DataColumn_Type-Nachfolger Elements des DataRecordSet_Type sein, dessen Primärschlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2764b-141">It MUST be the value of the **ColumnNameID** attribute of a DataColumn_Type descendant element of the DataRecordSet_Type whose primary key is being specified.</span></span>  <br/> |<span data-ttu-id="2764b-142">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="2764b-142">Values of the xsd:string type.</span></span>  <br/> |
   

