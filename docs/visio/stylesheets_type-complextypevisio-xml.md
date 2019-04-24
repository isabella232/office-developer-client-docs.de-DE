---
title: StyleSheets_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2603bc5-86bd-df29-43c2-25a39419ad1e
ms.openlocfilehash: 1992f0e31ae972320f80f99d94164fbd1dbc6d45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346781"
---
# <a name="stylesheetstype-complextype-visio-xml"></a><span data-ttu-id="09ef0-102">StyleSheets_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="09ef0-102">StyleSheets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="09ef0-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="09ef0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09ef0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="09ef0-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="09ef0-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="09ef0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="09ef0-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="09ef0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="09ef0-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="09ef0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="09ef0-108">Keine</span><span class="sxs-lookup"><span data-stu-id="09ef0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="09ef0-109">Definition</span><span class="sxs-lookup"><span data-stu-id="09ef0-109">Definition</span></span>

```XML
          <xs:complexType name="StyleSheets_Type">
          
          <xs:sequence>
    <xs:element name="StyleSheet"  type="StyleSheet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="09ef0-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="09ef0-110">Elements and attributes</span></span>

<span data-ttu-id="09ef0-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="09ef0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="09ef0-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="09ef0-112">Child elements</span></span>

|<span data-ttu-id="09ef0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="09ef0-113">**Element**</span></span>|<span data-ttu-id="09ef0-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="09ef0-114">**Type**</span></span>|<span data-ttu-id="09ef0-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="09ef0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="09ef0-116">StyleSheet</span><span class="sxs-lookup"><span data-stu-id="09ef0-116">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="09ef0-117">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="09ef0-117">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="09ef0-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="09ef0-118">Attributes</span></span>

<span data-ttu-id="09ef0-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="09ef0-119">None.</span></span>
  

