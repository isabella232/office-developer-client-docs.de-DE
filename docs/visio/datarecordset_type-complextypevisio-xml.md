---
title: DataRecordSet_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59544910-6bd5-2c89-71b3-5c8ee91a1dea
ms.openlocfilehash: 79fe048c578e8b9d8095d3fe7cd456af8ce08549
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796796"
---
# <a name="datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="61df4-102">DataRecordSet_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="61df4-102">DataRecordSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="61df4-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="61df4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61df4-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="61df4-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="61df4-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="61df4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="61df4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="61df4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="61df4-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="61df4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="61df4-108">Keine</span><span class="sxs-lookup"><span data-stu-id="61df4-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="61df4-109">Definition</span><span class="sxs-lookup"><span data-stu-id="61df4-109">Definition</span></span>

```XML
          <xs:complexType name="DataRecordSet_Type">
          
          <xs:sequence>
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="DataColumns"  type="DataColumns_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="PrimaryKey"  type="PrimaryKey_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RowMap"  type="RowMap_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RefreshConflict"  type="RefreshConflict_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="AutoLinkComparison"  type="AutoLinkComparison_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ConnectionID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Command"
  type="xsd:string"
    />
    <xs:attribute name="Options"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="TimeRefreshed"
  type="xsd:dateTime"
    />
    <xs:attribute name="NextRowID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="RowOrder"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshOverwriteAll"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshNoReconciliationUI"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshInterval"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ReplaceLinks"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Checksum"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="61df4-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="61df4-110">Elements and attributes</span></span>

<span data-ttu-id="61df4-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="61df4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="61df4-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="61df4-112">Child elements</span></span>

|<span data-ttu-id="61df4-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="61df4-113">**Element**</span></span>|<span data-ttu-id="61df4-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="61df4-114">**Type**</span></span>|<span data-ttu-id="61df4-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="61df4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="61df4-116">AutoLinkComparison</span><span class="sxs-lookup"><span data-stu-id="61df4-116">AutoLinkComparison</span></span>](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="61df4-117">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="61df4-117">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="61df4-118">DataColumns</span><span class="sxs-lookup"><span data-stu-id="61df4-118">DataColumns</span></span>](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="61df4-119">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="61df4-119">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="61df4-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="61df4-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="61df4-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="61df4-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="61df4-122">RefreshConflict</span><span class="sxs-lookup"><span data-stu-id="61df4-122">RefreshConflict</span></span>](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="61df4-123">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="61df4-123">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="61df4-124">Rel</span><span class="sxs-lookup"><span data-stu-id="61df4-124">Rel</span></span>](rel-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="61df4-125">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="61df4-125">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="61df4-126">RowMap</span><span class="sxs-lookup"><span data-stu-id="61df4-126">RowMap</span></span>](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="61df4-127">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="61df4-127">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="61df4-128">Attribute</span><span class="sxs-lookup"><span data-stu-id="61df4-128">Attributes</span></span>

|<span data-ttu-id="61df4-129">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="61df4-129">**Attribute**</span></span>|<span data-ttu-id="61df4-130">**Typ**</span><span class="sxs-lookup"><span data-stu-id="61df4-130">**Type**</span></span>|<span data-ttu-id="61df4-131">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="61df4-131">**Required**</span></span>|<span data-ttu-id="61df4-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="61df4-132">**Description**</span></span>|<span data-ttu-id="61df4-133">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="61df4-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="61df4-134">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="61df4-134">Checksum</span></span>  <br/> |<span data-ttu-id="61df4-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="61df4-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="61df4-136">Optional</span><span class="sxs-lookup"><span data-stu-id="61df4-136">optional</span></span>  <br/> ||<span data-ttu-id="61df4-137">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="61df4-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="61df4-138">Befehl</span><span class="sxs-lookup"><span data-stu-id="61df4-138">Command</span></span>  <br/> |<span data-ttu-id="61df4-139">XSD: String</span><span class="sxs-lookup"><span data-stu-id="61df4-139">xsd:string</span></span>  <br/> |<span data-ttu-id="61df4-140">Optional</span><span class="sxs-lookup"><span data-stu-id="61df4-140">optional</span></span>  <br/> ||<span data-ttu-id="61df4-141">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="61df4-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="61df4-142">ConnectionID</span><span class="sxs-lookup"><span data-stu-id="61df4-142">ConnectionID</span></span>  <br/> |<span data-ttu-id="61df4-143">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="61df4-143">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="61df4-144">Optional</span><span class="sxs-lookup"><span data-stu-id="61df4-144">optional</span></span>  <br/> ||<span data-ttu-id="61df4-145">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="61df4-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="61df4-146">ID</span><span class="sxs-lookup"><span data-stu-id="61df4-146">ID</span></span>  <br/> |<span data-ttu-id="61df4-147">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="61df4-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="61df4-148">erforderlich</span><span class="sxs-lookup"><span data-stu-id="61df4-148">required</span></span>  <br/> ||<span data-ttu-id="61df4-149">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="61df4-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="61df4-150">Name</span><span class="sxs-lookup"><span data-stu-id="61df4-150">Name</span></span>  <br/> |<span data-ttu-id="61df4-151">XSD: String</span><span class="sxs-lookup"><span data-stu-id="61df4-151">xsd:string</span></span>  <br/> |<span data-ttu-id="61df4-152">Optional</span><span class="sxs-lookup"><span data-stu-id="61df4-152">optional</span></span>  <br/> ||<span data-ttu-id="61df4-153">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="61df4-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="61df4-154">NextRowID</span><span class="sxs-lookup"><span data-stu-id="61df4-154">NextRowID</span></span>  <br/> |<span data-ttu-id="61df4-155">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="61df4-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="61df4-156">Optional</span><span class="sxs-lookup"><span data-stu-id="61df4-156">optional</span></span>  <br/> ||<span data-ttu-id="61df4-157">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="61df4-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="61df4-158">Options</span><span class="sxs-lookup"><span data-stu-id="61df4-158">Options</span></span>  <br/> |<span data-ttu-id="61df4-159">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="61df4-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="61df4-160">Optional</span><span class="sxs-lookup"><span data-stu-id="61df4-160">optional</span></span>  <br/> ||<span data-ttu-id="61df4-161">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="61df4-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="61df4-162">RefreshInterval</span><span class="sxs-lookup"><span data-stu-id="61df4-162">RefreshInterval</span></span>  <br/> |<span data-ttu-id="61df4-163">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="61df4-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="61df4-164">Optional</span><span class="sxs-lookup"><span data-stu-id="61df4-164">optional</span></span>  <br/> ||<span data-ttu-id="61df4-165">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="61df4-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="61df4-166">RefreshNoReconciliationUI</span><span class="sxs-lookup"><span data-stu-id="61df4-166">RefreshNoReconciliationUI</span></span>  <br/> |<span data-ttu-id="61df4-167">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="61df4-167">xsd:boolean</span></span>  <br/> |<span data-ttu-id="61df4-168">Optional</span><span class="sxs-lookup"><span data-stu-id="61df4-168">optional</span></span>  <br/> ||<span data-ttu-id="61df4-169">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="61df4-169">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="61df4-170">RefreshOverwriteAll</span><span class="sxs-lookup"><span data-stu-id="61df4-170">RefreshOverwriteAll</span></span>  <br/> |<span data-ttu-id="61df4-171">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="61df4-171">xsd:boolean</span></span>  <br/> |<span data-ttu-id="61df4-172">Optional</span><span class="sxs-lookup"><span data-stu-id="61df4-172">optional</span></span>  <br/> ||<span data-ttu-id="61df4-173">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="61df4-173">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="61df4-174">ReplaceLinks</span><span class="sxs-lookup"><span data-stu-id="61df4-174">ReplaceLinks</span></span>  <br/> |<span data-ttu-id="61df4-175">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="61df4-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="61df4-176">Optional</span><span class="sxs-lookup"><span data-stu-id="61df4-176">optional</span></span>  <br/> ||<span data-ttu-id="61df4-177">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="61df4-177">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="61df4-178">RowOrder</span><span class="sxs-lookup"><span data-stu-id="61df4-178">RowOrder</span></span>  <br/> |<span data-ttu-id="61df4-179">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="61df4-179">xsd:boolean</span></span>  <br/> |<span data-ttu-id="61df4-180">Optional</span><span class="sxs-lookup"><span data-stu-id="61df4-180">optional</span></span>  <br/> ||<span data-ttu-id="61df4-181">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="61df4-181">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="61df4-182">TimeRefreshed</span><span class="sxs-lookup"><span data-stu-id="61df4-182">TimeRefreshed</span></span>  <br/> |<span data-ttu-id="61df4-183">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="61df4-183">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="61df4-184">Optional</span><span class="sxs-lookup"><span data-stu-id="61df4-184">optional</span></span>  <br/> ||<span data-ttu-id="61df4-185">Werte des Typs xsd: DateTime.</span><span class="sxs-lookup"><span data-stu-id="61df4-185">Values of the xsd:dateTime type.</span></span>  <br/> |
   

