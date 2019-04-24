---
title: DataRecordSet_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59544910-6bd5-2c89-71b3-5c8ee91a1dea
ms.openlocfilehash: 36d6cf3b34ad0aa81f7b097d6452c46679342a02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360361"
---
# <a name="datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="efe53-102">DataRecordSet_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="efe53-102">DataRecordSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="efe53-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="efe53-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="efe53-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="efe53-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="efe53-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="efe53-105">**Schema file**</span></span> <br/> |<span data-ttu-id="efe53-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="efe53-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="efe53-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="efe53-107">**Extension base**</span></span> <br/> |<span data-ttu-id="efe53-108">Keine</span><span class="sxs-lookup"><span data-stu-id="efe53-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="efe53-109">Definition</span><span class="sxs-lookup"><span data-stu-id="efe53-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="efe53-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="efe53-110">Elements and attributes</span></span>

<span data-ttu-id="efe53-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="efe53-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="efe53-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="efe53-112">Child elements</span></span>

|<span data-ttu-id="efe53-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="efe53-113">**Element**</span></span>|<span data-ttu-id="efe53-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="efe53-114">**Type**</span></span>|<span data-ttu-id="efe53-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="efe53-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="efe53-116">AutoLinkComparison</span><span class="sxs-lookup"><span data-stu-id="efe53-116">AutoLinkComparison</span></span>](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="efe53-117">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="efe53-117">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="efe53-118">DataColumns</span><span class="sxs-lookup"><span data-stu-id="efe53-118">DataColumns</span></span>](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="efe53-119">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="efe53-119">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="efe53-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="efe53-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="efe53-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="efe53-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="efe53-122">RefreshConflict</span><span class="sxs-lookup"><span data-stu-id="efe53-122">RefreshConflict</span></span>](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="efe53-123">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="efe53-123">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="efe53-124">Rel</span><span class="sxs-lookup"><span data-stu-id="efe53-124">Rel</span></span>](rel-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="efe53-125">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="efe53-125">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="efe53-126">RowMap</span><span class="sxs-lookup"><span data-stu-id="efe53-126">RowMap</span></span>](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="efe53-127">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="efe53-127">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="efe53-128">Attribute</span><span class="sxs-lookup"><span data-stu-id="efe53-128">Attributes</span></span>

|<span data-ttu-id="efe53-129">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="efe53-129">**Attribute**</span></span>|<span data-ttu-id="efe53-130">**Typ**</span><span class="sxs-lookup"><span data-stu-id="efe53-130">**Type**</span></span>|<span data-ttu-id="efe53-131">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="efe53-131">**Required**</span></span>|<span data-ttu-id="efe53-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="efe53-132">**Description**</span></span>|<span data-ttu-id="efe53-133">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="efe53-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="efe53-134">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="efe53-134">Checksum</span></span>  <br/> |<span data-ttu-id="efe53-135">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="efe53-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="efe53-136">Optional</span><span class="sxs-lookup"><span data-stu-id="efe53-136">optional</span></span>  <br/> ||<span data-ttu-id="efe53-137">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="efe53-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="efe53-138">Befehl</span><span class="sxs-lookup"><span data-stu-id="efe53-138">Command</span></span>  <br/> |<span data-ttu-id="efe53-139">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="efe53-139">xsd:string</span></span>  <br/> |<span data-ttu-id="efe53-140">Optional</span><span class="sxs-lookup"><span data-stu-id="efe53-140">optional</span></span>  <br/> ||<span data-ttu-id="efe53-141">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="efe53-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="efe53-142">ConnectionID</span><span class="sxs-lookup"><span data-stu-id="efe53-142">ConnectionID</span></span>  <br/> |<span data-ttu-id="efe53-143">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="efe53-143">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="efe53-144">Optional</span><span class="sxs-lookup"><span data-stu-id="efe53-144">optional</span></span>  <br/> ||<span data-ttu-id="efe53-145">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="efe53-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="efe53-146">ID</span><span class="sxs-lookup"><span data-stu-id="efe53-146">ID</span></span>  <br/> |<span data-ttu-id="efe53-147">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="efe53-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="efe53-148">erforderlich</span><span class="sxs-lookup"><span data-stu-id="efe53-148">required</span></span>  <br/> ||<span data-ttu-id="efe53-149">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="efe53-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="efe53-150">Name</span><span class="sxs-lookup"><span data-stu-id="efe53-150">Name</span></span>  <br/> |<span data-ttu-id="efe53-151">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="efe53-151">xsd:string</span></span>  <br/> |<span data-ttu-id="efe53-152">Optional</span><span class="sxs-lookup"><span data-stu-id="efe53-152">optional</span></span>  <br/> ||<span data-ttu-id="efe53-153">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="efe53-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="efe53-154">NextRowID</span><span class="sxs-lookup"><span data-stu-id="efe53-154">NextRowID</span></span>  <br/> |<span data-ttu-id="efe53-155">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="efe53-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="efe53-156">Optional</span><span class="sxs-lookup"><span data-stu-id="efe53-156">optional</span></span>  <br/> ||<span data-ttu-id="efe53-157">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="efe53-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="efe53-158">Optionen</span><span class="sxs-lookup"><span data-stu-id="efe53-158">Options</span></span>  <br/> |<span data-ttu-id="efe53-159">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="efe53-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="efe53-160">Optional</span><span class="sxs-lookup"><span data-stu-id="efe53-160">optional</span></span>  <br/> ||<span data-ttu-id="efe53-161">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="efe53-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="efe53-162">RefreshInterval</span><span class="sxs-lookup"><span data-stu-id="efe53-162">RefreshInterval</span></span>  <br/> |<span data-ttu-id="efe53-163">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="efe53-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="efe53-164">Optional</span><span class="sxs-lookup"><span data-stu-id="efe53-164">optional</span></span>  <br/> ||<span data-ttu-id="efe53-165">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="efe53-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="efe53-166">RefreshNoReconciliationUI</span><span class="sxs-lookup"><span data-stu-id="efe53-166">RefreshNoReconciliationUI</span></span>  <br/> |<span data-ttu-id="efe53-167">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="efe53-167">xsd:boolean</span></span>  <br/> |<span data-ttu-id="efe53-168">Optional</span><span class="sxs-lookup"><span data-stu-id="efe53-168">optional</span></span>  <br/> ||<span data-ttu-id="efe53-169">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="efe53-169">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="efe53-170">RefreshOverwriteAll</span><span class="sxs-lookup"><span data-stu-id="efe53-170">RefreshOverwriteAll</span></span>  <br/> |<span data-ttu-id="efe53-171">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="efe53-171">xsd:boolean</span></span>  <br/> |<span data-ttu-id="efe53-172">Optional</span><span class="sxs-lookup"><span data-stu-id="efe53-172">optional</span></span>  <br/> ||<span data-ttu-id="efe53-173">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="efe53-173">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="efe53-174">ReplaceLinks</span><span class="sxs-lookup"><span data-stu-id="efe53-174">ReplaceLinks</span></span>  <br/> |<span data-ttu-id="efe53-175">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="efe53-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="efe53-176">Optional</span><span class="sxs-lookup"><span data-stu-id="efe53-176">optional</span></span>  <br/> ||<span data-ttu-id="efe53-177">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="efe53-177">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="efe53-178">RowOrder</span><span class="sxs-lookup"><span data-stu-id="efe53-178">RowOrder</span></span>  <br/> |<span data-ttu-id="efe53-179">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="efe53-179">xsd:boolean</span></span>  <br/> |<span data-ttu-id="efe53-180">Optional</span><span class="sxs-lookup"><span data-stu-id="efe53-180">optional</span></span>  <br/> ||<span data-ttu-id="efe53-181">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="efe53-181">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="efe53-182">TimeRefreshed</span><span class="sxs-lookup"><span data-stu-id="efe53-182">TimeRefreshed</span></span>  <br/> |<span data-ttu-id="efe53-183">XSD: dateTime</span><span class="sxs-lookup"><span data-stu-id="efe53-183">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="efe53-184">Optional</span><span class="sxs-lookup"><span data-stu-id="efe53-184">optional</span></span>  <br/> ||<span data-ttu-id="efe53-185">Werte des XSD: dateTime-Typs.</span><span class="sxs-lookup"><span data-stu-id="efe53-185">Values of the xsd:dateTime type.</span></span>  <br/> |
   

