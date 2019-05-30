---
title: StyleSheets_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2603bc5-86bd-df29-43c2-25a39419ad1e
ms.openlocfilehash: 845580f2842c098cfb16776b9ab1d5d513ef8e22
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538886"
---
# <a name="stylesheetstype-complextype-visio-xml"></a><span data-ttu-id="1e047-102">StyleSheets_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="1e047-102">StyleSheets_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="1e047-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="1e047-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e047-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1e047-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1e047-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="1e047-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1e047-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="1e047-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1e047-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="1e047-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1e047-108">Keine</span><span class="sxs-lookup"><span data-stu-id="1e047-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1e047-109">Definition</span><span class="sxs-lookup"><span data-stu-id="1e047-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1e047-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="1e047-110">Elements and attributes</span></span>

<span data-ttu-id="1e047-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="1e047-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1e047-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1e047-112">Child elements</span></span>

|<span data-ttu-id="1e047-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1e047-113">**Element**</span></span>|<span data-ttu-id="1e047-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1e047-114">**Type**</span></span>|<span data-ttu-id="1e047-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1e047-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1e047-116">Stylesheet</span><span class="sxs-lookup"><span data-stu-id="1e047-116">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1e047-117">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="1e047-117">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1e047-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="1e047-118">Attributes</span></span>

<span data-ttu-id="1e047-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="1e047-119">None.</span></span>
  

