---
title: PageSheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7bce473-9a3d-65f2-8323-1e00db110c71
ms.openlocfilehash: 01112db1465eece9ecf5faf200a1d866ce6e332d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540588"
---
# <a name="pagesheet_type-complextype-visio-xml"></a><span data-ttu-id="1d818-102">PageSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="1d818-102">PageSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="1d818-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="1d818-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d818-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1d818-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1d818-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="1d818-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1d818-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1d818-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1d818-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="1d818-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1d818-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="1d818-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1d818-109">Definition</span><span class="sxs-lookup"><span data-stu-id="1d818-109">Definition</span></span>

```XML
      <xs:complexType name="PageSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1d818-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="1d818-110">Elements and attributes</span></span>

<span data-ttu-id="1d818-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="1d818-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1d818-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1d818-112">Child elements</span></span>

<span data-ttu-id="1d818-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="1d818-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1d818-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="1d818-114">Attributes</span></span>

|<span data-ttu-id="1d818-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1d818-115">**Attribute**</span></span>|<span data-ttu-id="1d818-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1d818-116">**Type**</span></span>|<span data-ttu-id="1d818-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="1d818-117">**Required**</span></span>|<span data-ttu-id="1d818-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1d818-118">**Description**</span></span>|<span data-ttu-id="1d818-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="1d818-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1d818-120">UniqueID</span><span class="sxs-lookup"><span data-stu-id="1d818-120">UniqueID</span></span>  <br/> |<span data-ttu-id="1d818-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1d818-121">xsd:string</span></span>  <br/> |<span data-ttu-id="1d818-122">Optional</span><span class="sxs-lookup"><span data-stu-id="1d818-122">optional</span></span>  <br/> ||<span data-ttu-id="1d818-123">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="1d818-123">Values of the xsd:string type.</span></span>  <br/> |
   

