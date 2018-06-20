---
title: ValidationProperties_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b0d1209-4636-ea9c-acf7-895c3300492a
ms.openlocfilehash: eb1373881b1584b77c6663dd4ec375c50a61efd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798368"
---
# <a name="validationpropertiestype-complextype-visio-xml"></a><span data-ttu-id="4ccc6-102">ValidationProperties_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="4ccc6-102">ValidationProperties_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4ccc6-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="4ccc6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ccc6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4ccc6-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4ccc6-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="4ccc6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4ccc6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4ccc6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4ccc6-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="4ccc6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4ccc6-108">Keine</span><span class="sxs-lookup"><span data-stu-id="4ccc6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4ccc6-109">Definition</span><span class="sxs-lookup"><span data-stu-id="4ccc6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4ccc6-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="4ccc6-110">Elements and attributes</span></span>

<span data-ttu-id="4ccc6-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="4ccc6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4ccc6-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4ccc6-112">Child elements</span></span>

<span data-ttu-id="4ccc6-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="4ccc6-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4ccc6-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="4ccc6-114">Attributes</span></span>

|<span data-ttu-id="4ccc6-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4ccc6-115">**Attribute**</span></span>|<span data-ttu-id="4ccc6-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4ccc6-116">**Type**</span></span>|<span data-ttu-id="4ccc6-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="4ccc6-117">**Required**</span></span>|<span data-ttu-id="4ccc6-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ccc6-118">**Description**</span></span>|<span data-ttu-id="4ccc6-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="4ccc6-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4ccc6-120">LastValidated</span><span class="sxs-lookup"><span data-stu-id="4ccc6-120">LastValidated</span></span>  <br/> |<span data-ttu-id="4ccc6-121">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="4ccc6-121">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="4ccc6-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="4ccc6-122">required</span></span>  <br/> ||<span data-ttu-id="4ccc6-123">Werte des Typs xsd: DateTime.</span><span class="sxs-lookup"><span data-stu-id="4ccc6-123">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="4ccc6-124">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="4ccc6-124">ShowIgnored</span></span>  <br/> |<span data-ttu-id="4ccc6-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="4ccc6-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4ccc6-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="4ccc6-126">required</span></span>  <br/> ||<span data-ttu-id="4ccc6-127">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="4ccc6-127">Values of the xsd:boolean type.</span></span>  <br/> |
   

