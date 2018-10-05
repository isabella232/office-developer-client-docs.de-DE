---
title: ValidationProperties_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b0d1209-4636-ea9c-acf7-895c3300492a
ms.openlocfilehash: 2fa6724ce6262886379f3ac22625927608184bab
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389981"
---
# <a name="validationpropertiestype-complextype-visio-xml"></a><span data-ttu-id="4f043-102">ValidationProperties_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="4f043-102">ValidationProperties_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4f043-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="4f043-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f043-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4f043-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4f043-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="4f043-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4f043-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4f043-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4f043-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="4f043-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4f043-108">Keine</span><span class="sxs-lookup"><span data-stu-id="4f043-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4f043-109">Definition</span><span class="sxs-lookup"><span data-stu-id="4f043-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4f043-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="4f043-110">Elements and attributes</span></span>

<span data-ttu-id="4f043-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="4f043-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4f043-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f043-112">Child elements</span></span>

<span data-ttu-id="4f043-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="4f043-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f043-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="4f043-114">Attributes</span></span>

|<span data-ttu-id="4f043-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4f043-115">**Attribute**</span></span>|<span data-ttu-id="4f043-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4f043-116">**Type**</span></span>|<span data-ttu-id="4f043-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="4f043-117">**Required**</span></span>|<span data-ttu-id="4f043-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f043-118">**Description**</span></span>|<span data-ttu-id="4f043-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="4f043-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4f043-120">LastValidated</span><span class="sxs-lookup"><span data-stu-id="4f043-120">LastValidated</span></span>  <br/> |<span data-ttu-id="4f043-121">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="4f043-121">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="4f043-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="4f043-122">required</span></span>  <br/> ||<span data-ttu-id="4f043-123">Werte des Typs xsd: DateTime.</span><span class="sxs-lookup"><span data-stu-id="4f043-123">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="4f043-124">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="4f043-124">ShowIgnored</span></span>  <br/> |<span data-ttu-id="4f043-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="4f043-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4f043-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="4f043-126">required</span></span>  <br/> ||<span data-ttu-id="4f043-127">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="4f043-127">Values of the xsd:boolean type.</span></span>  <br/> |
   

