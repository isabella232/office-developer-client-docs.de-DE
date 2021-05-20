---
title: AuthorEntry_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6ea7b946-ecd3-1524-5e36-a2c35cb11d7a
ms.openlocfilehash: 41279e9f4ffa0bba17d4f74eb2f40d724589c17d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537878"
---
# <a name="authorentry_type-complextype-visio-xml"></a><span data-ttu-id="841bb-102">AuthorEntry_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="841bb-102">AuthorEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="841bb-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="841bb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="841bb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="841bb-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="841bb-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="841bb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="841bb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="841bb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="841bb-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="841bb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="841bb-108">Keine</span><span class="sxs-lookup"><span data-stu-id="841bb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="841bb-109">Definition</span><span class="sxs-lookup"><span data-stu-id="841bb-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="841bb-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="841bb-110">Elements and attributes</span></span>

<span data-ttu-id="841bb-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="841bb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="841bb-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="841bb-112">Child elements</span></span>

<span data-ttu-id="841bb-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="841bb-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="841bb-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="841bb-114">Attributes</span></span>

|<span data-ttu-id="841bb-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="841bb-115">**Attribute**</span></span>|<span data-ttu-id="841bb-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="841bb-116">**Type**</span></span>|<span data-ttu-id="841bb-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="841bb-117">**Required**</span></span>|<span data-ttu-id="841bb-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="841bb-118">**Description**</span></span>|<span data-ttu-id="841bb-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="841bb-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="841bb-120">ID</span><span class="sxs-lookup"><span data-stu-id="841bb-120">ID</span></span>  <br/> |<span data-ttu-id="841bb-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="841bb-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="841bb-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="841bb-122">required</span></span>  <br/> ||<span data-ttu-id="841bb-123">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="841bb-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="841bb-124">Initialen</span><span class="sxs-lookup"><span data-stu-id="841bb-124">Initials</span></span>  <br/> |<span data-ttu-id="841bb-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="841bb-125">xsd:string</span></span>  <br/> |<span data-ttu-id="841bb-126">Optional</span><span class="sxs-lookup"><span data-stu-id="841bb-126">optional</span></span>  <br/> ||<span data-ttu-id="841bb-127">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="841bb-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="841bb-128">Name</span><span class="sxs-lookup"><span data-stu-id="841bb-128">Name</span></span>  <br/> |<span data-ttu-id="841bb-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="841bb-129">xsd:string</span></span>  <br/> |<span data-ttu-id="841bb-130">Optional</span><span class="sxs-lookup"><span data-stu-id="841bb-130">optional</span></span>  <br/> ||<span data-ttu-id="841bb-131">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="841bb-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="841bb-132">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="841bb-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="841bb-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="841bb-133">xsd:string</span></span>  <br/> |<span data-ttu-id="841bb-134">Optional</span><span class="sxs-lookup"><span data-stu-id="841bb-134">optional</span></span>  <br/> ||<span data-ttu-id="841bb-135">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="841bb-135">Values of the xsd:string type.</span></span>  <br/> |
   

