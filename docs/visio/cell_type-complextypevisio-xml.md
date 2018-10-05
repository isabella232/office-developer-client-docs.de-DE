---
title: Cell_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: ae5f481d787ae5d07968df8cd0ef0eba6af26f9c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389463"
---
# <a name="celltype-complextype-visio-xml"></a><span data-ttu-id="88096-102">Cell_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="88096-102">Cell_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="88096-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="88096-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88096-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="88096-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="88096-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="88096-105">**Schema file**</span></span> <br/> |<span data-ttu-id="88096-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="88096-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="88096-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="88096-107">**Extension base**</span></span> <br/> |<span data-ttu-id="88096-108">Keine</span><span class="sxs-lookup"><span data-stu-id="88096-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="88096-109">Definition</span><span class="sxs-lookup"><span data-stu-id="88096-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="88096-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="88096-110">Elements and attributes</span></span>

<span data-ttu-id="88096-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="88096-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="88096-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="88096-112">Child elements</span></span>

|<span data-ttu-id="88096-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="88096-113">**Element**</span></span>|<span data-ttu-id="88096-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="88096-114">**Type**</span></span>|<span data-ttu-id="88096-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="88096-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="88096-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="88096-116">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="88096-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="88096-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="88096-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="88096-118">Attributes</span></span>

|<span data-ttu-id="88096-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="88096-119">**Attribute**</span></span>|<span data-ttu-id="88096-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="88096-120">**Type**</span></span>|<span data-ttu-id="88096-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="88096-121">**Required**</span></span>|<span data-ttu-id="88096-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="88096-122">**Description**</span></span>|<span data-ttu-id="88096-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="88096-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="88096-124">E</span><span class="sxs-lookup"><span data-stu-id="88096-124">E</span></span>  <br/> |<span data-ttu-id="88096-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="88096-125">xsd:string</span></span>  <br/> |<span data-ttu-id="88096-126">Optional</span><span class="sxs-lookup"><span data-stu-id="88096-126">optional</span></span>  <br/> ||<span data-ttu-id="88096-127">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="88096-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="88096-128">F</span><span class="sxs-lookup"><span data-stu-id="88096-128">F</span></span>  <br/> |<span data-ttu-id="88096-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="88096-129">xsd:string</span></span>  <br/> |<span data-ttu-id="88096-130">Optional</span><span class="sxs-lookup"><span data-stu-id="88096-130">optional</span></span>  <br/> ||<span data-ttu-id="88096-131">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="88096-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="88096-132">N</span><span class="sxs-lookup"><span data-stu-id="88096-132">N</span></span>  <br/> |<span data-ttu-id="88096-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="88096-133">xsd:string</span></span>  <br/> |<span data-ttu-id="88096-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="88096-134">required</span></span>  <br/> ||<span data-ttu-id="88096-135">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="88096-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="88096-136">U</span><span class="sxs-lookup"><span data-stu-id="88096-136">U</span></span>  <br/> |<span data-ttu-id="88096-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="88096-137">xsd:string</span></span>  <br/> |<span data-ttu-id="88096-138">Optional</span><span class="sxs-lookup"><span data-stu-id="88096-138">optional</span></span>  <br/> ||<span data-ttu-id="88096-139">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="88096-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="88096-140">V</span><span class="sxs-lookup"><span data-stu-id="88096-140">V</span></span>  <br/> |<span data-ttu-id="88096-141">XSD: String</span><span class="sxs-lookup"><span data-stu-id="88096-141">xsd:string</span></span>  <br/> |<span data-ttu-id="88096-142">Optional</span><span class="sxs-lookup"><span data-stu-id="88096-142">optional</span></span>  <br/> ||<span data-ttu-id="88096-143">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="88096-143">Values of the xsd:string type.</span></span>  <br/> |
   

