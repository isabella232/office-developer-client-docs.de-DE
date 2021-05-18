---
title: HYPERLINK-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251441
localization_priority: Normal
ms.assetid: 943636a6-e135-a626-7924-11e238156548
description: Navigiert zur angegebenen Adresse, bei der es sich um einen Datei-, UNC- oder URL-Pfad gehen kann.
ms.openlocfilehash: 5e4952c3d56eff0cb1e6518928a7b8259f645046
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329946"
---
# <a name="hyperlink-function"></a><span data-ttu-id="5d144-103">HYPERLINK Function</span><span class="sxs-lookup"><span data-stu-id="5d144-103">HYPERLINK Function</span></span>

<span data-ttu-id="5d144-104">Navigiert zur angegebenen Adresse, bei der es sich um einen Datei-, UNC- oder URL-Pfad gehen kann.</span><span class="sxs-lookup"><span data-stu-id="5d144-104">Navigates to the specified address, which can be a file, UNC, or URL path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5d144-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d144-105">Syntax</span></span>

<span data-ttu-id="5d144-106">HYPERLINK(" \*\* *address* \*\* "[," \*\* *subaddress* \*\* "," \*\* *extrainfo* \*\* ", \*\* *window* \*\*," \*\* *frame* \*\* "])</span><span class="sxs-lookup"><span data-stu-id="5d144-106">HYPERLINK(" \*\* *address* \*\* "[," \*\* *subaddress* \*\* "," \*\* *extrainfo* \*\* ", \*\* *window* \*\*," \*\* *frame* \*\* "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5d144-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d144-107">Parameters</span></span>

|<span data-ttu-id="5d144-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="5d144-108">**Name**</span></span>|<span data-ttu-id="5d144-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="5d144-109">**Required/Optional**</span></span>|<span data-ttu-id="5d144-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="5d144-110">**Data Type**</span></span>|<span data-ttu-id="5d144-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5d144-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5d144-112">_address_</span><span class="sxs-lookup"><span data-stu-id="5d144-112">_address_</span></span> <br/> |<span data-ttu-id="5d144-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5d144-113">Required</span></span>  <br/> |<span data-ttu-id="5d144-114">**String**</span><span class="sxs-lookup"><span data-stu-id="5d144-114">**String**</span></span> <br/> |<span data-ttu-id="5d144-115">Ein vollständiger Pfad oder ein relativer Pfad.</span><span class="sxs-lookup"><span data-stu-id="5d144-115">A full path or a relative path.</span></span>  <br/> |
| <span data-ttu-id="5d144-116">_subaddress_</span><span class="sxs-lookup"><span data-stu-id="5d144-116">_subaddress_</span></span> <br/> |<span data-ttu-id="5d144-117">Optional</span><span class="sxs-lookup"><span data-stu-id="5d144-117">Optional</span></span>  <br/> |<span data-ttu-id="5d144-118">**String**</span><span class="sxs-lookup"><span data-stu-id="5d144-118">**String**</span></span> <br/> |<span data-ttu-id="5d144-p101">Gibt eine Position innerhalb von address an, mit der eine Verknüpfung hergestellt werden soll. Wenn es sich bei address beispielsweise um eine Microsoft Visio-Datei handelt, kann subaddress ein Zeichenblattname sein. Wenn es sich um eine Microsoft Excel-Datei handelt, kann subaddress ein Arbeitsblatt oder ein Arbeitsblattbereich sein. Wenn es sich um eine URL für eine HTML-Seite handelt, kann sich subaddress auf einen Anker beziehen.</span><span class="sxs-lookup"><span data-stu-id="5d144-p101">Specifies a location within address to link to. For example, if address is a Microsoft Visio file, subaddress can be a page name; if a Microsoft Excel file, subaddress can be a worksheet or range within a worksheet; if a URL for an HTML page, subaddress can be an anchor.</span></span>  <br/> |
| <span data-ttu-id="5d144-121">_extrainfo_</span><span class="sxs-lookup"><span data-stu-id="5d144-121">_extrainfo_</span></span> <br/> |<span data-ttu-id="5d144-122">Optional</span><span class="sxs-lookup"><span data-stu-id="5d144-122">Optional</span></span>  <br/> |<span data-ttu-id="5d144-123">**String**</span><span class="sxs-lookup"><span data-stu-id="5d144-123">**String**</span></span> <br/> |<span data-ttu-id="5d144-124">Übergibt Informationen, die bei der Auflösung der URL verwendet werden, z. B. die Koordinaten für eine Imagemap.</span><span class="sxs-lookup"><span data-stu-id="5d144-124">Passes information used in resolving the URL, such as the coordinates of an image map.</span></span>  <br/> |
| <span data-ttu-id="5d144-125">_window_</span><span class="sxs-lookup"><span data-stu-id="5d144-125">_window_</span></span> <br/> |<span data-ttu-id="5d144-126">Optional</span><span class="sxs-lookup"><span data-stu-id="5d144-126">Optional</span></span>  <br/> |<span data-ttu-id="5d144-127">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="5d144-127">**Boolean**</span></span> <br/> |<span data-ttu-id="5d144-p102">Legt fest, ob der Hyperlink in einem neuen Fenster geöffnet wird. Die Standardeinstellung lautet FALSE.</span><span class="sxs-lookup"><span data-stu-id="5d144-p102">Specifies whether the hyperlink is opened in a new window. The default value is FALSE.</span></span>  <br/> |
| <span data-ttu-id="5d144-130">_frame_</span><span class="sxs-lookup"><span data-stu-id="5d144-130">_frame_</span></span> <br/> |<span data-ttu-id="5d144-131">Optional</span><span class="sxs-lookup"><span data-stu-id="5d144-131">Optional</span></span>  <br/> |<span data-ttu-id="5d144-132">**String**</span><span class="sxs-lookup"><span data-stu-id="5d144-132">**String**</span></span> <br/> | <span data-ttu-id="5d144-p103">Legt den Namen eines Frames zu einem Ziel fest, wenn Visio als aktives Dokument in einem ActiveX-Browser, z. B. Microsoft Internet Explorer 3.0 oder höher, geöffnet ist. Die Standardeinstellung ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="5d144-p103">Specifies the name of a frame to target when Visio is open as an Active document in an ActiveX browser, such as Microsoft Internet Explorer 3.0 or later. The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d144-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5d144-135">Remarks</span></span>

<span data-ttu-id="5d144-p104">Wenn das Dokument keinen Basispfad besitzt, navigiert Visio relativ zum Dokumentpfad. Wenn das Dokument noch nicht gespeichert wurde, bleibt der Hyperlink undefiniert.</span><span class="sxs-lookup"><span data-stu-id="5d144-p104">If the document has no base path, Visio navigates according to the document path. If the document has not been saved, the hyperlink is undefined.</span></span> 
  
<span data-ttu-id="5d144-138">Relative Pfade basieren auf dem Feld **Hyperlinkbasis**, das im Dialogfeld **Visio Eigenschaften** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5d144-138">Relative paths are based on the **Hyperlink base** field specified in the **Visio Properties** dialog box.</span></span> 
  
<span data-ttu-id="5d144-139">Sie können die GOTOPAGE-Funktion nutzen, um zu den Zeichenblättern eines Dokuments zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="5d144-139">You can use the GOTOPAGE function to navigate to pages of a document.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="5d144-140">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5d144-140">Example 1</span></span>

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a><span data-ttu-id="5d144-141">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5d144-141">Example 2</span></span>

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a><span data-ttu-id="5d144-142">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5d144-142">Example 3</span></span>

 `HYPERLINK("https://www.microsoft.com")`
  
## <a name="example-4"></a><span data-ttu-id="5d144-143">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="5d144-143">Example 4</span></span>

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

