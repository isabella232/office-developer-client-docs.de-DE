---
title: FooterMargin_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db8d1e5b-cd29-f9ff-994a-25c28672db81
ms.openlocfilehash: f5838855a5c21b699c7a81849b9afc40790f3d01
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538641"
---
# <a name="footermargin_type-complextype-visio-xml"></a><span data-ttu-id="1883c-102">FooterMargin_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="1883c-102">FooterMargin_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="1883c-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="1883c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1883c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1883c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1883c-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="1883c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1883c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1883c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1883c-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="1883c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1883c-108">xsd:double</span><span class="sxs-lookup"><span data-stu-id="1883c-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1883c-109">Definition</span><span class="sxs-lookup"><span data-stu-id="1883c-109">Definition</span></span>

```XML
      <xs:complexType name="FooterMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1883c-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="1883c-110">Elements and attributes</span></span>

<span data-ttu-id="1883c-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="1883c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1883c-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1883c-112">Child elements</span></span>

<span data-ttu-id="1883c-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="1883c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1883c-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="1883c-114">Attributes</span></span>

|<span data-ttu-id="1883c-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1883c-115">**Attribute**</span></span>|<span data-ttu-id="1883c-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1883c-116">**Type**</span></span>|<span data-ttu-id="1883c-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="1883c-117">**Required**</span></span>|<span data-ttu-id="1883c-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1883c-118">**Description**</span></span>|<span data-ttu-id="1883c-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="1883c-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1883c-120">Unit</span><span class="sxs-lookup"><span data-stu-id="1883c-120">Unit</span></span>  <br/> |<span data-ttu-id="1883c-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1883c-121">xsd:string</span></span>  <br/> |<span data-ttu-id="1883c-122">Optional</span><span class="sxs-lookup"><span data-stu-id="1883c-122">optional</span></span>  <br/> ||<span data-ttu-id="1883c-123">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="1883c-123">Values of the xsd:string type.</span></span>  <br/> |
   

