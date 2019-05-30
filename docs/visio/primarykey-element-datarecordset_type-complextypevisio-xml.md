---
title: Primary-Element (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: Gibt eine oder mehrere Primärschlüsselspalten im Datenrecordset an.
ms.openlocfilehash: bd77b1d18490695dc2b0cb43520f42bb845e91ab
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537710"
---
# <a name="primarykey-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="9f8ab-103">Primary-Element (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9f8ab-103">PrimaryKey element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="9f8ab-104">Gibt eine oder mehrere Primärschlüsselspalten im Datenrecordset an.</span><span class="sxs-lookup"><span data-stu-id="9f8ab-104">Identifies one or more primary-key columns in the data recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9f8ab-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9f8ab-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9f8ab-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="9f8ab-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9f8ab-107">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="9f8ab-107">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9f8ab-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9f8ab-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9f8ab-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="9f8ab-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9f8ab-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="9f8ab-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9f8ab-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="9f8ab-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9f8ab-112">Recordsets. XML</span><span class="sxs-lookup"><span data-stu-id="9f8ab-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9f8ab-113">Definition</span><span class="sxs-lookup"><span data-stu-id="9f8ab-113">Definition</span></span>

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9f8ab-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="9f8ab-114">Elements and attributes</span></span>

<span data-ttu-id="9f8ab-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="9f8ab-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9f8ab-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9f8ab-116">Parent elements</span></span>

|<span data-ttu-id="9f8ab-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="9f8ab-117">**Element**</span></span>|<span data-ttu-id="9f8ab-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9f8ab-118">**Type**</span></span>|<span data-ttu-id="9f8ab-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9f8ab-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9f8ab-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="9f8ab-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9f8ab-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="9f8ab-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9f8ab-122">Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.</span><span class="sxs-lookup"><span data-stu-id="9f8ab-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9f8ab-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9f8ab-123">Child elements</span></span>

|<span data-ttu-id="9f8ab-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="9f8ab-124">**Element**</span></span>|<span data-ttu-id="9f8ab-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9f8ab-125">**Type**</span></span>|<span data-ttu-id="9f8ab-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9f8ab-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9f8ab-127">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="9f8ab-127">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9f8ab-128">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="9f8ab-128">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9f8ab-129">Gibt den Wert dieser Komponente des Primärschlüssels für eine einzelne Zeile eines Recordset-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="9f8ab-129">Specifies the value of this component of the primary key for an individual row of a recordset.</span></span> <span data-ttu-id="9f8ab-130">Es muss mindestens ein Vorkommen dieses untergeordneten Elements vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="9f8ab-130">There MUST be at least one occurrence of this child element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9f8ab-131">Attribute</span><span class="sxs-lookup"><span data-stu-id="9f8ab-131">Attributes</span></span>

|<span data-ttu-id="9f8ab-132">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9f8ab-132">**Attribute**</span></span>|<span data-ttu-id="9f8ab-133">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9f8ab-133">**Type**</span></span>|<span data-ttu-id="9f8ab-134">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="9f8ab-134">**Required**</span></span>|<span data-ttu-id="9f8ab-135">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9f8ab-135">**Description**</span></span>|<span data-ttu-id="9f8ab-136">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="9f8ab-136">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9f8ab-137">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="9f8ab-137">ColumnNameID</span></span>  <br/> |<span data-ttu-id="9f8ab-138">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9f8ab-138">xsd:string</span></span>  <br/> |<span data-ttu-id="9f8ab-139">Optional</span><span class="sxs-lookup"><span data-stu-id="9f8ab-139">optional</span></span>  <br/> |<span data-ttu-id="9f8ab-140">Gibt den Namen eines Felds an, das eine Komponente des Primärschlüssels ist.</span><span class="sxs-lookup"><span data-stu-id="9f8ab-140">Specifies the name of a field that is a component of the primary key.</span></span> <span data-ttu-id="9f8ab-141">Es muss sich um den Wert des Attributs " **ColumnName** " eines DataColumn_Type-Nachfolger Elements des DataRecordSet_Type handeln, dessen Primärschlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9f8ab-141">It MUST be the value of the **ColumnNameID** attribute of a DataColumn_Type descendant element of the DataRecordSet_Type whose primary key is being specified.</span></span>  <br/> |<span data-ttu-id="9f8ab-142">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="9f8ab-142">Values of the xsd:string type.</span></span>  <br/> |
   

