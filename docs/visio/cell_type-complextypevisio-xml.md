---
title: Cell_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: 4e0cedaab755dab669d79ff52742b8ac2b9f9725
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542303"
---
# <a name="cell_type-complextype-visio-xml"></a><span data-ttu-id="c4617-102">Cell_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c4617-102">Cell_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="c4617-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="c4617-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4617-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c4617-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c4617-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="c4617-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c4617-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c4617-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c4617-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="c4617-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c4617-108">Keine</span><span class="sxs-lookup"><span data-stu-id="c4617-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c4617-109">Definition</span><span class="sxs-lookup"><span data-stu-id="c4617-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c4617-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="c4617-110">Elements and attributes</span></span>

<span data-ttu-id="c4617-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="c4617-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c4617-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c4617-112">Child elements</span></span>

|<span data-ttu-id="c4617-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c4617-113">**Element**</span></span>|<span data-ttu-id="c4617-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c4617-114">**Type**</span></span>|<span data-ttu-id="c4617-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c4617-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c4617-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="c4617-116">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c4617-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="c4617-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c4617-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="c4617-118">Attributes</span></span>

|<span data-ttu-id="c4617-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c4617-119">**Attribute**</span></span>|<span data-ttu-id="c4617-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c4617-120">**Type**</span></span>|<span data-ttu-id="c4617-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="c4617-121">**Required**</span></span>|<span data-ttu-id="c4617-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c4617-122">**Description**</span></span>|<span data-ttu-id="c4617-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="c4617-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c4617-124">E</span><span class="sxs-lookup"><span data-stu-id="c4617-124">E</span></span>  <br/> |<span data-ttu-id="c4617-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c4617-125">xsd:string</span></span>  <br/> |<span data-ttu-id="c4617-126">Optional</span><span class="sxs-lookup"><span data-stu-id="c4617-126">optional</span></span>  <br/> ||<span data-ttu-id="c4617-127">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="c4617-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c4617-128">F</span><span class="sxs-lookup"><span data-stu-id="c4617-128">F</span></span>  <br/> |<span data-ttu-id="c4617-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c4617-129">xsd:string</span></span>  <br/> |<span data-ttu-id="c4617-130">Optional</span><span class="sxs-lookup"><span data-stu-id="c4617-130">optional</span></span>  <br/> ||<span data-ttu-id="c4617-131">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="c4617-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c4617-132">N</span><span class="sxs-lookup"><span data-stu-id="c4617-132">N</span></span>  <br/> |<span data-ttu-id="c4617-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c4617-133">xsd:string</span></span>  <br/> |<span data-ttu-id="c4617-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="c4617-134">required</span></span>  <br/> ||<span data-ttu-id="c4617-135">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="c4617-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c4617-136">U</span><span class="sxs-lookup"><span data-stu-id="c4617-136">U</span></span>  <br/> |<span data-ttu-id="c4617-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c4617-137">xsd:string</span></span>  <br/> |<span data-ttu-id="c4617-138">Optional</span><span class="sxs-lookup"><span data-stu-id="c4617-138">optional</span></span>  <br/> ||<span data-ttu-id="c4617-139">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="c4617-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c4617-140">V</span><span class="sxs-lookup"><span data-stu-id="c4617-140">V</span></span>  <br/> |<span data-ttu-id="c4617-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c4617-141">xsd:string</span></span>  <br/> |<span data-ttu-id="c4617-142">Optional</span><span class="sxs-lookup"><span data-stu-id="c4617-142">optional</span></span>  <br/> ||<span data-ttu-id="c4617-143">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="c4617-143">Values of the xsd:string type.</span></span>  <br/> |
   

