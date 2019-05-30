---
title: DataRecordSet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59544910-6bd5-2c89-71b3-5c8ee91a1dea
ms.openlocfilehash: 132261ae823d1749676b7bdc28cdd1cb94f6ef5b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539144"
---
# <a name="datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="0c1f0-102">DataRecordSet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="0c1f0-102">DataRecordSet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="0c1f0-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="0c1f0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c1f0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0c1f0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0c1f0-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="0c1f0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0c1f0-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="0c1f0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0c1f0-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="0c1f0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0c1f0-108">Keine</span><span class="sxs-lookup"><span data-stu-id="0c1f0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0c1f0-109">Definition</span><span class="sxs-lookup"><span data-stu-id="0c1f0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0c1f0-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="0c1f0-110">Elements and attributes</span></span>

<span data-ttu-id="0c1f0-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0c1f0-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c1f0-112">Child elements</span></span>

|<span data-ttu-id="0c1f0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0c1f0-113">**Element**</span></span>|<span data-ttu-id="0c1f0-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0c1f0-114">**Type**</span></span>|<span data-ttu-id="0c1f0-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0c1f0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0c1f0-116">AutoLinkComparison</span><span class="sxs-lookup"><span data-stu-id="0c1f0-116">AutoLinkComparison</span></span>](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0c1f0-117">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="0c1f0-117">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0c1f0-118">DataColumns</span><span class="sxs-lookup"><span data-stu-id="0c1f0-118">DataColumns</span></span>](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0c1f0-119">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="0c1f0-119">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0c1f0-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="0c1f0-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0c1f0-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="0c1f0-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0c1f0-122">RefreshConflict</span><span class="sxs-lookup"><span data-stu-id="0c1f0-122">RefreshConflict</span></span>](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0c1f0-123">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="0c1f0-123">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0c1f0-124">Rel</span><span class="sxs-lookup"><span data-stu-id="0c1f0-124">Rel</span></span>](rel-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0c1f0-125">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="0c1f0-125">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0c1f0-126">RowMap</span><span class="sxs-lookup"><span data-stu-id="0c1f0-126">RowMap</span></span>](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0c1f0-127">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="0c1f0-127">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0c1f0-128">Attribute</span><span class="sxs-lookup"><span data-stu-id="0c1f0-128">Attributes</span></span>

|<span data-ttu-id="0c1f0-129">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0c1f0-129">**Attribute**</span></span>|<span data-ttu-id="0c1f0-130">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0c1f0-130">**Type**</span></span>|<span data-ttu-id="0c1f0-131">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="0c1f0-131">**Required**</span></span>|<span data-ttu-id="0c1f0-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0c1f0-132">**Description**</span></span>|<span data-ttu-id="0c1f0-133">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="0c1f0-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0c1f0-134">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0c1f0-134">Checksum</span></span>  <br/> |<span data-ttu-id="0c1f0-135">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0c1f0-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0c1f0-136">Optional</span><span class="sxs-lookup"><span data-stu-id="0c1f0-136">optional</span></span>  <br/> ||<span data-ttu-id="0c1f0-137">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0c1f0-138">Befehl</span><span class="sxs-lookup"><span data-stu-id="0c1f0-138">Command</span></span>  <br/> |<span data-ttu-id="0c1f0-139">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0c1f0-139">xsd:string</span></span>  <br/> |<span data-ttu-id="0c1f0-140">Optional</span><span class="sxs-lookup"><span data-stu-id="0c1f0-140">optional</span></span>  <br/> ||<span data-ttu-id="0c1f0-141">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0c1f0-142">ConnectionID</span><span class="sxs-lookup"><span data-stu-id="0c1f0-142">ConnectionID</span></span>  <br/> |<span data-ttu-id="0c1f0-143">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0c1f0-143">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0c1f0-144">Optional</span><span class="sxs-lookup"><span data-stu-id="0c1f0-144">optional</span></span>  <br/> ||<span data-ttu-id="0c1f0-145">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0c1f0-146">ID</span><span class="sxs-lookup"><span data-stu-id="0c1f0-146">ID</span></span>  <br/> |<span data-ttu-id="0c1f0-147">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0c1f0-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0c1f0-148">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0c1f0-148">required</span></span>  <br/> ||<span data-ttu-id="0c1f0-149">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0c1f0-150">Name</span><span class="sxs-lookup"><span data-stu-id="0c1f0-150">Name</span></span>  <br/> |<span data-ttu-id="0c1f0-151">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0c1f0-151">xsd:string</span></span>  <br/> |<span data-ttu-id="0c1f0-152">Optional</span><span class="sxs-lookup"><span data-stu-id="0c1f0-152">optional</span></span>  <br/> ||<span data-ttu-id="0c1f0-153">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0c1f0-154">NextRowID</span><span class="sxs-lookup"><span data-stu-id="0c1f0-154">NextRowID</span></span>  <br/> |<span data-ttu-id="0c1f0-155">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0c1f0-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0c1f0-156">Optional</span><span class="sxs-lookup"><span data-stu-id="0c1f0-156">optional</span></span>  <br/> ||<span data-ttu-id="0c1f0-157">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0c1f0-158">Optionen</span><span class="sxs-lookup"><span data-stu-id="0c1f0-158">Options</span></span>  <br/> |<span data-ttu-id="0c1f0-159">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0c1f0-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0c1f0-160">Optional</span><span class="sxs-lookup"><span data-stu-id="0c1f0-160">optional</span></span>  <br/> ||<span data-ttu-id="0c1f0-161">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0c1f0-162">RefreshInterval</span><span class="sxs-lookup"><span data-stu-id="0c1f0-162">RefreshInterval</span></span>  <br/> |<span data-ttu-id="0c1f0-163">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0c1f0-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0c1f0-164">Optional</span><span class="sxs-lookup"><span data-stu-id="0c1f0-164">optional</span></span>  <br/> ||<span data-ttu-id="0c1f0-165">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0c1f0-166">RefreshNoReconciliationUI</span><span class="sxs-lookup"><span data-stu-id="0c1f0-166">RefreshNoReconciliationUI</span></span>  <br/> |<span data-ttu-id="0c1f0-167">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="0c1f0-167">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0c1f0-168">Optional</span><span class="sxs-lookup"><span data-stu-id="0c1f0-168">optional</span></span>  <br/> ||<span data-ttu-id="0c1f0-169">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-169">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0c1f0-170">RefreshOverwriteAll</span><span class="sxs-lookup"><span data-stu-id="0c1f0-170">RefreshOverwriteAll</span></span>  <br/> |<span data-ttu-id="0c1f0-171">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="0c1f0-171">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0c1f0-172">Optional</span><span class="sxs-lookup"><span data-stu-id="0c1f0-172">optional</span></span>  <br/> ||<span data-ttu-id="0c1f0-173">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-173">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0c1f0-174">ReplaceLinks</span><span class="sxs-lookup"><span data-stu-id="0c1f0-174">ReplaceLinks</span></span>  <br/> |<span data-ttu-id="0c1f0-175">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0c1f0-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0c1f0-176">Optional</span><span class="sxs-lookup"><span data-stu-id="0c1f0-176">optional</span></span>  <br/> ||<span data-ttu-id="0c1f0-177">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-177">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0c1f0-178">RowOrder</span><span class="sxs-lookup"><span data-stu-id="0c1f0-178">RowOrder</span></span>  <br/> |<span data-ttu-id="0c1f0-179">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="0c1f0-179">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0c1f0-180">Optional</span><span class="sxs-lookup"><span data-stu-id="0c1f0-180">optional</span></span>  <br/> ||<span data-ttu-id="0c1f0-181">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-181">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0c1f0-182">TimeRefreshed</span><span class="sxs-lookup"><span data-stu-id="0c1f0-182">TimeRefreshed</span></span>  <br/> |<span data-ttu-id="0c1f0-183">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="0c1f0-183">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="0c1f0-184">Optional</span><span class="sxs-lookup"><span data-stu-id="0c1f0-184">optional</span></span>  <br/> ||<span data-ttu-id="0c1f0-185">Werte des Typs XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="0c1f0-185">Values of the xsd:dateTime type.</span></span>  <br/> |
   

