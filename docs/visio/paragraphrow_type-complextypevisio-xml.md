---
title: ParagraphRow_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32bb67e1-8db8-fe28-f173-028a20bb136c
ms.openlocfilehash: 64001e12b3e65e3259c3ebe381b2825fb80ad7b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338479"
---
# <a name="paragraphrowtype-complextype-visio-xml"></a><span data-ttu-id="9c8e7-102">ParagraphRow_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="9c8e7-102">ParagraphRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9c8e7-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="9c8e7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9c8e7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9c8e7-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9c8e7-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="9c8e7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9c8e7-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="9c8e7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9c8e7-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="9c8e7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9c8e7-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="9c8e7-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9c8e7-109">Definition</span><span class="sxs-lookup"><span data-stu-id="9c8e7-109">Definition</span></span>

```XML
          <xs:complexType name="ParagraphRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="9c8e7-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="9c8e7-110">Elements and attributes</span></span>

<span data-ttu-id="9c8e7-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="9c8e7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9c8e7-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9c8e7-112">Child elements</span></span>

|<span data-ttu-id="9c8e7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9c8e7-113">**Element**</span></span>|<span data-ttu-id="9c8e7-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9c8e7-114">**Type**</span></span>|<span data-ttu-id="9c8e7-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9c8e7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9c8e7-116">Cell</span><span class="sxs-lookup"><span data-stu-id="9c8e7-116">Cell</span></span>](cell-element-paragraph-sectionvisio-xml.md) <br/> |[<span data-ttu-id="9c8e7-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="9c8e7-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9c8e7-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="9c8e7-118">Attributes</span></span>

<span data-ttu-id="9c8e7-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="9c8e7-119">None.</span></span>
  

