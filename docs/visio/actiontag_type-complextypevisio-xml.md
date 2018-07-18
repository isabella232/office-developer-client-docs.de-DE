---
title: ActionTag_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bcc17e7-d59d-d392-f299-78d7665202fc
ms.openlocfilehash: e5061e4a4e6e51437ba53ec01f1bfcc33a17d6ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796375"
---
# <a name="actiontagtype-complextype-visio-xml"></a><span data-ttu-id="118a7-102">ActionTag_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="118a7-102">ActionTag_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="118a7-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="118a7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="118a7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="118a7-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="118a7-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="118a7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="118a7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="118a7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="118a7-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="118a7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="118a7-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="118a7-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="118a7-109">Definition</span><span class="sxs-lookup"><span data-stu-id="118a7-109">Definition</span></span>

```XML
          <xs:complexType name="ActionTag_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ActionTagRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="118a7-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="118a7-110">Elements and attributes</span></span>

<span data-ttu-id="118a7-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="118a7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="118a7-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="118a7-112">Child elements</span></span>

|<span data-ttu-id="118a7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="118a7-113">**Element**</span></span>|<span data-ttu-id="118a7-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="118a7-114">**Type**</span></span>|<span data-ttu-id="118a7-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="118a7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="118a7-116">Row</span><span class="sxs-lookup"><span data-stu-id="118a7-116">Row</span></span>](row-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="118a7-117">ActionTagRow_Type</span><span class="sxs-lookup"><span data-stu-id="118a7-117">ActionTagRow_Type</span></span>](actiontagrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="118a7-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="118a7-118">Attributes</span></span>

<span data-ttu-id="118a7-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="118a7-119">None.</span></span>
  

