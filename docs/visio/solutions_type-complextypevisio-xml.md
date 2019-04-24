---
title: Solutions_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74978183-8513-b359-0501-6094e072ac8e
ms.openlocfilehash: bf43b971399ec69c6f73cbfaaa6cade8c583d3c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334426"
---
# <a name="solutionstype-complextype-visio-xml"></a><span data-ttu-id="4fe06-102">Solutions_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="4fe06-102">Solutions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4fe06-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="4fe06-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4fe06-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4fe06-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4fe06-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="4fe06-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4fe06-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="4fe06-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4fe06-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="4fe06-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4fe06-108">Keine</span><span class="sxs-lookup"><span data-stu-id="4fe06-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4fe06-109">Definition</span><span class="sxs-lookup"><span data-stu-id="4fe06-109">Definition</span></span>

```XML
          <xs:complexType name="Solutions_Type">
          
          <xs:sequence>
    <xs:element name="Solution"  type="Solution_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4fe06-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="4fe06-110">Elements and attributes</span></span>

<span data-ttu-id="4fe06-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="4fe06-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4fe06-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4fe06-112">Child elements</span></span>

|<span data-ttu-id="4fe06-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4fe06-113">**Element**</span></span>|<span data-ttu-id="4fe06-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4fe06-114">**Type**</span></span>|<span data-ttu-id="4fe06-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4fe06-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4fe06-116">Solution</span><span class="sxs-lookup"><span data-stu-id="4fe06-116">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4fe06-117">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="4fe06-117">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4fe06-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="4fe06-118">Attributes</span></span>

<span data-ttu-id="4fe06-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="4fe06-119">None.</span></span>
  

