---
title: Colors_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f997b5-1f3c-ddff-41f2-af84960266ff
ms.openlocfilehash: bddcb93451bfb6d1b519720040a9e3875dc2ec5c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540140"
---
# <a name="colorstype-complextype-visio-xml"></a><span data-ttu-id="fefa3-102">Colors_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="fefa3-102">Colors_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="fefa3-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="fefa3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fefa3-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fefa3-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fefa3-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="fefa3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fefa3-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="fefa3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fefa3-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="fefa3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fefa3-108">Keine</span><span class="sxs-lookup"><span data-stu-id="fefa3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fefa3-109">Definition</span><span class="sxs-lookup"><span data-stu-id="fefa3-109">Definition</span></span>

```XML
          <xs:complexType name="Colors_Type">
          
          <xs:sequence>
    <xs:element name="ColorEntry"  type="ColorEntry_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fefa3-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="fefa3-110">Elements and attributes</span></span>

<span data-ttu-id="fefa3-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="fefa3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fefa3-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fefa3-112">Child elements</span></span>

|<span data-ttu-id="fefa3-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="fefa3-113">**Element**</span></span>|<span data-ttu-id="fefa3-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="fefa3-114">**Type**</span></span>|<span data-ttu-id="fefa3-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fefa3-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fefa3-116">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="fefa3-116">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fefa3-117">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="fefa3-117">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="fefa3-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="fefa3-118">Attributes</span></span>

<span data-ttu-id="fefa3-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="fefa3-119">None.</span></span>
  

