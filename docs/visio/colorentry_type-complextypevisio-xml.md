---
title: ColorEntry_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d56b6110-634d-02d8-cf11-7902a2aaaf49
ms.openlocfilehash: f5ada3fef8d50c2e53f63c797601980f88349868
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540147"
---
# <a name="colorentrytype-complextype-visio-xml"></a><span data-ttu-id="31508-102">ColorEntry_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="31508-102">ColorEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="31508-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="31508-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31508-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="31508-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="31508-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="31508-105">**Schema file**</span></span> <br/> |<span data-ttu-id="31508-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="31508-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="31508-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="31508-107">**Extension base**</span></span> <br/> |<span data-ttu-id="31508-108">Keine</span><span class="sxs-lookup"><span data-stu-id="31508-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="31508-109">Definition</span><span class="sxs-lookup"><span data-stu-id="31508-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="31508-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="31508-110">Elements and attributes</span></span>

<span data-ttu-id="31508-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="31508-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="31508-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="31508-112">Child elements</span></span>

<span data-ttu-id="31508-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="31508-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="31508-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="31508-114">Attributes</span></span>

|<span data-ttu-id="31508-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="31508-115">**Attribute**</span></span>|<span data-ttu-id="31508-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="31508-116">**Type**</span></span>|<span data-ttu-id="31508-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="31508-117">**Required**</span></span>|<span data-ttu-id="31508-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="31508-118">**Description**</span></span>|<span data-ttu-id="31508-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="31508-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="31508-120">IX</span><span class="sxs-lookup"><span data-stu-id="31508-120">IX</span></span>  <br/> |<span data-ttu-id="31508-121">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="31508-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="31508-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="31508-122">required</span></span>  <br/> ||<span data-ttu-id="31508-123">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="31508-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="31508-124">RGB</span><span class="sxs-lookup"><span data-stu-id="31508-124">RGB</span></span>  <br/> |<span data-ttu-id="31508-125">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="31508-125">xsd:string</span></span>  <br/> |<span data-ttu-id="31508-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="31508-126">required</span></span>  <br/> ||<span data-ttu-id="31508-127">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="31508-127">Values of the xsd:string type.</span></span>  <br/> |
   

