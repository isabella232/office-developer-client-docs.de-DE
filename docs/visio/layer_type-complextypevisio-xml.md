---
title: Layer_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f92ac1cc-fad2-dab9-5507-838c006ed633
ms.openlocfilehash: 9e6e477e97a0c8f1be1a89bd14262bb4c2a0d7dc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396699"
---
# <a name="layertype-complextype-visio-xml"></a><span data-ttu-id="b320d-102">Layer_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="b320d-102">Layer_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b320d-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="b320d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b320d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b320d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b320d-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="b320d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b320d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b320d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b320d-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="b320d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b320d-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="b320d-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b320d-109">Definition</span><span class="sxs-lookup"><span data-stu-id="b320d-109">Definition</span></span>

```XML
          <xs:complexType name="Layer_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="LayerRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b320d-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="b320d-110">Elements and attributes</span></span>

<span data-ttu-id="b320d-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="b320d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b320d-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b320d-112">Child elements</span></span>

|<span data-ttu-id="b320d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b320d-113">**Element**</span></span>|<span data-ttu-id="b320d-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b320d-114">**Type**</span></span>|<span data-ttu-id="b320d-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b320d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b320d-116">Row</span><span class="sxs-lookup"><span data-stu-id="b320d-116">Row</span></span>](row-element-layer-sectionvisio-xml.md) <br/> |[<span data-ttu-id="b320d-117">LayerRow_Type</span><span class="sxs-lookup"><span data-stu-id="b320d-117">LayerRow_Type</span></span>](layerrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b320d-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="b320d-118">Attributes</span></span>

<span data-ttu-id="b320d-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="b320d-119">None.</span></span>
  

