---
title: Issues_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f326e227-f68e-27d6-268e-1ae935516dbc
ms.openlocfilehash: 42482db0c4542398381bc02ec5b21a8b80fac62f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397233"
---
# <a name="issuestype-complextype-visio-xml"></a><span data-ttu-id="91630-102">Issues_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="91630-102">Issues_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="91630-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="91630-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91630-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="91630-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="91630-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="91630-105">**Schema file**</span></span> <br/> |<span data-ttu-id="91630-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="91630-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="91630-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="91630-107">**Extension base**</span></span> <br/> |<span data-ttu-id="91630-108">Keine</span><span class="sxs-lookup"><span data-stu-id="91630-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="91630-109">Definition</span><span class="sxs-lookup"><span data-stu-id="91630-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="91630-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="91630-110">Elements and attributes</span></span>

<span data-ttu-id="91630-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="91630-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="91630-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="91630-112">Child elements</span></span>

|<span data-ttu-id="91630-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="91630-113">**Element**</span></span>|<span data-ttu-id="91630-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="91630-114">**Type**</span></span>|<span data-ttu-id="91630-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="91630-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="91630-116">Problem</span><span class="sxs-lookup"><span data-stu-id="91630-116">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="91630-117">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="91630-117">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="91630-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="91630-118">Attributes</span></span>

<span data-ttu-id="91630-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="91630-119">None.</span></span>
  

