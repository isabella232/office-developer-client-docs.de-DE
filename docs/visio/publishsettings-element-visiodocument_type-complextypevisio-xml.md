---
title: PublishSettings-Element (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: Gibt die Einstellungen an, die verwendet werden, wenn das Diagramm mit Visio Services in Microsoft SharePoint Server 2013 geöffnet wird.
ms.openlocfilehash: 611dfe477228995bca6aedff27b468a2d57e7e85
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541358"
---
# <a name="publishsettings-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="ab055-103">PublishSettings-Element (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ab055-103">PublishSettings element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="ab055-104">Gibt die Einstellungen an, die verwendet werden, wenn das Diagramm mit Visio Services in Microsoft SharePoint Server 2013 geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="ab055-104">Specifies the settings that are used when the diagram is opened using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ab055-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ab055-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab055-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="ab055-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ab055-107">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="ab055-107">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ab055-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ab055-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ab055-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ab055-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ab055-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="ab055-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ab055-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="ab055-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ab055-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="ab055-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ab055-113">Definition</span><span class="sxs-lookup"><span data-stu-id="ab055-113">Definition</span></span>

```XML
< xs:element name="PublishSettings" type="PublishSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ab055-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ab055-114">Elements and attributes</span></span>

<span data-ttu-id="ab055-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="ab055-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ab055-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ab055-116">Parent elements</span></span>

|<span data-ttu-id="ab055-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="ab055-117">**Element**</span></span>|<span data-ttu-id="ab055-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ab055-118">**Type**</span></span>|<span data-ttu-id="ab055-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ab055-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ab055-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="ab055-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="ab055-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="ab055-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ab055-122">Gibt die Eigenschaften einer Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="ab055-122">Specifies properties of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ab055-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ab055-123">Child elements</span></span>

|<span data-ttu-id="ab055-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="ab055-124">**Element**</span></span>|<span data-ttu-id="ab055-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ab055-125">**Type**</span></span>|<span data-ttu-id="ab055-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ab055-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ab055-127">PublishedPage</span><span class="sxs-lookup"><span data-stu-id="ab055-127">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ab055-128">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="ab055-128">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ab055-129">Gibt an, ob ein Zeichenblatt im Browser mit Visio Services angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab055-129">Specifies whether a drawing page is viewable in the browser using Visio Services.</span></span>  <br/> |
|[<span data-ttu-id="ab055-130">RefreshableData</span><span class="sxs-lookup"><span data-stu-id="ab055-130">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ab055-131">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="ab055-131">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ab055-132">Gibt an, ob ein Recordset-Objekt mit Visio Services aktualisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ab055-132">Specifies whether a recordset is refreshable using Visio Services.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ab055-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="ab055-133">Attributes</span></span>

<span data-ttu-id="ab055-134">Keine.</span><span class="sxs-lookup"><span data-stu-id="ab055-134">None.</span></span>
  

