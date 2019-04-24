---
title: RefBy_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e2990281-6410-5a35-2b28-3a8b33246c73
ms.openlocfilehash: ebfc84b2e7eb88078b3b8010f0a7001e90a9cb31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348321"
---
# <a name="refbytype-complextype-visio-xml"></a><span data-ttu-id="b5e8a-102">RefBy_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="b5e8a-102">RefBy_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b5e8a-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="b5e8a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5e8a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b5e8a-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b5e8a-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="b5e8a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b5e8a-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="b5e8a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b5e8a-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="b5e8a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b5e8a-108">Keine</span><span class="sxs-lookup"><span data-stu-id="b5e8a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b5e8a-109">Definition</span><span class="sxs-lookup"><span data-stu-id="b5e8a-109">Definition</span></span>

```XML
      <xs:complexType name="RefBy_Type">
    <xs:attribute name="T"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b5e8a-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="b5e8a-110">Elements and attributes</span></span>

<span data-ttu-id="b5e8a-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="b5e8a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b5e8a-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b5e8a-112">Child elements</span></span>

<span data-ttu-id="b5e8a-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="b5e8a-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5e8a-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="b5e8a-114">Attributes</span></span>

|<span data-ttu-id="b5e8a-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b5e8a-115">**Attribute**</span></span>|<span data-ttu-id="b5e8a-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b5e8a-116">**Type**</span></span>|<span data-ttu-id="b5e8a-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="b5e8a-117">**Required**</span></span>|<span data-ttu-id="b5e8a-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b5e8a-118">**Description**</span></span>|<span data-ttu-id="b5e8a-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="b5e8a-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b5e8a-120">ID</span><span class="sxs-lookup"><span data-stu-id="b5e8a-120">ID</span></span>  <br/> |<span data-ttu-id="b5e8a-121">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b5e8a-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b5e8a-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="b5e8a-122">required</span></span>  <br/> ||<span data-ttu-id="b5e8a-123">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="b5e8a-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b5e8a-124">T</span><span class="sxs-lookup"><span data-stu-id="b5e8a-124">T</span></span>  <br/> |<span data-ttu-id="b5e8a-125">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b5e8a-125">xsd:string</span></span>  <br/> |<span data-ttu-id="b5e8a-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="b5e8a-126">required</span></span>  <br/> ||<span data-ttu-id="b5e8a-127">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="b5e8a-127">Values of the xsd:string type.</span></span>  <br/> |
   

