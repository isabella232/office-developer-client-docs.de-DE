---
title: TabsRow_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8b9258a0-05fa-b0b0-90ed-dc1c4faa288a
ms.openlocfilehash: d7119cc1fef637992213ce49b250291d15b66c9f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541932"
---
# <a name="tabsrowtype-complextype-visio-xml"></a><span data-ttu-id="01415-102">TabsRow_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="01415-102">TabsRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="01415-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="01415-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01415-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="01415-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="01415-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="01415-105">**Schema file**</span></span> <br/> |<span data-ttu-id="01415-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="01415-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="01415-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="01415-107">**Extension base**</span></span> <br/> |<span data-ttu-id="01415-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="01415-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="01415-109">Definition</span><span class="sxs-lookup"><span data-stu-id="01415-109">Definition</span></span>

```XML
          <xs:complexType name="TabsRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="01415-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="01415-110">Elements and attributes</span></span>

<span data-ttu-id="01415-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="01415-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="01415-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="01415-112">Child elements</span></span>

|<span data-ttu-id="01415-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="01415-113">**Element**</span></span>|<span data-ttu-id="01415-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="01415-114">**Type**</span></span>|<span data-ttu-id="01415-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="01415-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="01415-116">Cell</span><span class="sxs-lookup"><span data-stu-id="01415-116">Cell</span></span>](cell-element-tabs-sectionvisio-xml.md) <br/> |[<span data-ttu-id="01415-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="01415-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="01415-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="01415-118">Attributes</span></span>

<span data-ttu-id="01415-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="01415-119">None.</span></span>
  

