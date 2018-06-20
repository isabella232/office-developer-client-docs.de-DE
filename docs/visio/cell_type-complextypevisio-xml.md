---
title: Cell_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: b17a251844a00ce01ad572dc63d971329214a23f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796603"
---
# <a name="celltype-complextype-visio-xml"></a><span data-ttu-id="0055a-102">Cell_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="0055a-102">Cell_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0055a-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="0055a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0055a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0055a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0055a-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="0055a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0055a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0055a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0055a-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="0055a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0055a-108">Keine</span><span class="sxs-lookup"><span data-stu-id="0055a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0055a-109">Definition</span><span class="sxs-lookup"><span data-stu-id="0055a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0055a-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="0055a-110">Elements and attributes</span></span>

<span data-ttu-id="0055a-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="0055a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0055a-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0055a-112">Child elements</span></span>

|<span data-ttu-id="0055a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0055a-113">**Element**</span></span>|<span data-ttu-id="0055a-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0055a-114">**Type**</span></span>|<span data-ttu-id="0055a-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0055a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0055a-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="0055a-116">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0055a-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="0055a-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0055a-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="0055a-118">Attributes</span></span>

|<span data-ttu-id="0055a-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0055a-119">**Attribute**</span></span>|<span data-ttu-id="0055a-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0055a-120">**Type**</span></span>|<span data-ttu-id="0055a-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="0055a-121">**Required**</span></span>|<span data-ttu-id="0055a-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0055a-122">**Description**</span></span>|<span data-ttu-id="0055a-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="0055a-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0055a-124">E</span><span class="sxs-lookup"><span data-stu-id="0055a-124">E</span></span>  <br/> |<span data-ttu-id="0055a-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0055a-125">xsd:string</span></span>  <br/> |<span data-ttu-id="0055a-126">Optional</span><span class="sxs-lookup"><span data-stu-id="0055a-126">optional</span></span>  <br/> ||<span data-ttu-id="0055a-127">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0055a-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0055a-128">F</span><span class="sxs-lookup"><span data-stu-id="0055a-128">F</span></span>  <br/> |<span data-ttu-id="0055a-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0055a-129">xsd:string</span></span>  <br/> |<span data-ttu-id="0055a-130">Optional</span><span class="sxs-lookup"><span data-stu-id="0055a-130">optional</span></span>  <br/> ||<span data-ttu-id="0055a-131">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0055a-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0055a-132">N</span><span class="sxs-lookup"><span data-stu-id="0055a-132">N</span></span>  <br/> |<span data-ttu-id="0055a-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0055a-133">xsd:string</span></span>  <br/> |<span data-ttu-id="0055a-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0055a-134">required</span></span>  <br/> ||<span data-ttu-id="0055a-135">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0055a-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0055a-136">U</span><span class="sxs-lookup"><span data-stu-id="0055a-136">U</span></span>  <br/> |<span data-ttu-id="0055a-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0055a-137">xsd:string</span></span>  <br/> |<span data-ttu-id="0055a-138">Optional</span><span class="sxs-lookup"><span data-stu-id="0055a-138">optional</span></span>  <br/> ||<span data-ttu-id="0055a-139">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0055a-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0055a-140">V</span><span class="sxs-lookup"><span data-stu-id="0055a-140">V</span></span>  <br/> |<span data-ttu-id="0055a-141">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0055a-141">xsd:string</span></span>  <br/> |<span data-ttu-id="0055a-142">Optional</span><span class="sxs-lookup"><span data-stu-id="0055a-142">optional</span></span>  <br/> ||<span data-ttu-id="0055a-143">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0055a-143">Values of the xsd:string type.</span></span>  <br/> |
   

