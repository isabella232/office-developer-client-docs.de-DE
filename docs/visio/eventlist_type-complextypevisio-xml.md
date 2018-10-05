---
title: EventList_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e7a6e5e-5ce4-1e21-c1e8-dafd22bd367f
ms.openlocfilehash: 454a54749e9f72cacc3e7359041705d3487b9e79
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392081"
---
# <a name="eventlisttype-complextype-visio-xml"></a><span data-ttu-id="4fe73-102">EventList_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="4fe73-102">EventList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4fe73-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="4fe73-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4fe73-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4fe73-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4fe73-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="4fe73-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4fe73-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4fe73-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4fe73-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="4fe73-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4fe73-108">Keine</span><span class="sxs-lookup"><span data-stu-id="4fe73-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4fe73-109">Definition</span><span class="sxs-lookup"><span data-stu-id="4fe73-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4fe73-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="4fe73-110">Elements and attributes</span></span>

<span data-ttu-id="4fe73-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="4fe73-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4fe73-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4fe73-112">Child elements</span></span>

|<span data-ttu-id="4fe73-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4fe73-113">**Element**</span></span>|<span data-ttu-id="4fe73-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4fe73-114">**Type**</span></span>|<span data-ttu-id="4fe73-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4fe73-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4fe73-116">EventItem</span><span class="sxs-lookup"><span data-stu-id="4fe73-116">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4fe73-117">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="4fe73-117">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4fe73-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="4fe73-118">Attributes</span></span>

<span data-ttu-id="4fe73-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="4fe73-119">None.</span></span>
  

