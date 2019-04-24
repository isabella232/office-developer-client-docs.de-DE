---
title: Cell_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: ae5f481d787ae5d07968df8cd0ef0eba6af26f9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327118"
---
# <a name="celltype-complextype-visio-xml"></a><span data-ttu-id="e5765-102">Cell_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="e5765-102">Cell_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e5765-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="e5765-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5765-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e5765-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e5765-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="e5765-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e5765-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="e5765-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e5765-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="e5765-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e5765-108">Keine</span><span class="sxs-lookup"><span data-stu-id="e5765-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e5765-109">Definition</span><span class="sxs-lookup"><span data-stu-id="e5765-109">Definition</span></span>

```XML
          <xs:complexType name="Cell_Type">
          
          <xs:sequence>
    <xs:element name="RefBy"  type="RefBy_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="U"
  type="xsd:string"
    />
    <xs:attribute name="E"
  type="xsd:string"
    />
    <xs:attribute name="F"
  type="xsd:string"
    />
    <xs:attribute name="V"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e5765-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="e5765-110">Elements and attributes</span></span>

<span data-ttu-id="e5765-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="e5765-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e5765-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e5765-112">Child elements</span></span>

|<span data-ttu-id="e5765-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e5765-113">**Element**</span></span>|<span data-ttu-id="e5765-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="e5765-114">**Type**</span></span>|<span data-ttu-id="e5765-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e5765-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e5765-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="e5765-116">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e5765-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="e5765-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e5765-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="e5765-118">Attributes</span></span>

|<span data-ttu-id="e5765-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e5765-119">**Attribute**</span></span>|<span data-ttu-id="e5765-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="e5765-120">**Type**</span></span>|<span data-ttu-id="e5765-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="e5765-121">**Required**</span></span>|<span data-ttu-id="e5765-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e5765-122">**Description**</span></span>|<span data-ttu-id="e5765-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="e5765-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e5765-124">E</span><span class="sxs-lookup"><span data-stu-id="e5765-124">E</span></span>  <br/> |<span data-ttu-id="e5765-125">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e5765-125">xsd:string</span></span>  <br/> |<span data-ttu-id="e5765-126">Optional</span><span class="sxs-lookup"><span data-stu-id="e5765-126">optional</span></span>  <br/> ||<span data-ttu-id="e5765-127">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="e5765-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e5765-128">F</span><span class="sxs-lookup"><span data-stu-id="e5765-128">F</span></span>  <br/> |<span data-ttu-id="e5765-129">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e5765-129">xsd:string</span></span>  <br/> |<span data-ttu-id="e5765-130">Optional</span><span class="sxs-lookup"><span data-stu-id="e5765-130">optional</span></span>  <br/> ||<span data-ttu-id="e5765-131">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="e5765-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e5765-132">N</span><span class="sxs-lookup"><span data-stu-id="e5765-132">N</span></span>  <br/> |<span data-ttu-id="e5765-133">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e5765-133">xsd:string</span></span>  <br/> |<span data-ttu-id="e5765-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="e5765-134">required</span></span>  <br/> ||<span data-ttu-id="e5765-135">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="e5765-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e5765-136">U</span><span class="sxs-lookup"><span data-stu-id="e5765-136">U</span></span>  <br/> |<span data-ttu-id="e5765-137">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e5765-137">xsd:string</span></span>  <br/> |<span data-ttu-id="e5765-138">Optional</span><span class="sxs-lookup"><span data-stu-id="e5765-138">optional</span></span>  <br/> ||<span data-ttu-id="e5765-139">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="e5765-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e5765-140">V</span><span class="sxs-lookup"><span data-stu-id="e5765-140">V</span></span>  <br/> |<span data-ttu-id="e5765-141">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e5765-141">xsd:string</span></span>  <br/> |<span data-ttu-id="e5765-142">Optional</span><span class="sxs-lookup"><span data-stu-id="e5765-142">optional</span></span>  <br/> ||<span data-ttu-id="e5765-143">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="e5765-143">Values of the xsd:string type.</span></span>  <br/> |
   

