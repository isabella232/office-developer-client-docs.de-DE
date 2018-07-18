---
title: Issues_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f326e227-f68e-27d6-268e-1ae935516dbc
ms.openlocfilehash: 1ebec9e42c71b93637155037bd881c8ddf330367
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797255"
---
# <a name="issuestype-complextype-visio-xml"></a><span data-ttu-id="e2352-102">Issues_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="e2352-102">Issues_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e2352-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="e2352-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2352-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e2352-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e2352-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="e2352-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e2352-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e2352-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e2352-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="e2352-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e2352-108">Keine</span><span class="sxs-lookup"><span data-stu-id="e2352-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e2352-109">Definition</span><span class="sxs-lookup"><span data-stu-id="e2352-109">Definition</span></span>

```XML
          <xs:complexType name="Issues_Type">
          
          <xs:sequence>
    <xs:element name="Issue"  type="Issue_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e2352-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="e2352-110">Elements and attributes</span></span>

<span data-ttu-id="e2352-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="e2352-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e2352-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e2352-112">Child elements</span></span>

|<span data-ttu-id="e2352-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e2352-113">**Element**</span></span>|<span data-ttu-id="e2352-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="e2352-114">**Type**</span></span>|<span data-ttu-id="e2352-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e2352-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e2352-116">Problem</span><span class="sxs-lookup"><span data-stu-id="e2352-116">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e2352-117">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="e2352-117">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e2352-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="e2352-118">Attributes</span></span>

<span data-ttu-id="e2352-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="e2352-119">None.</span></span>
  

