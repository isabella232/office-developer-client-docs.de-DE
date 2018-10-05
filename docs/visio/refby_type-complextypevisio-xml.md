---
title: RefBy_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e2990281-6410-5a35-2b28-3a8b33246c73
ms.openlocfilehash: ebfc84b2e7eb88078b3b8010f0a7001e90a9cb31
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383484"
---
# <a name="refbytype-complextype-visio-xml"></a><span data-ttu-id="5ddcd-102">RefBy_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="5ddcd-102">RefBy_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5ddcd-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="5ddcd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5ddcd-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5ddcd-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5ddcd-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="5ddcd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5ddcd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5ddcd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5ddcd-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="5ddcd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5ddcd-108">Keine</span><span class="sxs-lookup"><span data-stu-id="5ddcd-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5ddcd-109">Definition</span><span class="sxs-lookup"><span data-stu-id="5ddcd-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="5ddcd-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="5ddcd-110">Elements and attributes</span></span>

<span data-ttu-id="5ddcd-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="5ddcd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5ddcd-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5ddcd-112">Child elements</span></span>

<span data-ttu-id="5ddcd-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="5ddcd-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5ddcd-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="5ddcd-114">Attributes</span></span>

|<span data-ttu-id="5ddcd-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="5ddcd-115">**Attribute**</span></span>|<span data-ttu-id="5ddcd-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="5ddcd-116">**Type**</span></span>|<span data-ttu-id="5ddcd-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="5ddcd-117">**Required**</span></span>|<span data-ttu-id="5ddcd-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5ddcd-118">**Description**</span></span>|<span data-ttu-id="5ddcd-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="5ddcd-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5ddcd-120">ID</span><span class="sxs-lookup"><span data-stu-id="5ddcd-120">ID</span></span>  <br/> |<span data-ttu-id="5ddcd-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5ddcd-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5ddcd-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="5ddcd-122">required</span></span>  <br/> ||<span data-ttu-id="5ddcd-123">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5ddcd-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5ddcd-124">T</span><span class="sxs-lookup"><span data-stu-id="5ddcd-124">T</span></span>  <br/> |<span data-ttu-id="5ddcd-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="5ddcd-125">xsd:string</span></span>  <br/> |<span data-ttu-id="5ddcd-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="5ddcd-126">required</span></span>  <br/> ||<span data-ttu-id="5ddcd-127">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="5ddcd-127">Values of the xsd:string type.</span></span>  <br/> |
   

