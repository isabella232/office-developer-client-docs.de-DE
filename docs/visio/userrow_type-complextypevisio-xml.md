---
title: UserRow_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae2e014b-2e53-c317-0bfa-9a0cb1e09588
ms.openlocfilehash: aed034bb2f8ced384e8c7c9c82b9be7570988332
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538557"
---
# <a name="userrowtype-complextype-visio-xml"></a><span data-ttu-id="37eca-102">UserRow_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="37eca-102">UserRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="37eca-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="37eca-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37eca-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="37eca-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="37eca-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="37eca-105">**Schema file**</span></span> <br/> |<span data-ttu-id="37eca-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="37eca-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="37eca-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="37eca-107">**Extension base**</span></span> <br/> |<span data-ttu-id="37eca-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="37eca-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="37eca-109">Definition</span><span class="sxs-lookup"><span data-stu-id="37eca-109">Definition</span></span>

```XML
          <xs:complexType name="UserRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="37eca-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="37eca-110">Elements and attributes</span></span>

<span data-ttu-id="37eca-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="37eca-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="37eca-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="37eca-112">Child elements</span></span>

|<span data-ttu-id="37eca-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="37eca-113">**Element**</span></span>|<span data-ttu-id="37eca-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="37eca-114">**Type**</span></span>|<span data-ttu-id="37eca-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="37eca-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="37eca-116">Cell</span><span class="sxs-lookup"><span data-stu-id="37eca-116">Cell</span></span>](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="37eca-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="37eca-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="37eca-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="37eca-118">Attributes</span></span>

<span data-ttu-id="37eca-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="37eca-119">None.</span></span>
  

