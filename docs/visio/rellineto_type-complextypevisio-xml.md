---
title: RelLineTo_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e5504166-653d-15d2-75eb-9b36f376b788
ms.openlocfilehash: 953130a69e477aeef836aa8b95d3979e84e8ba79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797811"
---
# <a name="rellinetotype-complextype-visio-xml"></a><span data-ttu-id="75fa8-102">RelLineTo_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="75fa8-102">RelLineTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="75fa8-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="75fa8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75fa8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="75fa8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="75fa8-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="75fa8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="75fa8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="75fa8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="75fa8-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="75fa8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="75fa8-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="75fa8-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="75fa8-109">Definition</span><span class="sxs-lookup"><span data-stu-id="75fa8-109">Definition</span></span>

```XML
          <xs:complexType name="RelLineTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="75fa8-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="75fa8-110">Elements and attributes</span></span>

<span data-ttu-id="75fa8-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="75fa8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="75fa8-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="75fa8-112">Child elements</span></span>

|<span data-ttu-id="75fa8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="75fa8-113">**Element**</span></span>|<span data-ttu-id="75fa8-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="75fa8-114">**Type**</span></span>|<span data-ttu-id="75fa8-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="75fa8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="75fa8-116">Cell</span><span class="sxs-lookup"><span data-stu-id="75fa8-116">Cell</span></span>](cell-element-rellineto-rowvisio-xml.md) <br/> |[<span data-ttu-id="75fa8-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="75fa8-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="75fa8-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="75fa8-118">Attributes</span></span>

<span data-ttu-id="75fa8-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="75fa8-119">None.</span></span>
  

