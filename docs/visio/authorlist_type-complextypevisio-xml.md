---
title: AuthorList_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc1e059b-7705-8b30-aeab-f56707086416
ms.openlocfilehash: 80a0dd01b3628bc44ed469ff7c236753d7677f51
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338745"
---
# <a name="authorlisttype-complextype-visio-xml"></a><span data-ttu-id="4a720-102">AuthorList_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="4a720-102">AuthorList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4a720-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="4a720-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4a720-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4a720-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4a720-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="4a720-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4a720-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="4a720-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4a720-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="4a720-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4a720-108">Keine</span><span class="sxs-lookup"><span data-stu-id="4a720-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4a720-109">Definition</span><span class="sxs-lookup"><span data-stu-id="4a720-109">Definition</span></span>

```XML
          <xs:complexType name="AuthorList_Type">
          
          <xs:sequence>
    <xs:element name="AuthorEntry"  type="AuthorEntry_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4a720-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="4a720-110">Elements and attributes</span></span>

<span data-ttu-id="4a720-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="4a720-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4a720-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4a720-112">Child elements</span></span>

|<span data-ttu-id="4a720-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4a720-113">**Element**</span></span>|<span data-ttu-id="4a720-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4a720-114">**Type**</span></span>|<span data-ttu-id="4a720-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4a720-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4a720-116">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="4a720-116">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a720-117">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="4a720-117">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4a720-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="4a720-118">Attributes</span></span>

<span data-ttu-id="4a720-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="4a720-119">None.</span></span>
  

