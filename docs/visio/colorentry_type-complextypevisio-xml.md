---
title: ColorEntry_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d56b6110-634d-02d8-cf11-7902a2aaaf49
ms.openlocfilehash: c5f2cafba60cd8157f80dc548cea328d179e74db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358779"
---
# <a name="colorentrytype-complextype-visio-xml"></a><span data-ttu-id="bfd24-102">ColorEntry_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="bfd24-102">ColorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bfd24-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="bfd24-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bfd24-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bfd24-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bfd24-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="bfd24-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bfd24-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="bfd24-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bfd24-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="bfd24-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bfd24-108">Keine</span><span class="sxs-lookup"><span data-stu-id="bfd24-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bfd24-109">Definition</span><span class="sxs-lookup"><span data-stu-id="bfd24-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="bfd24-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="bfd24-110">Elements and attributes</span></span>

<span data-ttu-id="bfd24-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="bfd24-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bfd24-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bfd24-112">Child elements</span></span>

<span data-ttu-id="bfd24-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="bfd24-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bfd24-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="bfd24-114">Attributes</span></span>

|<span data-ttu-id="bfd24-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="bfd24-115">**Attribute**</span></span>|<span data-ttu-id="bfd24-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="bfd24-116">**Type**</span></span>|<span data-ttu-id="bfd24-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="bfd24-117">**Required**</span></span>|<span data-ttu-id="bfd24-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bfd24-118">**Description**</span></span>|<span data-ttu-id="bfd24-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="bfd24-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bfd24-120">IX</span><span class="sxs-lookup"><span data-stu-id="bfd24-120">IX</span></span>  <br/> |<span data-ttu-id="bfd24-121">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bfd24-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bfd24-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="bfd24-122">required</span></span>  <br/> ||<span data-ttu-id="bfd24-123">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="bfd24-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bfd24-124">RGB</span><span class="sxs-lookup"><span data-stu-id="bfd24-124">RGB</span></span>  <br/> |<span data-ttu-id="bfd24-125">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bfd24-125">xsd:string</span></span>  <br/> |<span data-ttu-id="bfd24-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="bfd24-126">required</span></span>  <br/> ||<span data-ttu-id="bfd24-127">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="bfd24-127">Values of the xsd:string type.</span></span>  <br/> |
   

