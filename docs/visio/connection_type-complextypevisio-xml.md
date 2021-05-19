---
title: Connection_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c0ac13b-70cc-398b-a1a3-e7d8080c8f7b
ms.openlocfilehash: c079a7b1b12dec66d589adc1c6eb869cef0a1ed0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542506"
---
# <a name="connection_type-complextype-visio-xml"></a><span data-ttu-id="d8beb-102">Connection_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d8beb-102">Connection_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d8beb-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="d8beb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8beb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d8beb-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d8beb-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="d8beb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d8beb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d8beb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d8beb-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="d8beb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d8beb-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="d8beb-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d8beb-109">Definition</span><span class="sxs-lookup"><span data-stu-id="d8beb-109">Definition</span></span>

```XML
          <xs:complexType name="Connection_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ConnectionRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d8beb-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="d8beb-110">Elements and attributes</span></span>

<span data-ttu-id="d8beb-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="d8beb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d8beb-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d8beb-112">Child elements</span></span>

|<span data-ttu-id="d8beb-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d8beb-113">**Element**</span></span>|<span data-ttu-id="d8beb-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d8beb-114">**Type**</span></span>|<span data-ttu-id="d8beb-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d8beb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d8beb-116">Row</span><span class="sxs-lookup"><span data-stu-id="d8beb-116">Row</span></span>](row-element-connection-sectionvisio-xml.md) <br/> |[<span data-ttu-id="d8beb-117">ConnectionRow_Type</span><span class="sxs-lookup"><span data-stu-id="d8beb-117">ConnectionRow_Type</span></span>](connectionrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d8beb-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="d8beb-118">Attributes</span></span>

<span data-ttu-id="d8beb-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="d8beb-119">None.</span></span>
  

