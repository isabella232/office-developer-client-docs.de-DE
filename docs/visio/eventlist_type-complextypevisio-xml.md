---
title: EventList_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e7a6e5e-5ce4-1e21-c1e8-dafd22bd367f
ms.openlocfilehash: 454a54749e9f72cacc3e7359041705d3487b9e79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351023"
---
# <a name="eventlisttype-complextype-visio-xml"></a><span data-ttu-id="ad461-102">EventList_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="ad461-102">EventList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ad461-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="ad461-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad461-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ad461-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ad461-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ad461-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ad461-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="ad461-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ad461-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="ad461-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ad461-108">Keine</span><span class="sxs-lookup"><span data-stu-id="ad461-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ad461-109">Definition</span><span class="sxs-lookup"><span data-stu-id="ad461-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ad461-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ad461-110">Elements and attributes</span></span>

<span data-ttu-id="ad461-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="ad461-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ad461-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ad461-112">Child elements</span></span>

|<span data-ttu-id="ad461-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad461-113">**Element**</span></span>|<span data-ttu-id="ad461-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ad461-114">**Type**</span></span>|<span data-ttu-id="ad461-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad461-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad461-116">EventItem</span><span class="sxs-lookup"><span data-stu-id="ad461-116">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad461-117">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="ad461-117">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ad461-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="ad461-118">Attributes</span></span>

<span data-ttu-id="ad461-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="ad461-119">None.</span></span>
  

