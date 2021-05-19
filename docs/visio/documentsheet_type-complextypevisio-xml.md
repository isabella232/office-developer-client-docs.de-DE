---
title: DocumentSheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: 18e7f064b1b6c9ac8e084c96011c1b18a646aecb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540007"
---
# <a name="documentsheet_type-complextype-visio-xml"></a><span data-ttu-id="fd980-102">DocumentSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="fd980-102">DocumentSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="fd980-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="fd980-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fd980-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fd980-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fd980-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="fd980-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fd980-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fd980-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fd980-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="fd980-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fd980-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="fd980-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fd980-109">Definition</span><span class="sxs-lookup"><span data-stu-id="fd980-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="fd980-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="fd980-110">Elements and attributes</span></span>

<span data-ttu-id="fd980-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="fd980-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fd980-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fd980-112">Child elements</span></span>

<span data-ttu-id="fd980-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="fd980-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fd980-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="fd980-114">Attributes</span></span>

|<span data-ttu-id="fd980-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="fd980-115">**Attribute**</span></span>|<span data-ttu-id="fd980-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="fd980-116">**Type**</span></span>|<span data-ttu-id="fd980-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="fd980-117">**Required**</span></span>|<span data-ttu-id="fd980-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fd980-118">**Description**</span></span>|<span data-ttu-id="fd980-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="fd980-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fd980-120">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="fd980-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="fd980-121">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="fd980-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="fd980-122">Optional</span><span class="sxs-lookup"><span data-stu-id="fd980-122">optional</span></span>  <br/> ||<span data-ttu-id="fd980-123">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="fd980-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="fd980-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="fd980-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="fd980-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="fd980-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="fd980-126">Optional</span><span class="sxs-lookup"><span data-stu-id="fd980-126">optional</span></span>  <br/> ||<span data-ttu-id="fd980-127">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="fd980-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="fd980-128">Name</span><span class="sxs-lookup"><span data-stu-id="fd980-128">Name</span></span>  <br/> |<span data-ttu-id="fd980-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fd980-129">xsd:string</span></span>  <br/> |<span data-ttu-id="fd980-130">Optional</span><span class="sxs-lookup"><span data-stu-id="fd980-130">optional</span></span>  <br/> ||<span data-ttu-id="fd980-131">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="fd980-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fd980-132">NameU</span><span class="sxs-lookup"><span data-stu-id="fd980-132">NameU</span></span>  <br/> |<span data-ttu-id="fd980-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fd980-133">xsd:string</span></span>  <br/> |<span data-ttu-id="fd980-134">Optional</span><span class="sxs-lookup"><span data-stu-id="fd980-134">optional</span></span>  <br/> ||<span data-ttu-id="fd980-135">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="fd980-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fd980-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="fd980-136">UniqueID</span></span>  <br/> |<span data-ttu-id="fd980-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fd980-137">xsd:string</span></span>  <br/> |<span data-ttu-id="fd980-138">Optional</span><span class="sxs-lookup"><span data-stu-id="fd980-138">optional</span></span>  <br/> ||<span data-ttu-id="fd980-139">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="fd980-139">Values of the xsd:string type.</span></span>  <br/> |
   

