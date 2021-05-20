---
title: AuthorList_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc1e059b-7705-8b30-aeab-f56707086416
ms.openlocfilehash: 5df48bcc69f0bd4aa818f265d0c7db1986165b3e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537899"
---
# <a name="authorlist_type-complextype-visio-xml"></a><span data-ttu-id="5fbbd-102">AuthorList_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5fbbd-102">AuthorList_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="5fbbd-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="5fbbd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5fbbd-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5fbbd-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5fbbd-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="5fbbd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5fbbd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5fbbd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5fbbd-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="5fbbd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5fbbd-108">Keine</span><span class="sxs-lookup"><span data-stu-id="5fbbd-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5fbbd-109">Definition</span><span class="sxs-lookup"><span data-stu-id="5fbbd-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="5fbbd-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="5fbbd-110">Elements and attributes</span></span>

<span data-ttu-id="5fbbd-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="5fbbd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5fbbd-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5fbbd-112">Child elements</span></span>

|<span data-ttu-id="5fbbd-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5fbbd-113">**Element**</span></span>|<span data-ttu-id="5fbbd-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="5fbbd-114">**Type**</span></span>|<span data-ttu-id="5fbbd-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5fbbd-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5fbbd-116">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="5fbbd-116">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5fbbd-117">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="5fbbd-117">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5fbbd-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="5fbbd-118">Attributes</span></span>

<span data-ttu-id="5fbbd-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="5fbbd-119">None.</span></span>
  

