---
title: Connects_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 68a85d32-9bf2-2f7c-2797-85ddd593fc37
ms.openlocfilehash: d9a3283e9ac16af8997d7e9d632e067ecec7423d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538697"
---
# <a name="connects_type-complextype-visio-xml"></a><span data-ttu-id="27dfa-102">Connects_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="27dfa-102">Connects_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="27dfa-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="27dfa-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27dfa-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="27dfa-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="27dfa-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="27dfa-105">**Schema file**</span></span> <br/> |<span data-ttu-id="27dfa-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="27dfa-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="27dfa-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="27dfa-107">**Extension base**</span></span> <br/> |<span data-ttu-id="27dfa-108">Keine</span><span class="sxs-lookup"><span data-stu-id="27dfa-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="27dfa-109">Definition</span><span class="sxs-lookup"><span data-stu-id="27dfa-109">Definition</span></span>

```XML
          <xs:complexType name="Connects_Type">
          
          <xs:sequence>
    <xs:element name="Connect"  type="Connect_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="27dfa-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="27dfa-110">Elements and attributes</span></span>

<span data-ttu-id="27dfa-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="27dfa-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="27dfa-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="27dfa-112">Child elements</span></span>

|<span data-ttu-id="27dfa-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="27dfa-113">**Element**</span></span>|<span data-ttu-id="27dfa-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="27dfa-114">**Type**</span></span>|<span data-ttu-id="27dfa-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="27dfa-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="27dfa-116">Connect</span><span class="sxs-lookup"><span data-stu-id="27dfa-116">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="27dfa-117">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="27dfa-117">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="27dfa-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="27dfa-118">Attributes</span></span>

<span data-ttu-id="27dfa-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="27dfa-119">None.</span></span>
  

