---
title: AuthorEntry_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6ea7b946-ecd3-1524-5e36-a2c35cb11d7a
ms.openlocfilehash: 39cf47915230b18d22db78f5470fd9c26b9c77ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796396"
---
# <a name="authorentrytype-complextype-visio-xml"></a><span data-ttu-id="19daa-102">AuthorEntry_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="19daa-102">AuthorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="19daa-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="19daa-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19daa-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="19daa-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="19daa-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="19daa-105">**Schema file**</span></span> <br/> |<span data-ttu-id="19daa-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="19daa-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="19daa-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="19daa-107">**Extension base**</span></span> <br/> |<span data-ttu-id="19daa-108">Keine</span><span class="sxs-lookup"><span data-stu-id="19daa-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="19daa-109">Definition</span><span class="sxs-lookup"><span data-stu-id="19daa-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="19daa-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="19daa-110">Elements and attributes</span></span>

<span data-ttu-id="19daa-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="19daa-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="19daa-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="19daa-112">Child elements</span></span>

<span data-ttu-id="19daa-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="19daa-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="19daa-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="19daa-114">Attributes</span></span>

|<span data-ttu-id="19daa-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="19daa-115">**Attribute**</span></span>|<span data-ttu-id="19daa-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="19daa-116">**Type**</span></span>|<span data-ttu-id="19daa-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="19daa-117">**Required**</span></span>|<span data-ttu-id="19daa-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="19daa-118">**Description**</span></span>|<span data-ttu-id="19daa-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="19daa-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="19daa-120">ID</span><span class="sxs-lookup"><span data-stu-id="19daa-120">ID</span></span>  <br/> |<span data-ttu-id="19daa-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="19daa-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="19daa-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="19daa-122">required</span></span>  <br/> ||<span data-ttu-id="19daa-123">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="19daa-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="19daa-124">Initialen</span><span class="sxs-lookup"><span data-stu-id="19daa-124">Initials</span></span>  <br/> |<span data-ttu-id="19daa-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="19daa-125">xsd:string</span></span>  <br/> |<span data-ttu-id="19daa-126">Optional</span><span class="sxs-lookup"><span data-stu-id="19daa-126">optional</span></span>  <br/> ||<span data-ttu-id="19daa-127">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="19daa-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="19daa-128">Name</span><span class="sxs-lookup"><span data-stu-id="19daa-128">Name</span></span>  <br/> |<span data-ttu-id="19daa-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="19daa-129">xsd:string</span></span>  <br/> |<span data-ttu-id="19daa-130">Optional</span><span class="sxs-lookup"><span data-stu-id="19daa-130">optional</span></span>  <br/> ||<span data-ttu-id="19daa-131">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="19daa-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="19daa-132">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="19daa-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="19daa-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="19daa-133">xsd:string</span></span>  <br/> |<span data-ttu-id="19daa-134">Optional</span><span class="sxs-lookup"><span data-stu-id="19daa-134">optional</span></span>  <br/> ||<span data-ttu-id="19daa-135">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="19daa-135">Values of the xsd:string type.</span></span>  <br/> |
   

