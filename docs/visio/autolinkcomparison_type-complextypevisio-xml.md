---
title: AutoLinkComparison_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: bb1b07a59fbe3fc706bc67db58e67c5b0ec14033
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796411"
---
# <a name="autolinkcomparisontype-complextype-visio-xml"></a><span data-ttu-id="38b0b-102">AutoLinkComparison_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="38b0b-102">AutoLinkComparison_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="38b0b-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="38b0b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38b0b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="38b0b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="38b0b-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="38b0b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="38b0b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="38b0b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="38b0b-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="38b0b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="38b0b-108">Keine</span><span class="sxs-lookup"><span data-stu-id="38b0b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="38b0b-109">Definition</span><span class="sxs-lookup"><span data-stu-id="38b0b-109">Definition</span></span>

```XML
      <xs:complexType name="AutoLinkComparison_Type">
    <xs:attribute name="ColumnName"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ContextType"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ContextTypeLabel"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="38b0b-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="38b0b-110">Elements and attributes</span></span>

<span data-ttu-id="38b0b-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="38b0b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="38b0b-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="38b0b-112">Child elements</span></span>

<span data-ttu-id="38b0b-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="38b0b-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="38b0b-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="38b0b-114">Attributes</span></span>

|<span data-ttu-id="38b0b-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="38b0b-115">**Attribute**</span></span>|<span data-ttu-id="38b0b-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="38b0b-116">**Type**</span></span>|<span data-ttu-id="38b0b-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="38b0b-117">**Required**</span></span>|<span data-ttu-id="38b0b-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="38b0b-118">**Description**</span></span>|<span data-ttu-id="38b0b-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="38b0b-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="38b0b-120">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="38b0b-120">ColumnName</span></span>  <br/> |<span data-ttu-id="38b0b-121">XSD: String</span><span class="sxs-lookup"><span data-stu-id="38b0b-121">xsd:string</span></span>  <br/> |<span data-ttu-id="38b0b-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="38b0b-122">required</span></span>  <br/> ||<span data-ttu-id="38b0b-123">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="38b0b-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="38b0b-124">ContextType</span><span class="sxs-lookup"><span data-stu-id="38b0b-124">ContextType</span></span>  <br/> |<span data-ttu-id="38b0b-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="38b0b-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="38b0b-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="38b0b-126">required</span></span>  <br/> ||<span data-ttu-id="38b0b-127">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="38b0b-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="38b0b-128">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="38b0b-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="38b0b-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="38b0b-129">xsd:string</span></span>  <br/> |<span data-ttu-id="38b0b-130">Optional</span><span class="sxs-lookup"><span data-stu-id="38b0b-130">optional</span></span>  <br/> ||<span data-ttu-id="38b0b-131">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="38b0b-131">Values of the xsd:string type.</span></span>  <br/> |
   

