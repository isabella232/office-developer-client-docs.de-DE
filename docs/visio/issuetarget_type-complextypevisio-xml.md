---
title: IssueTarget_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0dde1d-5748-63ce-b0da-87f545299b38
ms.openlocfilehash: b9e69edc5bd30ede969bc77d43501a4473e9f69e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797247"
---
# <a name="issuetargettype-complextype-visio-xml"></a><span data-ttu-id="0bbf3-102">IssueTarget_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="0bbf3-102">IssueTarget_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0bbf3-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="0bbf3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0bbf3-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0bbf3-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0bbf3-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="0bbf3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0bbf3-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0bbf3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0bbf3-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="0bbf3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0bbf3-108">Keine</span><span class="sxs-lookup"><span data-stu-id="0bbf3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0bbf3-109">Definition</span><span class="sxs-lookup"><span data-stu-id="0bbf3-109">Definition</span></span>

```XML
      <xs:complexType name="IssueTarget_Type">
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0bbf3-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="0bbf3-110">Elements and attributes</span></span>

<span data-ttu-id="0bbf3-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="0bbf3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0bbf3-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0bbf3-112">Child elements</span></span>

<span data-ttu-id="0bbf3-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="0bbf3-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0bbf3-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="0bbf3-114">Attributes</span></span>

|<span data-ttu-id="0bbf3-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0bbf3-115">**Attribute**</span></span>|<span data-ttu-id="0bbf3-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0bbf3-116">**Type**</span></span>|<span data-ttu-id="0bbf3-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="0bbf3-117">**Required**</span></span>|<span data-ttu-id="0bbf3-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0bbf3-118">**Description**</span></span>|<span data-ttu-id="0bbf3-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="0bbf3-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0bbf3-120">PageID</span><span class="sxs-lookup"><span data-stu-id="0bbf3-120">PageID</span></span>  <br/> |<span data-ttu-id="0bbf3-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0bbf3-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0bbf3-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0bbf3-122">required</span></span>  <br/> ||<span data-ttu-id="0bbf3-123">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0bbf3-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0bbf3-124">ShapeID</span><span class="sxs-lookup"><span data-stu-id="0bbf3-124">ShapeID</span></span>  <br/> |<span data-ttu-id="0bbf3-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0bbf3-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0bbf3-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0bbf3-126">required</span></span>  <br/> ||<span data-ttu-id="0bbf3-127">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0bbf3-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

