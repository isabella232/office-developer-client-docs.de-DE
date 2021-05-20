---
title: ConnectionRow_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 14a92d20-78fb-0043-7360-7dfda52fb9c7
ms.openlocfilehash: ad8f4f877153b871b897be7da5d5e09a5ff070fb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538732"
---
# <a name="connectionrow_type-complextype-visio-xml"></a><span data-ttu-id="26ada-102">ConnectionRow_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="26ada-102">ConnectionRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="26ada-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="26ada-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26ada-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="26ada-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="26ada-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="26ada-105">**Schema file**</span></span> <br/> |<span data-ttu-id="26ada-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="26ada-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="26ada-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="26ada-107">**Extension base**</span></span> <br/> |<span data-ttu-id="26ada-108">NamedIndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="26ada-108">NamedIndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="26ada-109">Definition</span><span class="sxs-lookup"><span data-stu-id="26ada-109">Definition</span></span>

```XML
          <xs:complexType name="ConnectionRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedIndexedRow_Type">
          <xs:all>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:all>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="26ada-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="26ada-110">Elements and attributes</span></span>

<span data-ttu-id="26ada-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="26ada-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="26ada-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="26ada-112">Child elements</span></span>

|<span data-ttu-id="26ada-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="26ada-113">**Element**</span></span>|<span data-ttu-id="26ada-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="26ada-114">**Type**</span></span>|<span data-ttu-id="26ada-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="26ada-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="26ada-116">Cell</span><span class="sxs-lookup"><span data-stu-id="26ada-116">Cell</span></span>](cell-element-connection-rowvisio-xml.md) <br/> |[<span data-ttu-id="26ada-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="26ada-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="26ada-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="26ada-118">Attributes</span></span>

<span data-ttu-id="26ada-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="26ada-119">None.</span></span>
  

