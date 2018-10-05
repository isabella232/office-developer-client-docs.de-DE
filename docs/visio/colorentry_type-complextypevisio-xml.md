---
title: ColorEntry_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d56b6110-634d-02d8-cf11-7902a2aaaf49
ms.openlocfilehash: c5f2cafba60cd8157f80dc548cea328d179e74db
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394909"
---
# <a name="colorentrytype-complextype-visio-xml"></a><span data-ttu-id="961c7-102">ColorEntry_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="961c7-102">ColorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="961c7-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="961c7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="961c7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="961c7-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="961c7-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="961c7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="961c7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="961c7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="961c7-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="961c7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="961c7-108">Keine</span><span class="sxs-lookup"><span data-stu-id="961c7-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="961c7-109">Definition</span><span class="sxs-lookup"><span data-stu-id="961c7-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="961c7-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="961c7-110">Elements and attributes</span></span>

<span data-ttu-id="961c7-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="961c7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="961c7-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="961c7-112">Child elements</span></span>

<span data-ttu-id="961c7-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="961c7-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="961c7-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="961c7-114">Attributes</span></span>

|<span data-ttu-id="961c7-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="961c7-115">**Attribute**</span></span>|<span data-ttu-id="961c7-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="961c7-116">**Type**</span></span>|<span data-ttu-id="961c7-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="961c7-117">**Required**</span></span>|<span data-ttu-id="961c7-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="961c7-118">**Description**</span></span>|<span data-ttu-id="961c7-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="961c7-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="961c7-120">IX</span><span class="sxs-lookup"><span data-stu-id="961c7-120">IX</span></span>  <br/> |<span data-ttu-id="961c7-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="961c7-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="961c7-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="961c7-122">required</span></span>  <br/> ||<span data-ttu-id="961c7-123">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="961c7-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="961c7-124">RGB</span><span class="sxs-lookup"><span data-stu-id="961c7-124">RGB</span></span>  <br/> |<span data-ttu-id="961c7-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="961c7-125">xsd:string</span></span>  <br/> |<span data-ttu-id="961c7-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="961c7-126">required</span></span>  <br/> ||<span data-ttu-id="961c7-127">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="961c7-127">Values of the xsd:string type.</span></span>  <br/> |
   

