---
title: PolylineTo_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e0b87cc0-397d-7640-34ea-2a725d8f0999
ms.openlocfilehash: 051054b8ad95438392a006814331d75e4721d0e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797646"
---
# <a name="polylinetotype-complextype-visio-xml"></a><span data-ttu-id="b3624-102">PolylineTo_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="b3624-102">PolylineTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b3624-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="b3624-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b3624-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b3624-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b3624-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="b3624-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b3624-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b3624-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b3624-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="b3624-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b3624-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="b3624-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b3624-109">Definition</span><span class="sxs-lookup"><span data-stu-id="b3624-109">Definition</span></span>

```XML
          <xs:complexType name="PolylineTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="b3624-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="b3624-110">Elements and attributes</span></span>

<span data-ttu-id="b3624-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="b3624-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b3624-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b3624-112">Child elements</span></span>

|<span data-ttu-id="b3624-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b3624-113">**Element**</span></span>|<span data-ttu-id="b3624-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b3624-114">**Type**</span></span>|<span data-ttu-id="b3624-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b3624-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b3624-116">Cell</span><span class="sxs-lookup"><span data-stu-id="b3624-116">Cell</span></span>](cell-element-polylineto-rowvisio-xml.md) <br/> |[<span data-ttu-id="b3624-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="b3624-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b3624-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="b3624-118">Attributes</span></span>

<span data-ttu-id="b3624-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="b3624-119">None.</span></span>
  

