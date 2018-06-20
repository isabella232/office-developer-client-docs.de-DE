---
title: Hyperlink_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 48c31987-bb85-e49a-c337-740fa507a02d
ms.openlocfilehash: 226af4fee615b0dc6ddc4d92d13aff6dd1fd4b19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797155"
---
# <a name="hyperlinktype-complextype-visio-xml"></a><span data-ttu-id="23880-102">Hyperlink_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="23880-102">Hyperlink_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="23880-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="23880-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23880-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="23880-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="23880-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="23880-105">**Schema file**</span></span> <br/> |<span data-ttu-id="23880-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="23880-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="23880-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="23880-107">**Extension base**</span></span> <br/> |<span data-ttu-id="23880-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="23880-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="23880-109">Definition</span><span class="sxs-lookup"><span data-stu-id="23880-109">Definition</span></span>

```XML
          <xs:complexType name="Hyperlink_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="HyperlinkRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="23880-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="23880-110">Elements and attributes</span></span>

<span data-ttu-id="23880-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="23880-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="23880-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="23880-112">Child elements</span></span>

|<span data-ttu-id="23880-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="23880-113">**Element**</span></span>|<span data-ttu-id="23880-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="23880-114">**Type**</span></span>|<span data-ttu-id="23880-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="23880-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="23880-116">Row</span><span class="sxs-lookup"><span data-stu-id="23880-116">Row</span></span>](row-element-hyperlink-sectionvisio-xml.md) <br/> |[<span data-ttu-id="23880-117">HyperlinkRow_Type</span><span class="sxs-lookup"><span data-stu-id="23880-117">HyperlinkRow_Type</span></span>](hyperlinkrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="23880-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="23880-118">Attributes</span></span>

<span data-ttu-id="23880-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="23880-119">None.</span></span>
  

