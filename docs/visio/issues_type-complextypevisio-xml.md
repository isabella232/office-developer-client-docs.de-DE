---
title: Issues_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f326e227-f68e-27d6-268e-1ae935516dbc
ms.openlocfilehash: 160afddb1352a93050496a9b3497a3e3b6f2e585
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538109"
---
# <a name="issues_type-complextype-visio-xml"></a><span data-ttu-id="e32a2-102">Issues_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e32a2-102">Issues_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="e32a2-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="e32a2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e32a2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e32a2-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e32a2-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="e32a2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e32a2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e32a2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e32a2-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="e32a2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e32a2-108">Keine</span><span class="sxs-lookup"><span data-stu-id="e32a2-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e32a2-109">Definition</span><span class="sxs-lookup"><span data-stu-id="e32a2-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="e32a2-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="e32a2-110">Elements and attributes</span></span>

<span data-ttu-id="e32a2-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="e32a2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e32a2-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e32a2-112">Child elements</span></span>

|<span data-ttu-id="e32a2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e32a2-113">**Element**</span></span>|<span data-ttu-id="e32a2-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="e32a2-114">**Type**</span></span>|<span data-ttu-id="e32a2-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e32a2-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e32a2-116">Problem</span><span class="sxs-lookup"><span data-stu-id="e32a2-116">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e32a2-117">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="e32a2-117">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e32a2-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="e32a2-118">Attributes</span></span>

<span data-ttu-id="e32a2-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="e32a2-119">None.</span></span>
  

