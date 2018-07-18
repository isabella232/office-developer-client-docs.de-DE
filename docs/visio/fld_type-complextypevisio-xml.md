---
title: Fld_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f680eb55-2dbb-a7b9-0879-6e91576983f3
ms.openlocfilehash: c4ea016adea237258ba699c54bf05b902119eca1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797027"
---
# <a name="fldtype-complextype-visio-xml"></a><span data-ttu-id="37f28-102">Fld_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="37f28-102">fld_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="37f28-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="37f28-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37f28-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="37f28-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="37f28-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="37f28-105">**Schema file**</span></span> <br/> |<span data-ttu-id="37f28-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="37f28-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="37f28-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="37f28-107">**Extension base**</span></span> <br/> |<span data-ttu-id="37f28-108">XSD: String</span><span class="sxs-lookup"><span data-stu-id="37f28-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="37f28-109">Definition</span><span class="sxs-lookup"><span data-stu-id="37f28-109">Definition</span></span>

```XML
      <xs:complexType name="fld_Type">
        <xs:complexContent>
        <xs:extension base="xsd:string">
      
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="37f28-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="37f28-110">Elements and attributes</span></span>

<span data-ttu-id="37f28-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="37f28-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="37f28-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="37f28-112">Child elements</span></span>

<span data-ttu-id="37f28-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="37f28-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="37f28-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="37f28-114">Attributes</span></span>

|<span data-ttu-id="37f28-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="37f28-115">**Attribute**</span></span>|<span data-ttu-id="37f28-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="37f28-116">**Type**</span></span>|<span data-ttu-id="37f28-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="37f28-117">**Required**</span></span>|<span data-ttu-id="37f28-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="37f28-118">**Description**</span></span>|<span data-ttu-id="37f28-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="37f28-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="37f28-120">IX</span><span class="sxs-lookup"><span data-stu-id="37f28-120">IX</span></span>  <br/> |<span data-ttu-id="37f28-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="37f28-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="37f28-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="37f28-122">required</span></span>  <br/> ||<span data-ttu-id="37f28-123">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="37f28-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

