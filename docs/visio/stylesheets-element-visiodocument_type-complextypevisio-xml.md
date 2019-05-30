---
title: Stylesheets-Element (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da26de4b-3e5b-326b-de46-e8c542b74f02
description: Enthält eine Auflistung von Stylesheet-Elementen für das Dokument.
ms.openlocfilehash: 363cb102fb545ffd20601bf0125c22aeb06defa8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541988"
---
# <a name="stylesheets-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="7fc02-103">Stylesheets-Element (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7fc02-103">StyleSheets element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="7fc02-104">Enthält eine Auflistung von Stylesheet-Elementen für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="7fc02-104">Contains a collection of StyleSheet elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7fc02-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7fc02-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7fc02-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="7fc02-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7fc02-107">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="7fc02-107">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7fc02-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7fc02-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7fc02-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="7fc02-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7fc02-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="7fc02-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7fc02-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="7fc02-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7fc02-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="7fc02-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7fc02-113">Definition</span><span class="sxs-lookup"><span data-stu-id="7fc02-113">Definition</span></span>

```XML
< xs:element name="StyleSheets" type="StyleSheets_Type" minOccurs="0" maxOccurs="1" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7fc02-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="7fc02-114">Elements and attributes</span></span>

<span data-ttu-id="7fc02-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="7fc02-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7fc02-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7fc02-116">Parent elements</span></span>

|<span data-ttu-id="7fc02-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="7fc02-117">**Element**</span></span>|<span data-ttu-id="7fc02-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7fc02-118">**Type**</span></span>|<span data-ttu-id="7fc02-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7fc02-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7fc02-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="7fc02-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="7fc02-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="7fc02-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7fc02-122">Das Stammelement eines Microsoft Visio Dokuments.</span><span class="sxs-lookup"><span data-stu-id="7fc02-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7fc02-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7fc02-123">Child elements</span></span>

|<span data-ttu-id="7fc02-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="7fc02-124">**Element**</span></span>|<span data-ttu-id="7fc02-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7fc02-125">**Type**</span></span>|<span data-ttu-id="7fc02-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7fc02-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7fc02-127">Stylesheet</span><span class="sxs-lookup"><span data-stu-id="7fc02-127">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7fc02-128">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="7fc02-128">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7fc02-129">Repräsentiert eine in einem Dokument definierte Formatvorlage.</span><span class="sxs-lookup"><span data-stu-id="7fc02-129">Represents a style defined in a document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7fc02-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="7fc02-130">Attributes</span></span>

<span data-ttu-id="7fc02-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="7fc02-131">None.</span></span>
  

