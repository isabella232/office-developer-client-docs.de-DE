---
title: Row_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5e5c420e-f384-7b62-c862-35aea16e6d55
ms.openlocfilehash: 6ebd483ae9b0748a3afa15360bf2c88feae44aeb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586900"
---
# <a name="rowtype-complextype-visio-xml"></a><span data-ttu-id="4f400-102">Row_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="4f400-102">Row_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4f400-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="4f400-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f400-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4f400-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4f400-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="4f400-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4f400-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4f400-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4f400-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="4f400-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4f400-108">Keine</span><span class="sxs-lookup"><span data-stu-id="4f400-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4f400-109">Definition</span><span class="sxs-lookup"><span data-stu-id="4f400-109">Definition</span></span>

```XML
          <xs:complexType name="Row_Type">
          
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Trigger"  type="Trigger_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
    />
    <xs:attribute name="LocalName"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="T"
  type="xsd:string"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4f400-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="4f400-110">Elements and attributes</span></span>

<span data-ttu-id="4f400-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="4f400-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4f400-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f400-112">Child elements</span></span>

|<span data-ttu-id="4f400-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f400-113">**Element**</span></span>|<span data-ttu-id="4f400-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4f400-114">**Type**</span></span>|<span data-ttu-id="4f400-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f400-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4f400-116">Cell</span><span class="sxs-lookup"><span data-stu-id="4f400-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="4f400-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="4f400-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4f400-118">Trigger</span><span class="sxs-lookup"><span data-stu-id="4f400-118">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="4f400-119">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="4f400-119">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4f400-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="4f400-120">Attributes</span></span>

|<span data-ttu-id="4f400-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4f400-121">**Attribute**</span></span>|<span data-ttu-id="4f400-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4f400-122">**Type**</span></span>|<span data-ttu-id="4f400-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="4f400-123">**Required**</span></span>|<span data-ttu-id="4f400-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f400-124">**Description**</span></span>|<span data-ttu-id="4f400-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="4f400-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4f400-126">ENTF</span><span class="sxs-lookup"><span data-stu-id="4f400-126">Del</span></span>  <br/> |<span data-ttu-id="4f400-127">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="4f400-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4f400-128">Optional</span><span class="sxs-lookup"><span data-stu-id="4f400-128">optional</span></span>  <br/> ||<span data-ttu-id="4f400-129">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="4f400-129">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4f400-130">IX</span><span class="sxs-lookup"><span data-stu-id="4f400-130">IX</span></span>  <br/> |<span data-ttu-id="4f400-131">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4f400-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4f400-132">Optional</span><span class="sxs-lookup"><span data-stu-id="4f400-132">optional</span></span>  <br/> ||<span data-ttu-id="4f400-133">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4f400-133">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4f400-134">LocalName</span><span class="sxs-lookup"><span data-stu-id="4f400-134">LocalName</span></span>  <br/> |<span data-ttu-id="4f400-135">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4f400-135">xsd:string</span></span>  <br/> |<span data-ttu-id="4f400-136">Optional</span><span class="sxs-lookup"><span data-stu-id="4f400-136">optional</span></span>  <br/> ||<span data-ttu-id="4f400-137">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4f400-137">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4f400-138">N</span><span class="sxs-lookup"><span data-stu-id="4f400-138">N</span></span>  <br/> |<span data-ttu-id="4f400-139">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4f400-139">xsd:string</span></span>  <br/> |<span data-ttu-id="4f400-140">Optional</span><span class="sxs-lookup"><span data-stu-id="4f400-140">optional</span></span>  <br/> ||<span data-ttu-id="4f400-141">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4f400-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4f400-142">T</span><span class="sxs-lookup"><span data-stu-id="4f400-142">T</span></span>  <br/> |<span data-ttu-id="4f400-143">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4f400-143">xsd:string</span></span>  <br/> |<span data-ttu-id="4f400-144">Optional</span><span class="sxs-lookup"><span data-stu-id="4f400-144">optional</span></span>  <br/> ||<span data-ttu-id="4f400-145">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4f400-145">Values of the xsd:string type.</span></span>  <br/> |
   

