---
title: PrimaryKey-Element (DataRecordSet_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: Eine oder mehrere Primärschlüsselspalten im Datenrecordset identifiziert.
ms.openlocfilehash: f720636bbdf2c55baca6d98aa7d0761607e53ffc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797742"
---
# <a name="primarykey-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="8eca4-103">PrimaryKey-Element (DataRecordSet_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="8eca4-103">PrimaryKey element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8eca4-104">Eine oder mehrere Primärschlüsselspalten im Datenrecordset identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8eca4-104">Identifies one or more primary-key columns in the data recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8eca4-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8eca4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8eca4-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="8eca4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8eca4-107">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="8eca4-107">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8eca4-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8eca4-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8eca4-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="8eca4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8eca4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8eca4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8eca4-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="8eca4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8eca4-112">Recordsets.Xml</span><span class="sxs-lookup"><span data-stu-id="8eca4-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8eca4-113">Definition</span><span class="sxs-lookup"><span data-stu-id="8eca4-113">Definition</span></span>

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8eca4-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="8eca4-114">Elements and attributes</span></span>

<span data-ttu-id="8eca4-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="8eca4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8eca4-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8eca4-116">Parent elements</span></span>

|<span data-ttu-id="8eca4-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="8eca4-117">**Element**</span></span>|<span data-ttu-id="8eca4-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="8eca4-118">**Type**</span></span>|<span data-ttu-id="8eca4-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8eca4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8eca4-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="8eca4-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8eca4-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="8eca4-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8eca4-122">Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.</span><span class="sxs-lookup"><span data-stu-id="8eca4-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8eca4-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8eca4-123">Child elements</span></span>

|<span data-ttu-id="8eca4-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="8eca4-124">**Element**</span></span>|<span data-ttu-id="8eca4-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="8eca4-125">**Type**</span></span>|<span data-ttu-id="8eca4-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8eca4-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8eca4-127">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="8eca4-127">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8eca4-128">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="8eca4-128">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8eca4-129">Gibt den Wert dieser Komponente der Primärschlüssel für eine einzelne Zeile eines Recordset-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8eca4-129">Specifies the value of this component of the primary key for an individual row of a recordset.</span></span> <span data-ttu-id="8eca4-130">Es muss mindestens ein Vorkommen des untergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="8eca4-130">There MUST be at least one occurrence of this child element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8eca4-131">Attribute</span><span class="sxs-lookup"><span data-stu-id="8eca4-131">Attributes</span></span>

|<span data-ttu-id="8eca4-132">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8eca4-132">**Attribute**</span></span>|<span data-ttu-id="8eca4-133">**Typ**</span><span class="sxs-lookup"><span data-stu-id="8eca4-133">**Type**</span></span>|<span data-ttu-id="8eca4-134">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="8eca4-134">**Required**</span></span>|<span data-ttu-id="8eca4-135">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8eca4-135">**Description**</span></span>|<span data-ttu-id="8eca4-136">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="8eca4-136">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8eca4-137">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="8eca4-137">ColumnNameID</span></span>  <br/> |<span data-ttu-id="8eca4-138">XSD: String</span><span class="sxs-lookup"><span data-stu-id="8eca4-138">xsd:string</span></span>  <br/> |<span data-ttu-id="8eca4-139">Optional</span><span class="sxs-lookup"><span data-stu-id="8eca4-139">optional</span></span>  <br/> |<span data-ttu-id="8eca4-140">Gibt den Namen eines Felds, das eine Komponente des Primärschlüssels ist.</span><span class="sxs-lookup"><span data-stu-id="8eca4-140">Specifies the name of a field that is a component of the primary key.</span></span> <span data-ttu-id="8eca4-141">Es muss der Wert des Attributs **ColumnNameID** aus einem DataColumn_Type untergeordnete Element des der DataRecordSet_Type, deren Primärschlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8eca4-141">It MUST be the value of the **ColumnNameID** attribute of a DataColumn_Type descendant element of the DataRecordSet_Type whose primary key is being specified.</span></span>  <br/> |<span data-ttu-id="8eca4-142">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="8eca4-142">Values of the xsd:string type.</span></span>  <br/> |
   

