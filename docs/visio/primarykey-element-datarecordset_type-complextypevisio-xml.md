---
title: PrimaryKey-Element (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: Identifiziert eine oder mehrere Primärschlüsselspalten im Datendatensatz.
ms.openlocfilehash: bd77b1d18490695dc2b0cb43520f42bb845e91ab
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537710"
---
# <a name="primarykey-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="beeea-103">PrimaryKey-Element (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="beeea-103">PrimaryKey element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="beeea-104">Identifiziert eine oder mehrere Primärschlüsselspalten im Datendatensatz.</span><span class="sxs-lookup"><span data-stu-id="beeea-104">Identifies one or more primary-key columns in the data recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="beeea-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="beeea-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="beeea-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="beeea-106">**Element type**</span></span> <br/> |[<span data-ttu-id="beeea-107">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="beeea-107">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="beeea-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="beeea-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="beeea-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="beeea-109">**Schema file**</span></span> <br/> |<span data-ttu-id="beeea-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="beeea-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="beeea-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="beeea-111">**Document parts**</span></span> <br/> |<span data-ttu-id="beeea-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="beeea-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="beeea-113">Definition</span><span class="sxs-lookup"><span data-stu-id="beeea-113">Definition</span></span>

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="beeea-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="beeea-114">Elements and attributes</span></span>

<span data-ttu-id="beeea-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="beeea-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="beeea-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="beeea-116">Parent elements</span></span>

|<span data-ttu-id="beeea-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="beeea-117">**Element**</span></span>|<span data-ttu-id="beeea-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="beeea-118">**Type**</span></span>|<span data-ttu-id="beeea-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="beeea-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="beeea-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="beeea-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="beeea-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="beeea-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="beeea-122">Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.</span><span class="sxs-lookup"><span data-stu-id="beeea-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="beeea-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="beeea-123">Child elements</span></span>

|<span data-ttu-id="beeea-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="beeea-124">**Element**</span></span>|<span data-ttu-id="beeea-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="beeea-125">**Type**</span></span>|<span data-ttu-id="beeea-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="beeea-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="beeea-127">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="beeea-127">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="beeea-128">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="beeea-128">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="beeea-129">Gibt den Wert dieser Komponente des Primärschlüssels für eine einzelne Zeile eines Recordsets an.</span><span class="sxs-lookup"><span data-stu-id="beeea-129">Specifies the value of this component of the primary key for an individual row of a recordset.</span></span> <span data-ttu-id="beeea-130">Dieses untergeordnete Element muss mindestens ein Vorkommen haben.</span><span class="sxs-lookup"><span data-stu-id="beeea-130">There MUST be at least one occurrence of this child element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="beeea-131">Attribute</span><span class="sxs-lookup"><span data-stu-id="beeea-131">Attributes</span></span>

|<span data-ttu-id="beeea-132">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="beeea-132">**Attribute**</span></span>|<span data-ttu-id="beeea-133">**Typ**</span><span class="sxs-lookup"><span data-stu-id="beeea-133">**Type**</span></span>|<span data-ttu-id="beeea-134">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="beeea-134">**Required**</span></span>|<span data-ttu-id="beeea-135">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="beeea-135">**Description**</span></span>|<span data-ttu-id="beeea-136">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="beeea-136">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="beeea-137">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="beeea-137">ColumnNameID</span></span>  <br/> |<span data-ttu-id="beeea-138">xsd:string</span><span class="sxs-lookup"><span data-stu-id="beeea-138">xsd:string</span></span>  <br/> |<span data-ttu-id="beeea-139">Optional</span><span class="sxs-lookup"><span data-stu-id="beeea-139">optional</span></span>  <br/> |<span data-ttu-id="beeea-140">Gibt den Namen eines Felds an, das eine Komponente des Primärschlüssels ist.</span><span class="sxs-lookup"><span data-stu-id="beeea-140">Specifies the name of a field that is a component of the primary key.</span></span> <span data-ttu-id="beeea-141">Es muss sich um den Wert des **ColumnNameID-Attributs** eines DataColumn_Type untergeordneten Elements des DataRecordSet_Type, dessen Primärschlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="beeea-141">It MUST be the value of the **ColumnNameID** attribute of a DataColumn_Type descendant element of the DataRecordSet_Type whose primary key is being specified.</span></span>  <br/> |<span data-ttu-id="beeea-142">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="beeea-142">Values of the xsd:string type.</span></span>  <br/> |
   

