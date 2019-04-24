---
title: Section_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f8e855f-064c-d286-560f-9f89e7fce7b7
ms.openlocfilehash: 35cd638d36f4ddd1d90e0c312e65626f7d8b0bff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326096"
---
# <a name="sectiontype-complextype-visio-xml"></a><span data-ttu-id="2db88-102">Section_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="2db88-102">Section_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2db88-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="2db88-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2db88-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2db88-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2db88-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="2db88-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2db88-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="2db88-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2db88-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="2db88-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2db88-108">Keine</span><span class="sxs-lookup"><span data-stu-id="2db88-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2db88-109">Definition</span><span class="sxs-lookup"><span data-stu-id="2db88-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2db88-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="2db88-110">Elements and attributes</span></span>

<span data-ttu-id="2db88-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="2db88-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2db88-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2db88-112">Child elements</span></span>

|<span data-ttu-id="2db88-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2db88-113">**Element**</span></span>|<span data-ttu-id="2db88-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="2db88-114">**Type**</span></span>|<span data-ttu-id="2db88-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2db88-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2db88-116">Cell</span><span class="sxs-lookup"><span data-stu-id="2db88-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="2db88-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="2db88-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="2db88-118">Zeile</span><span class="sxs-lookup"><span data-stu-id="2db88-118">Row</span></span>](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[<span data-ttu-id="2db88-119">Row_Type</span><span class="sxs-lookup"><span data-stu-id="2db88-119">Row_Type</span></span>](row_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="2db88-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="2db88-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="2db88-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="2db88-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2db88-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="2db88-122">Attributes</span></span>

|<span data-ttu-id="2db88-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="2db88-123">**Attribute**</span></span>|<span data-ttu-id="2db88-124">**Typ**</span><span class="sxs-lookup"><span data-stu-id="2db88-124">**Type**</span></span>|<span data-ttu-id="2db88-125">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="2db88-125">**Required**</span></span>|<span data-ttu-id="2db88-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2db88-126">**Description**</span></span>|<span data-ttu-id="2db88-127">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="2db88-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2db88-128">ENTF</span><span class="sxs-lookup"><span data-stu-id="2db88-128">Del</span></span>  <br/> |<span data-ttu-id="2db88-129">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="2db88-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2db88-130">Optional</span><span class="sxs-lookup"><span data-stu-id="2db88-130">optional</span></span>  <br/> ||<span data-ttu-id="2db88-131">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="2db88-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2db88-132">IX</span><span class="sxs-lookup"><span data-stu-id="2db88-132">IX</span></span>  <br/> |<span data-ttu-id="2db88-133">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2db88-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2db88-134">Optional</span><span class="sxs-lookup"><span data-stu-id="2db88-134">optional</span></span>  <br/> ||<span data-ttu-id="2db88-135">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="2db88-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2db88-136">N</span><span class="sxs-lookup"><span data-stu-id="2db88-136">N</span></span>  <br/> |<span data-ttu-id="2db88-137">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2db88-137">xsd:string</span></span>  <br/> |<span data-ttu-id="2db88-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="2db88-138">required</span></span>  <br/> ||<span data-ttu-id="2db88-139">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="2db88-139">Values of the xsd:string type.</span></span>  <br/> |
   

