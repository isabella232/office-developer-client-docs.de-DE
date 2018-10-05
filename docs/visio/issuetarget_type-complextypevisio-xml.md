---
title: IssueTarget_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0dde1d-5748-63ce-b0da-87f545299b38
ms.openlocfilehash: d7b8309bb6dac9648d379c89687dc89165f44edf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393768"
---
# <a name="issuetargettype-complextype-visio-xml"></a><span data-ttu-id="b9f2a-102">IssueTarget_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="b9f2a-102">IssueTarget_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b9f2a-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="b9f2a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b9f2a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b9f2a-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b9f2a-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="b9f2a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b9f2a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b9f2a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b9f2a-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="b9f2a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b9f2a-108">Keine</span><span class="sxs-lookup"><span data-stu-id="b9f2a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b9f2a-109">Definition</span><span class="sxs-lookup"><span data-stu-id="b9f2a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="b9f2a-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="b9f2a-110">Elements and attributes</span></span>

<span data-ttu-id="b9f2a-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b9f2a-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b9f2a-112">Child elements</span></span>

<span data-ttu-id="b9f2a-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b9f2a-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="b9f2a-114">Attributes</span></span>

|<span data-ttu-id="b9f2a-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b9f2a-115">**Attribute**</span></span>|<span data-ttu-id="b9f2a-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b9f2a-116">**Type**</span></span>|<span data-ttu-id="b9f2a-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="b9f2a-117">**Required**</span></span>|<span data-ttu-id="b9f2a-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b9f2a-118">**Description**</span></span>|<span data-ttu-id="b9f2a-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="b9f2a-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b9f2a-120">PageID</span><span class="sxs-lookup"><span data-stu-id="b9f2a-120">PageID</span></span>  <br/> |<span data-ttu-id="b9f2a-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b9f2a-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b9f2a-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="b9f2a-122">required</span></span>  <br/> ||<span data-ttu-id="b9f2a-123">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b9f2a-124">ShapeID</span><span class="sxs-lookup"><span data-stu-id="b9f2a-124">ShapeID</span></span>  <br/> |<span data-ttu-id="b9f2a-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b9f2a-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b9f2a-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="b9f2a-126">required</span></span>  <br/> ||<span data-ttu-id="b9f2a-127">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

