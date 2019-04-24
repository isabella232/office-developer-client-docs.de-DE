---
title: LineGradientRow_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b35d58b-ec6f-9b99-01fb-c665630e65d7
ms.openlocfilehash: e48172e8213359244a61716d208b8b98776429af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361131"
---
# <a name="linegradientrowtype-complextype-visio-xml"></a><span data-ttu-id="6d259-102">LineGradientRow_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="6d259-102">LineGradientRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6d259-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="6d259-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d259-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6d259-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6d259-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="6d259-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6d259-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="6d259-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6d259-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="6d259-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6d259-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="6d259-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6d259-109">Definition</span><span class="sxs-lookup"><span data-stu-id="6d259-109">Definition</span></span>

```XML
          <xs:complexType name="LineGradientRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="6d259-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="6d259-110">Elements and attributes</span></span>

<span data-ttu-id="6d259-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="6d259-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6d259-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6d259-112">Child elements</span></span>

|<span data-ttu-id="6d259-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6d259-113">**Element**</span></span>|<span data-ttu-id="6d259-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6d259-114">**Type**</span></span>|<span data-ttu-id="6d259-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6d259-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6d259-116">Cell</span><span class="sxs-lookup"><span data-stu-id="6d259-116">Cell</span></span>](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="6d259-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="6d259-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6d259-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="6d259-118">Attributes</span></span>

<span data-ttu-id="6d259-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="6d259-119">None.</span></span>
  

