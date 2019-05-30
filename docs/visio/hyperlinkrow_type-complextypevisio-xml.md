---
title: HyperlinkRow_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f8ded1a6-3bbd-0d59-c9f0-ab84341888cd
ms.openlocfilehash: 64705604ce12f032f49827b28fa3e61e879f2162
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541505"
---
# <a name="hyperlinkrowtype-complextype-visio-xml"></a><span data-ttu-id="db794-102">HyperlinkRow_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="db794-102">HyperlinkRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="db794-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="db794-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db794-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="db794-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="db794-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="db794-105">**Schema file**</span></span> <br/> |<span data-ttu-id="db794-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="db794-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="db794-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="db794-107">**Extension base**</span></span> <br/> |<span data-ttu-id="db794-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="db794-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="db794-109">Definition</span><span class="sxs-lookup"><span data-stu-id="db794-109">Definition</span></span>

```XML
          <xs:complexType name="HyperlinkRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="db794-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="db794-110">Elements and attributes</span></span>

<span data-ttu-id="db794-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="db794-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="db794-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="db794-112">Child elements</span></span>

|<span data-ttu-id="db794-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="db794-113">**Element**</span></span>|<span data-ttu-id="db794-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="db794-114">**Type**</span></span>|<span data-ttu-id="db794-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="db794-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="db794-116">Cell</span><span class="sxs-lookup"><span data-stu-id="db794-116">Cell</span></span>](cell-element-hyperlink-rowvisio-xml.md) <br/> |[<span data-ttu-id="db794-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="db794-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="db794-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="db794-118">Attributes</span></span>

<span data-ttu-id="db794-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="db794-119">None.</span></span>
  

