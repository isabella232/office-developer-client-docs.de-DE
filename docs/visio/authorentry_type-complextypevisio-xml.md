---
title: AuthorEntry_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6ea7b946-ecd3-1524-5e36-a2c35cb11d7a
ms.openlocfilehash: 7d43d34559f212e3de1a91291cbf14b75a3b2e0c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386838"
---
# <a name="authorentrytype-complextype-visio-xml"></a><span data-ttu-id="7f5f3-102">AuthorEntry_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="7f5f3-102">AuthorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7f5f3-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="7f5f3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7f5f3-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7f5f3-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7f5f3-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="7f5f3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7f5f3-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7f5f3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7f5f3-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="7f5f3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7f5f3-108">Keine</span><span class="sxs-lookup"><span data-stu-id="7f5f3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7f5f3-109">Definition</span><span class="sxs-lookup"><span data-stu-id="7f5f3-109">Definition</span></span>

```XML
      <xs:complexType name="AuthorEntry_Type">
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="Initials"
  type="xsd:string"
    />
    <xs:attribute name="ResolutionID"
  type="xsd:string"
    />
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7f5f3-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="7f5f3-110">Elements and attributes</span></span>

<span data-ttu-id="7f5f3-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="7f5f3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7f5f3-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7f5f3-112">Child elements</span></span>

<span data-ttu-id="7f5f3-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="7f5f3-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7f5f3-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="7f5f3-114">Attributes</span></span>

|<span data-ttu-id="7f5f3-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7f5f3-115">**Attribute**</span></span>|<span data-ttu-id="7f5f3-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7f5f3-116">**Type**</span></span>|<span data-ttu-id="7f5f3-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="7f5f3-117">**Required**</span></span>|<span data-ttu-id="7f5f3-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7f5f3-118">**Description**</span></span>|<span data-ttu-id="7f5f3-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="7f5f3-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7f5f3-120">ID</span><span class="sxs-lookup"><span data-stu-id="7f5f3-120">ID</span></span>  <br/> |<span data-ttu-id="7f5f3-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7f5f3-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7f5f3-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="7f5f3-122">required</span></span>  <br/> ||<span data-ttu-id="7f5f3-123">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7f5f3-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7f5f3-124">Initialen</span><span class="sxs-lookup"><span data-stu-id="7f5f3-124">Initials</span></span>  <br/> |<span data-ttu-id="7f5f3-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="7f5f3-125">xsd:string</span></span>  <br/> |<span data-ttu-id="7f5f3-126">Optional</span><span class="sxs-lookup"><span data-stu-id="7f5f3-126">optional</span></span>  <br/> ||<span data-ttu-id="7f5f3-127">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="7f5f3-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7f5f3-128">Name</span><span class="sxs-lookup"><span data-stu-id="7f5f3-128">Name</span></span>  <br/> |<span data-ttu-id="7f5f3-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="7f5f3-129">xsd:string</span></span>  <br/> |<span data-ttu-id="7f5f3-130">Optional</span><span class="sxs-lookup"><span data-stu-id="7f5f3-130">optional</span></span>  <br/> ||<span data-ttu-id="7f5f3-131">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="7f5f3-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7f5f3-132">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="7f5f3-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="7f5f3-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="7f5f3-133">xsd:string</span></span>  <br/> |<span data-ttu-id="7f5f3-134">Optional</span><span class="sxs-lookup"><span data-stu-id="7f5f3-134">optional</span></span>  <br/> ||<span data-ttu-id="7f5f3-135">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="7f5f3-135">Values of the xsd:string type.</span></span>  <br/> |
   

