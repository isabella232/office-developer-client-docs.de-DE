---
title: ActionsRow_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32777219-850b-9526-425f-bcb017c45093
ms.openlocfilehash: d62513877dc2c441d521b20505f5849ea31a1a4a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283003"
---
# <a name="actionsrowtype-complextype-visio-xml"></a><span data-ttu-id="d3415-102">ActionsRow_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="d3415-102">ActionsRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d3415-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="d3415-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d3415-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d3415-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d3415-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="d3415-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d3415-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="d3415-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d3415-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="d3415-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d3415-108">NamedIndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="d3415-108">NamedIndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d3415-109">Definition</span><span class="sxs-lookup"><span data-stu-id="d3415-109">Definition</span></span>

```XML
          <xs:complexType name="ActionsRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="d3415-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="d3415-110">Elements and attributes</span></span>

<span data-ttu-id="d3415-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="d3415-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d3415-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3415-112">Child elements</span></span>

|<span data-ttu-id="d3415-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d3415-113">**Element**</span></span>|<span data-ttu-id="d3415-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d3415-114">**Type**</span></span>|<span data-ttu-id="d3415-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3415-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d3415-116">Cell</span><span class="sxs-lookup"><span data-stu-id="d3415-116">Cell</span></span>](cell-element-actions-rowvisio-xml.md) <br/> |[<span data-ttu-id="d3415-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="d3415-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d3415-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="d3415-118">Attributes</span></span>

<span data-ttu-id="d3415-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="d3415-119">None.</span></span>
  

