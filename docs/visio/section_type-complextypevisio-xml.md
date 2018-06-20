---
title: Section_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f8e855f-064c-d286-560f-9f89e7fce7b7
ms.openlocfilehash: 8eb9362f84849ad22a20662b327ae33cd795cc5a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797979"
---
# <a name="sectiontype-complextype-visio-xml"></a><span data-ttu-id="ef4b0-102">Section_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="ef4b0-102">Section_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ef4b0-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="ef4b0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef4b0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ef4b0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ef4b0-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ef4b0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ef4b0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ef4b0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ef4b0-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="ef4b0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ef4b0-108">Keine</span><span class="sxs-lookup"><span data-stu-id="ef4b0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ef4b0-109">Definition</span><span class="sxs-lookup"><span data-stu-id="ef4b0-109">Definition</span></span>

```XML
          <xs:complexType name="Section_Type">
          
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
    
    <xs:element name="Row"  type="Row_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ef4b0-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ef4b0-110">Elements and attributes</span></span>

<span data-ttu-id="ef4b0-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="ef4b0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ef4b0-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef4b0-112">Child elements</span></span>

|<span data-ttu-id="ef4b0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ef4b0-113">**Element**</span></span>|<span data-ttu-id="ef4b0-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ef4b0-114">**Type**</span></span>|<span data-ttu-id="ef4b0-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef4b0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ef4b0-116">Cell</span><span class="sxs-lookup"><span data-stu-id="ef4b0-116">Cell</span></span>](http://msdn.microsoft.com/library/70a9d6d6-a4ff-2b0d-febc-789a04a2f5b0%28Office.15%29.aspx) <br/> |[<span data-ttu-id="ef4b0-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="ef4b0-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ef4b0-118">Row</span><span class="sxs-lookup"><span data-stu-id="ef4b0-118">Row</span></span>](http://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[<span data-ttu-id="ef4b0-119">Row_Type</span><span class="sxs-lookup"><span data-stu-id="ef4b0-119">Row_Type</span></span>](row_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ef4b0-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="ef4b0-120">Trigger</span></span>](http://msdn.microsoft.com/library/e4eeb238-f6d0-fb23-db1c-01d55b0a8d88%28Office.15%29.aspx) <br/> |[<span data-ttu-id="ef4b0-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="ef4b0-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ef4b0-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="ef4b0-122">Attributes</span></span>

|<span data-ttu-id="ef4b0-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ef4b0-123">**Attribute**</span></span>|<span data-ttu-id="ef4b0-124">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ef4b0-124">**Type**</span></span>|<span data-ttu-id="ef4b0-125">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ef4b0-125">**Required**</span></span>|<span data-ttu-id="ef4b0-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef4b0-126">**Description**</span></span>|<span data-ttu-id="ef4b0-127">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="ef4b0-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ef4b0-128">ENTF</span><span class="sxs-lookup"><span data-stu-id="ef4b0-128">Del</span></span>  <br/> |<span data-ttu-id="ef4b0-129">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="ef4b0-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ef4b0-130">Optional</span><span class="sxs-lookup"><span data-stu-id="ef4b0-130">optional</span></span>  <br/> ||<span data-ttu-id="ef4b0-131">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="ef4b0-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ef4b0-132">IX</span><span class="sxs-lookup"><span data-stu-id="ef4b0-132">IX</span></span>  <br/> |<span data-ttu-id="ef4b0-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ef4b0-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ef4b0-134">Optional</span><span class="sxs-lookup"><span data-stu-id="ef4b0-134">optional</span></span>  <br/> ||<span data-ttu-id="ef4b0-135">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ef4b0-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ef4b0-136">N</span><span class="sxs-lookup"><span data-stu-id="ef4b0-136">N</span></span>  <br/> |<span data-ttu-id="ef4b0-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ef4b0-137">xsd:string</span></span>  <br/> |<span data-ttu-id="ef4b0-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="ef4b0-138">required</span></span>  <br/> ||<span data-ttu-id="ef4b0-139">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ef4b0-139">Values of the xsd:string type.</span></span>  <br/> |
   

