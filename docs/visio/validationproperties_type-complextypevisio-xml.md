---
title: ValidationProperties_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b0d1209-4636-ea9c-acf7-895c3300492a
ms.openlocfilehash: 2fa6724ce6262886379f3ac22625927608184bab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355979"
---
# <a name="validationpropertiestype-complextype-visio-xml"></a><span data-ttu-id="d2d51-102">ValidationProperties_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="d2d51-102">ValidationProperties_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d2d51-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="d2d51-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d2d51-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d2d51-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d2d51-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="d2d51-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d2d51-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="d2d51-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d2d51-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="d2d51-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d2d51-108">Keine</span><span class="sxs-lookup"><span data-stu-id="d2d51-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d2d51-109">Definition</span><span class="sxs-lookup"><span data-stu-id="d2d51-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d2d51-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="d2d51-110">Elements and attributes</span></span>

<span data-ttu-id="d2d51-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="d2d51-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d2d51-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d2d51-112">Child elements</span></span>

<span data-ttu-id="d2d51-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="d2d51-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d2d51-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="d2d51-114">Attributes</span></span>

|<span data-ttu-id="d2d51-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d2d51-115">**Attribute**</span></span>|<span data-ttu-id="d2d51-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d2d51-116">**Type**</span></span>|<span data-ttu-id="d2d51-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d2d51-117">**Required**</span></span>|<span data-ttu-id="d2d51-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d2d51-118">**Description**</span></span>|<span data-ttu-id="d2d51-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="d2d51-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d2d51-120">LastValidated</span><span class="sxs-lookup"><span data-stu-id="d2d51-120">LastValidated</span></span>  <br/> |<span data-ttu-id="d2d51-121">XSD: dateTime</span><span class="sxs-lookup"><span data-stu-id="d2d51-121">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="d2d51-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d2d51-122">required</span></span>  <br/> ||<span data-ttu-id="d2d51-123">Werte des XSD: dateTime-Typs.</span><span class="sxs-lookup"><span data-stu-id="d2d51-123">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="d2d51-124">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="d2d51-124">ShowIgnored</span></span>  <br/> |<span data-ttu-id="d2d51-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="d2d51-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d2d51-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d2d51-126">required</span></span>  <br/> ||<span data-ttu-id="d2d51-127">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="d2d51-127">Values of the xsd:boolean type.</span></span>  <br/> |
   

