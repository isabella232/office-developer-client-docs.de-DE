---
title: EventList_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e7a6e5e-5ce4-1e21-c1e8-dafd22bd367f
ms.openlocfilehash: 7bbb8d1074d869a9171a188118c920260b3a903d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796958"
---
# <a name="eventlisttype-complextype-visio-xml"></a><span data-ttu-id="f17d9-102">EventList_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="f17d9-102">EventList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f17d9-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="f17d9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f17d9-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f17d9-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f17d9-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="f17d9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f17d9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f17d9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f17d9-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="f17d9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f17d9-108">Keine</span><span class="sxs-lookup"><span data-stu-id="f17d9-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f17d9-109">Definition</span><span class="sxs-lookup"><span data-stu-id="f17d9-109">Definition</span></span>

```XML
          <xs:complexType name="EventList_Type">
          
          <xs:sequence>
    <xs:element name="EventItem"  type="EventItem_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f17d9-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="f17d9-110">Elements and attributes</span></span>

<span data-ttu-id="f17d9-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="f17d9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f17d9-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f17d9-112">Child elements</span></span>

|<span data-ttu-id="f17d9-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f17d9-113">**Element**</span></span>|<span data-ttu-id="f17d9-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f17d9-114">**Type**</span></span>|<span data-ttu-id="f17d9-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f17d9-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f17d9-116">EventItem</span><span class="sxs-lookup"><span data-stu-id="f17d9-116">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f17d9-117">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="f17d9-117">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f17d9-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="f17d9-118">Attributes</span></span>

<span data-ttu-id="f17d9-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="f17d9-119">None.</span></span>
  

