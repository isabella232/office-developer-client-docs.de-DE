---
title: DocumentSheet_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: a1f51ef6f0340b4430860eabde3ad778e923fed0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396344"
---
# <a name="documentsheettype-complextype-visio-xml"></a><span data-ttu-id="aad24-102">DocumentSheet_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="aad24-102">DocumentSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="aad24-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="aad24-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aad24-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="aad24-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="aad24-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="aad24-105">**Schema file**</span></span> <br/> |<span data-ttu-id="aad24-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="aad24-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="aad24-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="aad24-107">**Extension base**</span></span> <br/> |<span data-ttu-id="aad24-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="aad24-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="aad24-109">Definition</span><span class="sxs-lookup"><span data-stu-id="aad24-109">Definition</span></span>

```XML
      <xs:complexType name="DocumentSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="aad24-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="aad24-110">Elements and attributes</span></span>

<span data-ttu-id="aad24-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="aad24-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="aad24-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aad24-112">Child elements</span></span>

<span data-ttu-id="aad24-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="aad24-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aad24-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="aad24-114">Attributes</span></span>

|<span data-ttu-id="aad24-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="aad24-115">**Attribute**</span></span>|<span data-ttu-id="aad24-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="aad24-116">**Type**</span></span>|<span data-ttu-id="aad24-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="aad24-117">**Required**</span></span>|<span data-ttu-id="aad24-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aad24-118">**Description**</span></span>|<span data-ttu-id="aad24-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="aad24-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="aad24-120">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="aad24-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="aad24-121">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="aad24-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="aad24-122">Optional</span><span class="sxs-lookup"><span data-stu-id="aad24-122">optional</span></span>  <br/> ||<span data-ttu-id="aad24-123">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="aad24-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="aad24-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="aad24-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="aad24-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="aad24-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="aad24-126">Optional</span><span class="sxs-lookup"><span data-stu-id="aad24-126">optional</span></span>  <br/> ||<span data-ttu-id="aad24-127">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="aad24-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="aad24-128">Name</span><span class="sxs-lookup"><span data-stu-id="aad24-128">Name</span></span>  <br/> |<span data-ttu-id="aad24-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="aad24-129">xsd:string</span></span>  <br/> |<span data-ttu-id="aad24-130">Optional</span><span class="sxs-lookup"><span data-stu-id="aad24-130">optional</span></span>  <br/> ||<span data-ttu-id="aad24-131">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="aad24-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="aad24-132">NameU</span><span class="sxs-lookup"><span data-stu-id="aad24-132">NameU</span></span>  <br/> |<span data-ttu-id="aad24-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="aad24-133">xsd:string</span></span>  <br/> |<span data-ttu-id="aad24-134">Optional</span><span class="sxs-lookup"><span data-stu-id="aad24-134">optional</span></span>  <br/> ||<span data-ttu-id="aad24-135">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="aad24-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="aad24-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="aad24-136">UniqueID</span></span>  <br/> |<span data-ttu-id="aad24-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="aad24-137">xsd:string</span></span>  <br/> |<span data-ttu-id="aad24-138">Optional</span><span class="sxs-lookup"><span data-stu-id="aad24-138">optional</span></span>  <br/> ||<span data-ttu-id="aad24-139">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="aad24-139">Values of the xsd:string type.</span></span>  <br/> |
   

