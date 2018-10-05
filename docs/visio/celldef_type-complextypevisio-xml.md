---
title: CellDef_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ea346d-1786-dc87-073d-8e7459b7fef1
ms.openlocfilehash: bdcfadc36f278fc97b8589b2989d214e5f4b3333
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399984"
---
# <a name="celldeftype-complextype-visio-xml"></a><span data-ttu-id="b486f-102">CellDef_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="b486f-102">CellDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b486f-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="b486f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b486f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b486f-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b486f-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="b486f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b486f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b486f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b486f-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="b486f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b486f-108">Keine</span><span class="sxs-lookup"><span data-stu-id="b486f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b486f-109">Definition</span><span class="sxs-lookup"><span data-stu-id="b486f-109">Definition</span></span>

```XML
      <xs:complexType name="CellDef_Type">
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="F"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b486f-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="b486f-110">Elements and attributes</span></span>

<span data-ttu-id="b486f-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="b486f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b486f-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b486f-112">Child elements</span></span>

<span data-ttu-id="b486f-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="b486f-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b486f-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="b486f-114">Attributes</span></span>

|<span data-ttu-id="b486f-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b486f-115">**Attribute**</span></span>|<span data-ttu-id="b486f-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b486f-116">**Type**</span></span>|<span data-ttu-id="b486f-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="b486f-117">**Required**</span></span>|<span data-ttu-id="b486f-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b486f-118">**Description**</span></span>|<span data-ttu-id="b486f-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="b486f-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b486f-120">F</span><span class="sxs-lookup"><span data-stu-id="b486f-120">F</span></span>  <br/> |<span data-ttu-id="b486f-121">XSD: String</span><span class="sxs-lookup"><span data-stu-id="b486f-121">xsd:string</span></span>  <br/> |<span data-ttu-id="b486f-122">Optional</span><span class="sxs-lookup"><span data-stu-id="b486f-122">optional</span></span>  <br/> ||<span data-ttu-id="b486f-123">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="b486f-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b486f-124">IX</span><span class="sxs-lookup"><span data-stu-id="b486f-124">IX</span></span>  <br/> |<span data-ttu-id="b486f-125">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="b486f-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="b486f-126">Optional</span><span class="sxs-lookup"><span data-stu-id="b486f-126">optional</span></span>  <br/> ||<span data-ttu-id="b486f-127">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="b486f-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="b486f-128">N</span><span class="sxs-lookup"><span data-stu-id="b486f-128">N</span></span>  <br/> |<span data-ttu-id="b486f-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="b486f-129">xsd:string</span></span>  <br/> |<span data-ttu-id="b486f-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="b486f-130">required</span></span>  <br/> ||<span data-ttu-id="b486f-131">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="b486f-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b486f-132">S</span><span class="sxs-lookup"><span data-stu-id="b486f-132">S</span></span>  <br/> |<span data-ttu-id="b486f-133">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="b486f-133">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="b486f-134">Optional</span><span class="sxs-lookup"><span data-stu-id="b486f-134">optional</span></span>  <br/> ||<span data-ttu-id="b486f-135">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="b486f-135">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="b486f-136">T</span><span class="sxs-lookup"><span data-stu-id="b486f-136">T</span></span>  <br/> |<span data-ttu-id="b486f-137">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="b486f-137">xsd:token</span></span>  <br/> |<span data-ttu-id="b486f-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="b486f-138">required</span></span>  <br/> ||<span data-ttu-id="b486f-139">Werte des Typs Xsd:token.</span><span class="sxs-lookup"><span data-stu-id="b486f-139">Values of the xsd:token type.</span></span>  <br/> |
   

