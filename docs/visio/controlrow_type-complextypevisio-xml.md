---
title: ControlRow_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f9ee251-e685-e56c-3c8a-cb727ad62064
ms.openlocfilehash: 8d9e5e2b627930ab795639150ea1109517039f3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796739"
---
# <a name="controlrowtype-complextype-visio-xml"></a><span data-ttu-id="e6cbd-102">ControlRow_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="e6cbd-102">ControlRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e6cbd-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="e6cbd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e6cbd-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e6cbd-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e6cbd-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="e6cbd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e6cbd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e6cbd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e6cbd-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="e6cbd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e6cbd-108">NamedIndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="e6cbd-108">NamedIndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e6cbd-109">Definition</span><span class="sxs-lookup"><span data-stu-id="e6cbd-109">Definition</span></span>

```XML
          <xs:complexType name="ControlRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedIndexedRow_Type">
          <xs:all>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:all>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e6cbd-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="e6cbd-110">Elements and attributes</span></span>

<span data-ttu-id="e6cbd-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="e6cbd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e6cbd-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e6cbd-112">Child elements</span></span>

|<span data-ttu-id="e6cbd-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e6cbd-113">**Element**</span></span>|<span data-ttu-id="e6cbd-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="e6cbd-114">**Type**</span></span>|<span data-ttu-id="e6cbd-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e6cbd-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e6cbd-116">Cell</span><span class="sxs-lookup"><span data-stu-id="e6cbd-116">Cell</span></span>](cell-element-controls-rowvisio-xml.md) <br/> |[<span data-ttu-id="e6cbd-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="e6cbd-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e6cbd-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="e6cbd-118">Attributes</span></span>

<span data-ttu-id="e6cbd-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="e6cbd-119">None.</span></span>
  

