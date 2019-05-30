---
title: ValidationProperties_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b0d1209-4636-ea9c-acf7-895c3300492a
ms.openlocfilehash: d83a1ce8e7ad89155726200de2950da755e5d3db
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538515"
---
# <a name="validationpropertiestype-complextype-visio-xml"></a><span data-ttu-id="d2a6b-102">ValidationProperties_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d2a6b-102">ValidationProperties_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d2a6b-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="d2a6b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d2a6b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d2a6b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d2a6b-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="d2a6b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d2a6b-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="d2a6b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d2a6b-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="d2a6b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d2a6b-108">Keine</span><span class="sxs-lookup"><span data-stu-id="d2a6b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d2a6b-109">Definition</span><span class="sxs-lookup"><span data-stu-id="d2a6b-109">Definition</span></span>

```XML
      <xs:complexType name="ValidationProperties_Type">
    <xs:attribute name="LastValidated"
  type="xsd:dateTime"
     use="required"
    />
    <xs:attribute name="ShowIgnored"
  type="xsd:boolean"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d2a6b-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="d2a6b-110">Elements and attributes</span></span>

<span data-ttu-id="d2a6b-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="d2a6b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d2a6b-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d2a6b-112">Child elements</span></span>

<span data-ttu-id="d2a6b-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="d2a6b-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d2a6b-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="d2a6b-114">Attributes</span></span>

|<span data-ttu-id="d2a6b-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d2a6b-115">**Attribute**</span></span>|<span data-ttu-id="d2a6b-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d2a6b-116">**Type**</span></span>|<span data-ttu-id="d2a6b-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d2a6b-117">**Required**</span></span>|<span data-ttu-id="d2a6b-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d2a6b-118">**Description**</span></span>|<span data-ttu-id="d2a6b-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="d2a6b-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d2a6b-120">LastValidated</span><span class="sxs-lookup"><span data-stu-id="d2a6b-120">LastValidated</span></span>  <br/> |<span data-ttu-id="d2a6b-121">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="d2a6b-121">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="d2a6b-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d2a6b-122">required</span></span>  <br/> ||<span data-ttu-id="d2a6b-123">Werte des Typs XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="d2a6b-123">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="d2a6b-124">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="d2a6b-124">ShowIgnored</span></span>  <br/> |<span data-ttu-id="d2a6b-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="d2a6b-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d2a6b-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d2a6b-126">required</span></span>  <br/> ||<span data-ttu-id="d2a6b-127">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="d2a6b-127">Values of the xsd:boolean type.</span></span>  <br/> |
   

