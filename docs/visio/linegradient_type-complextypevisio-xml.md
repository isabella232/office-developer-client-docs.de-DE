---
title: LineGradient_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b36eb8f-d1af-9bbc-2822-0c3d09dfc2a9
ms.openlocfilehash: 6be5575336b3fb3ae014abd2685733ce4889f841
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541169"
---
# <a name="linegradienttype-complextype-visio-xml"></a><span data-ttu-id="8bcb9-102">LineGradient_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="8bcb9-102">LineGradient_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="8bcb9-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="8bcb9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8bcb9-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8bcb9-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8bcb9-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="8bcb9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8bcb9-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="8bcb9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8bcb9-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="8bcb9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8bcb9-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="8bcb9-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8bcb9-109">Definition</span><span class="sxs-lookup"><span data-stu-id="8bcb9-109">Definition</span></span>

```XML
          <xs:complexType name="LineGradient_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="LineGradientRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8bcb9-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="8bcb9-110">Elements and attributes</span></span>

<span data-ttu-id="8bcb9-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="8bcb9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8bcb9-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8bcb9-112">Child elements</span></span>

|<span data-ttu-id="8bcb9-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="8bcb9-113">**Element**</span></span>|<span data-ttu-id="8bcb9-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="8bcb9-114">**Type**</span></span>|<span data-ttu-id="8bcb9-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8bcb9-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8bcb9-116">Row</span><span class="sxs-lookup"><span data-stu-id="8bcb9-116">Row</span></span>](row-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="8bcb9-117">LineGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="8bcb9-117">LineGradientRow_Type</span></span>](linegradientrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="8bcb9-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="8bcb9-118">Attributes</span></span>

<span data-ttu-id="8bcb9-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="8bcb9-119">None.</span></span>
  

