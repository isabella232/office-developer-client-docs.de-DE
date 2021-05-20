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
# <a name="datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="9ca86-102">DataRecordSet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9ca86-102">DataRecordSet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9ca86-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="9ca86-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9ca86-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9ca86-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9ca86-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="9ca86-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9ca86-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9ca86-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9ca86-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="9ca86-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9ca86-108">Keine</span><span class="sxs-lookup"><span data-stu-id="9ca86-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9ca86-109">Definition</span><span class="sxs-lookup"><span data-stu-id="9ca86-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="9ca86-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="9ca86-110">Elements and attributes</span></span>

<span data-ttu-id="9ca86-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="9ca86-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9ca86-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9ca86-112">Child elements</span></span>

|<span data-ttu-id="9ca86-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9ca86-113">**Element**</span></span>|<span data-ttu-id="9ca86-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9ca86-114">**Type**</span></span>|<span data-ttu-id="9ca86-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9ca86-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9ca86-116">AutoLinkComparison</span><span class="sxs-lookup"><span data-stu-id="9ca86-116">AutoLinkComparison</span></span>](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9ca86-117">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="9ca86-117">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9ca86-118">DataColumns</span><span class="sxs-lookup"><span data-stu-id="9ca86-118">DataColumns</span></span>](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9ca86-119">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="9ca86-119">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9ca86-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="9ca86-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9ca86-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="9ca86-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9ca86-122">RefreshConflict</span><span class="sxs-lookup"><span data-stu-id="9ca86-122">RefreshConflict</span></span>](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9ca86-123">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="9ca86-123">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9ca86-124">Rel</span><span class="sxs-lookup"><span data-stu-id="9ca86-124">Rel</span></span>](rel-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9ca86-125">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="9ca86-125">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9ca86-126">RowMap</span><span class="sxs-lookup"><span data-stu-id="9ca86-126">RowMap</span></span>](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9ca86-127">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="9ca86-127">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9ca86-128">Attribute</span><span class="sxs-lookup"><span data-stu-id="9ca86-128">Attributes</span></span>

|<span data-ttu-id="9ca86-129">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9ca86-129">**Attribute**</span></span>|<span data-ttu-id="9ca86-130">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9ca86-130">**Type**</span></span>|<span data-ttu-id="9ca86-131">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="9ca86-131">**Required**</span></span>|<span data-ttu-id="9ca86-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9ca86-132">**Description**</span></span>|<span data-ttu-id="9ca86-133">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="9ca86-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9ca86-134">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9ca86-134">Checksum</span></span>  <br/> |<span data-ttu-id="9ca86-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ca86-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ca86-136">Optional</span><span class="sxs-lookup"><span data-stu-id="9ca86-136">optional</span></span>  <br/> ||<span data-ttu-id="9ca86-137">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9ca86-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9ca86-138">Get-Help</span><span class="sxs-lookup"><span data-stu-id="9ca86-138">Command</span></span>  <br/> |<span data-ttu-id="9ca86-139">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9ca86-139">xsd:string</span></span>  <br/> |<span data-ttu-id="9ca86-140">Optional</span><span class="sxs-lookup"><span data-stu-id="9ca86-140">optional</span></span>  <br/> ||<span data-ttu-id="9ca86-141">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="9ca86-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9ca86-142">ConnectionID</span><span class="sxs-lookup"><span data-stu-id="9ca86-142">ConnectionID</span></span>  <br/> |<span data-ttu-id="9ca86-143">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ca86-143">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ca86-144">Optional</span><span class="sxs-lookup"><span data-stu-id="9ca86-144">optional</span></span>  <br/> ||<span data-ttu-id="9ca86-145">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9ca86-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9ca86-146">ID</span><span class="sxs-lookup"><span data-stu-id="9ca86-146">ID</span></span>  <br/> |<span data-ttu-id="9ca86-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ca86-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ca86-148">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9ca86-148">required</span></span>  <br/> ||<span data-ttu-id="9ca86-149">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9ca86-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9ca86-150">Name</span><span class="sxs-lookup"><span data-stu-id="9ca86-150">Name</span></span>  <br/> |<span data-ttu-id="9ca86-151">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9ca86-151">xsd:string</span></span>  <br/> |<span data-ttu-id="9ca86-152">Optional</span><span class="sxs-lookup"><span data-stu-id="9ca86-152">optional</span></span>  <br/> ||<span data-ttu-id="9ca86-153">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="9ca86-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9ca86-154">NextRowID</span><span class="sxs-lookup"><span data-stu-id="9ca86-154">NextRowID</span></span>  <br/> |<span data-ttu-id="9ca86-155">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ca86-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ca86-156">Optional</span><span class="sxs-lookup"><span data-stu-id="9ca86-156">optional</span></span>  <br/> ||<span data-ttu-id="9ca86-157">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9ca86-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9ca86-158">Optionen</span><span class="sxs-lookup"><span data-stu-id="9ca86-158">Options</span></span>  <br/> |<span data-ttu-id="9ca86-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ca86-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ca86-160">Optional</span><span class="sxs-lookup"><span data-stu-id="9ca86-160">optional</span></span>  <br/> ||<span data-ttu-id="9ca86-161">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9ca86-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9ca86-162">RefreshInterval</span><span class="sxs-lookup"><span data-stu-id="9ca86-162">RefreshInterval</span></span>  <br/> |<span data-ttu-id="9ca86-163">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ca86-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ca86-164">Optional</span><span class="sxs-lookup"><span data-stu-id="9ca86-164">optional</span></span>  <br/> ||<span data-ttu-id="9ca86-165">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9ca86-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9ca86-166">RefreshNoReconciliationUI</span><span class="sxs-lookup"><span data-stu-id="9ca86-166">RefreshNoReconciliationUI</span></span>  <br/> |<span data-ttu-id="9ca86-167">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9ca86-167">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9ca86-168">Optional</span><span class="sxs-lookup"><span data-stu-id="9ca86-168">optional</span></span>  <br/> ||<span data-ttu-id="9ca86-169">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9ca86-169">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9ca86-170">RefreshOverwriteAll</span><span class="sxs-lookup"><span data-stu-id="9ca86-170">RefreshOverwriteAll</span></span>  <br/> |<span data-ttu-id="9ca86-171">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9ca86-171">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9ca86-172">Optional</span><span class="sxs-lookup"><span data-stu-id="9ca86-172">optional</span></span>  <br/> ||<span data-ttu-id="9ca86-173">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9ca86-173">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9ca86-174">ReplaceLinks</span><span class="sxs-lookup"><span data-stu-id="9ca86-174">ReplaceLinks</span></span>  <br/> |<span data-ttu-id="9ca86-175">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ca86-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ca86-176">Optional</span><span class="sxs-lookup"><span data-stu-id="9ca86-176">optional</span></span>  <br/> ||<span data-ttu-id="9ca86-177">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9ca86-177">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9ca86-178">RowOrder</span><span class="sxs-lookup"><span data-stu-id="9ca86-178">RowOrder</span></span>  <br/> |<span data-ttu-id="9ca86-179">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9ca86-179">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9ca86-180">Optional</span><span class="sxs-lookup"><span data-stu-id="9ca86-180">optional</span></span>  <br/> ||<span data-ttu-id="9ca86-181">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9ca86-181">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9ca86-182">TimeRefreshed</span><span class="sxs-lookup"><span data-stu-id="9ca86-182">TimeRefreshed</span></span>  <br/> |<span data-ttu-id="9ca86-183">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="9ca86-183">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="9ca86-184">Optional</span><span class="sxs-lookup"><span data-stu-id="9ca86-184">optional</span></span>  <br/> ||<span data-ttu-id="9ca86-185">Werte des xsd:dateTime-Typs.</span><span class="sxs-lookup"><span data-stu-id="9ca86-185">Values of the xsd:dateTime type.</span></span>  <br/> |
   

