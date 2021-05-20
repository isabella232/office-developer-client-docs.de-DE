---
title: LineGradientRow_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b35d58b-ec6f-9b99-01fb-c665630e65d7
ms.openlocfilehash: 9c39ddd971f3089bb8b87026616c455e6a0524eb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541141"
---
# <a name="linegradientrow_type-complextype-visio-xml"></a><span data-ttu-id="8ad87-102">LineGradientRow_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="8ad87-102">LineGradientRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="8ad87-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="8ad87-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ad87-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8ad87-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8ad87-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="8ad87-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8ad87-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8ad87-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8ad87-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="8ad87-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8ad87-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="8ad87-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8ad87-109">Definition</span><span class="sxs-lookup"><span data-stu-id="8ad87-109">Definition</span></span>

```XML
          <xs:complexType name="LineGradientRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8ad87-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="8ad87-110">Elements and attributes</span></span>

<span data-ttu-id="8ad87-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="8ad87-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8ad87-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8ad87-112">Child elements</span></span>

|<span data-ttu-id="8ad87-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="8ad87-113">**Element**</span></span>|<span data-ttu-id="8ad87-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="8ad87-114">**Type**</span></span>|<span data-ttu-id="8ad87-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8ad87-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8ad87-116">Cell</span><span class="sxs-lookup"><span data-stu-id="8ad87-116">Cell</span></span>](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="8ad87-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="8ad87-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="8ad87-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="8ad87-118">Attributes</span></span>

<span data-ttu-id="8ad87-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="8ad87-119">None.</span></span>
  

