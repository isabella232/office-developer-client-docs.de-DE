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
# <a name="colorentrytype-complextype-visio-xml"></a><span data-ttu-id="d5607-102">ColorEntry_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="d5607-102">ColorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d5607-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="d5607-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5607-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d5607-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d5607-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="d5607-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d5607-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d5607-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d5607-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="d5607-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d5607-108">Keine</span><span class="sxs-lookup"><span data-stu-id="d5607-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d5607-109">Definition</span><span class="sxs-lookup"><span data-stu-id="d5607-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d5607-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="d5607-110">Elements and attributes</span></span>

<span data-ttu-id="d5607-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="d5607-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d5607-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d5607-112">Child elements</span></span>

<span data-ttu-id="d5607-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="d5607-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5607-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="d5607-114">Attributes</span></span>

|<span data-ttu-id="d5607-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d5607-115">**Attribute**</span></span>|<span data-ttu-id="d5607-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d5607-116">**Type**</span></span>|<span data-ttu-id="d5607-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d5607-117">**Required**</span></span>|<span data-ttu-id="d5607-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d5607-118">**Description**</span></span>|<span data-ttu-id="d5607-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="d5607-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d5607-120">IX</span><span class="sxs-lookup"><span data-stu-id="d5607-120">IX</span></span>  <br/> |<span data-ttu-id="d5607-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d5607-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d5607-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d5607-122">required</span></span>  <br/> ||<span data-ttu-id="d5607-123">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d5607-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d5607-124">RGB</span><span class="sxs-lookup"><span data-stu-id="d5607-124">RGB</span></span>  <br/> |<span data-ttu-id="d5607-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d5607-125">xsd:string</span></span>  <br/> |<span data-ttu-id="d5607-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d5607-126">required</span></span>  <br/> ||<span data-ttu-id="d5607-127">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d5607-127">Values of the xsd:string type.</span></span>  <br/> |
   

