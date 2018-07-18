---
title: ColorEntry_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d56b6110-634d-02d8-cf11-7902a2aaaf49
ms.openlocfilehash: 58a0abdd4f7f8c2014ec8c6763441840a07b93db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796640"
---
# <a name="colorentrytype-complextype-visio-xml"></a><span data-ttu-id="24e8c-102">ColorEntry_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="24e8c-102">ColorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="24e8c-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="24e8c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24e8c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="24e8c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="24e8c-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="24e8c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="24e8c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="24e8c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="24e8c-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="24e8c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="24e8c-108">Keine</span><span class="sxs-lookup"><span data-stu-id="24e8c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="24e8c-109">Definition</span><span class="sxs-lookup"><span data-stu-id="24e8c-109">Definition</span></span>

```XML
      <xs:complexType name="ColorEntry_Type">
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="RGB"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="24e8c-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="24e8c-110">Elements and attributes</span></span>

<span data-ttu-id="24e8c-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="24e8c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="24e8c-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="24e8c-112">Child elements</span></span>

<span data-ttu-id="24e8c-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="24e8c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="24e8c-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="24e8c-114">Attributes</span></span>

|<span data-ttu-id="24e8c-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="24e8c-115">**Attribute**</span></span>|<span data-ttu-id="24e8c-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="24e8c-116">**Type**</span></span>|<span data-ttu-id="24e8c-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="24e8c-117">**Required**</span></span>|<span data-ttu-id="24e8c-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="24e8c-118">**Description**</span></span>|<span data-ttu-id="24e8c-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="24e8c-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="24e8c-120">IX</span><span class="sxs-lookup"><span data-stu-id="24e8c-120">IX</span></span>  <br/> |<span data-ttu-id="24e8c-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="24e8c-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="24e8c-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="24e8c-122">required</span></span>  <br/> ||<span data-ttu-id="24e8c-123">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="24e8c-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="24e8c-124">RGB</span><span class="sxs-lookup"><span data-stu-id="24e8c-124">RGB</span></span>  <br/> |<span data-ttu-id="24e8c-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="24e8c-125">xsd:string</span></span>  <br/> |<span data-ttu-id="24e8c-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="24e8c-126">required</span></span>  <br/> ||<span data-ttu-id="24e8c-127">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="24e8c-127">Values of the xsd:string type.</span></span>  <br/> |
   

