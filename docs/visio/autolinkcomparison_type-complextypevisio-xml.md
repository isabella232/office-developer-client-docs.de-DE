---
title: AutoLinkComparison_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: 235b63777d21955a2f2062757d6a54e899b169ac
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389750"
---
# <a name="autolinkcomparisontype-complextype-visio-xml"></a><span data-ttu-id="0e568-102">AutoLinkComparison_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="0e568-102">AutoLinkComparison_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0e568-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="0e568-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e568-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0e568-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0e568-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="0e568-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0e568-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0e568-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0e568-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="0e568-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0e568-108">Keine</span><span class="sxs-lookup"><span data-stu-id="0e568-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0e568-109">Definition</span><span class="sxs-lookup"><span data-stu-id="0e568-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0e568-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="0e568-110">Elements and attributes</span></span>

<span data-ttu-id="0e568-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="0e568-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0e568-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0e568-112">Child elements</span></span>

<span data-ttu-id="0e568-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="0e568-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0e568-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="0e568-114">Attributes</span></span>

|<span data-ttu-id="0e568-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0e568-115">**Attribute**</span></span>|<span data-ttu-id="0e568-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0e568-116">**Type**</span></span>|<span data-ttu-id="0e568-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="0e568-117">**Required**</span></span>|<span data-ttu-id="0e568-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0e568-118">**Description**</span></span>|<span data-ttu-id="0e568-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="0e568-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0e568-120">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="0e568-120">ColumnName</span></span>  <br/> |<span data-ttu-id="0e568-121">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0e568-121">xsd:string</span></span>  <br/> |<span data-ttu-id="0e568-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0e568-122">required</span></span>  <br/> ||<span data-ttu-id="0e568-123">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0e568-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0e568-124">ContextType</span><span class="sxs-lookup"><span data-stu-id="0e568-124">ContextType</span></span>  <br/> |<span data-ttu-id="0e568-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0e568-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0e568-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0e568-126">required</span></span>  <br/> ||<span data-ttu-id="0e568-127">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0e568-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0e568-128">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="0e568-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="0e568-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0e568-129">xsd:string</span></span>  <br/> |<span data-ttu-id="0e568-130">Optional</span><span class="sxs-lookup"><span data-stu-id="0e568-130">optional</span></span>  <br/> ||<span data-ttu-id="0e568-131">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0e568-131">Values of the xsd:string type.</span></span>  <br/> |
   

