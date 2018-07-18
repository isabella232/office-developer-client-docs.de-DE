---
title: RelCubBezTo_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 004dc563-d089-230f-0055-038b72eebbed
ms.openlocfilehash: 5dec2bde6b2ac704d9107bf195282bb3f53e61e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797828"
---
# <a name="relcubbeztotype-complextype-visio-xml"></a><span data-ttu-id="c304b-102">RelCubBezTo_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="c304b-102">RelCubBezTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c304b-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="c304b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c304b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c304b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c304b-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="c304b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c304b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c304b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c304b-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="c304b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c304b-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="c304b-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c304b-109">Definition</span><span class="sxs-lookup"><span data-stu-id="c304b-109">Definition</span></span>

```XML
          <xs:complexType name="RelCubBezTo_Type">
          
          <xs:complexContent>
          <xs:extension base="GeometryRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c304b-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="c304b-110">Elements and attributes</span></span>

<span data-ttu-id="c304b-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="c304b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c304b-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c304b-112">Child elements</span></span>

|<span data-ttu-id="c304b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c304b-113">**Element**</span></span>|<span data-ttu-id="c304b-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c304b-114">**Type**</span></span>|<span data-ttu-id="c304b-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c304b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c304b-116">Cell</span><span class="sxs-lookup"><span data-stu-id="c304b-116">Cell</span></span>](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[<span data-ttu-id="c304b-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="c304b-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c304b-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="c304b-118">Attributes</span></span>

<span data-ttu-id="c304b-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="c304b-119">None.</span></span>
  

